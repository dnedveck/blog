---
layout: post
title: "GitHub Pages and Google Domains"
date: 2016-01-10
categories: google-domains github github-pages
---

Transferred my `dnedveck.com` domain to Google Domains from Hostgator, and this gave me an excellent opportunity to switch my hosting from them as well. 

So setting up my website to be hosted on github.

I already have my domain with google domains.


made a repo dnedveck.github.io, pushed a simple html file to it.

Added a CNAME file to it with www.dnedveck.com in it


Thanks to [Christopher Kyle Horton](http://blog.christopherkylehorton.com/2015/01/setting-up-my-custom-domain-with-github.html) for help on figuring the next bits out. 

I went to google domains, under the DNS tab for my domain I went to custom resource records and added a CNAME record, the line that I added looks like:

		www	CNAME 	1H 	dnedveck.github.io.

(it automatically added a `.` at the end of the address)

so now I can type `www.dnedveck.com` into my address bar and I go to my github hosted site. 

but `dnedveck.com` does not work. so I added an A record (because it turns out I am interested in adding an apex domain, I guess).

I added another record in the custom resource records

		@	A 	1H	192.30.252.153
					192.30.252.154

Then using the dig command on my linux box to check to see if it is set up correctly

		dig dnedveck.com +nostats +nocomments +nocmd

and it returned the same IP Addresses. Navigating to `dnedveck.com` now redirects to `www.dnedveck.com`. Nice.

Now I'm going to set up a jekyll blog under a blog repo, and have that be at blog.dnedveck.com

Made a repo, pulled it down, made a gh-pages branch

		git checkout --orphan gh-pages

added a CNAME file for my desired subdomain

		echo "blog.dnedveck.com" >> CNAME

copied in a jekyll skeleton

pushed to github

added CNAME record on google domains (DNS Tab > Custom Resource Records)

		blog	CNAME	1H	dnedveck.github.io/blog

(and the DATA was modified to dnedveck.github.io/blog.dnedveck.com.) 
Since the DATA field was modified, I entered in `dnedveck.github.io/blog.`, and it was not modified from that.

I tried navigating to blog.dnedveck.com, and got an error that the name was not resolved. 

After reading the help docs, I think it didn't work beacause I'm not allowed to have a path in the DATA field.

So I can try a subdomain forward, under synthetic records, I selected a subdomain forward from the dropdown.

Still didn't work.
 
Saw a stack overflow answet that mentioned ["... I had to point the DNS only to my main github user name. The CNAME in the gh-page branch of user.github.com/project took care of the rest... "](http://stackoverflow.com/questions/26384498/custom-domain-for-github-project-pages)

So I added another custom resource record

		blog 	CNAME	1H	dnedveck.github.io

and now going to blog.dnedveck.com works. Whatever, the internet is magical.





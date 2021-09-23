# Introduction ([Web API Guide](../../README.md))
by [Charles Iliya Krempeaux](http://changelog.ca/)
-----

There are different ways one _could_ create a Web-based API — i.e., a HTTP or HTTPS based API — what I describe in this guide is, in general, how I recommend it is done.

## My History

I have been programming for what feels, to me, to be a long time.

I think the first time I did any programming was back in the early 1980s — back when I was in elementary school — writing programs in the _Logo programming language_.
These _Logo programs_ that I and others wrote would draw pictures using _turtle graphics_ — a _vector graphics_ API for the _Logo programming language_.
I think this was an after-school-hours class that you could sign up for — and (I assume) one of my parents signed me up for it.

To do this _Logo programming_ I used the computers they had at the elementary school I was attending at the time.
Back then it wasn't common for people to have computers at home.
So, for many children, if they were programming, it was often using a computer at their school.

So for me and many other children, the only time we would have a chance to do _Logo programming_ was using the computers at our elementary school as part of a computer class.

My mother actually volunteered to help teach Logo programming.
Although I don't think my mother had any programming experience before that, so I assume she picked it up just before teaching it.
So, at least back then, my mother was involved in teaching me how to program.
My father actually did have exposure to computers, teletype machines, and some low level programming — but, for whatever reason, he didn't get involved with teaching me how to program. Or at least, I don't recall him doing so. Although he was involved in my education in a number of other ways.

Later on when I was older and in high school, in either the late 1980s or early 1990s I did some programming in the BASIC programming language.
It was part of one of my high school classes — a class on computers.

To do this _BASIC programming_ I used the computers they had at the high school I was attending at the time.
Still, even then, it still wasn't common for people to have computers at home.
So, for many young adults in their teenage years, if they were programming, it was often using a computer at their school as part of a computer class.

A little later on, in the 1990s, after convincing my parents to buy a personal-computer (PC) for our home — a desktop-computer based on the old Intel 80486 CPU — I learned how to program on my own, by reading (physical) books and (physical) magazines.

This was _before_ the Internet and the Web became ubiquitous.
So if you wanted to learn something, you couldn't just go on the Internet or the Web to learn it — really, for most people, all you had were (physical) books and (physical) magazines.
And, for books, you had to find a bookstore that sold computer programming books — which wasn't always easy.

But when I got into programming this time, I didn't stop, because I finally had access to a computer that I could program on anytime I wanted — since it was a computer we had at home.
I kept on programming, more and more and more.

With this personal-computer (PC) I convinced my parents to get — at first, after learning how to use the DOS command-line shell, I learned how to program _DOS batch files_. After that got back in _BASIC programming_ by learning how to program in _QBasic_.

Eventually, while in university (despite, at the time, mathematics being my intended major) I started taking computer science courses for fun.

While in university, I both took more and more computer science courses, learning more and more programming languages, and programming topics.
But I also kept learning programming on my own.
I actually learned more on my own by reading (physical) books, reading (physical) magazines, and eventually by participating on Internet e-mail mailing lists, by participating on Usenet newsgroups, and by reading web-pages.

Eventually I graduated and had a career as a computer programmer.
(Although my career was non-typical. And I did a lot of things that computer programmers typically don't do.)

## API

“API” is an initialization — it is short for either **“application programming interface”** or **“application programmer interface”** depending on who you ask.

Nowadays, at the time I'm writing this, if you ask programmers:
> what is an “API” is?

I think many (maybe most) of them will just think of HTTP or HTTPS based APIs — i.e., Web-based APIs. I.e., things such as:

> `GET https://api.example.com/v1/toys`
> 
> `DELETE https://api.example.com/v1/toys/{id}`
> 
> `GET https://api.example.com/v1/toys/{id}`
> 
> `PATCH https://api.example.com/v1/toys/{id}`
> 
> `PUT https://api.example.com/v1/toys/{id}`

The sense I have right now is that — if the programmer is born in the 1990s or later, they are likely to think “API” just means HTTP or HTTPS based APIs — i.e., Web-based APIs

If you ask a programmer born before that they likely think of something different than that!
Yes, they would include Web-based APIs as APIs.
But they would also include other things as APIs too — such as libraries such as OpenGL, a Java programming language's class, a Go programming language's package, the Logo programming language's turtle graphics, Borland's Object Windows Library (OWL) for the C++ programming language, the JavaScript programming language's WebRTC, PHP programming language's ereg, etc.

**Remember — APIs existed _before_ HTTP, HTTPS, and the Web existed.**

Having said that, this guide is about Web-based APIs.
So even though not all APIs are Web-based, this guide will focus on Web-based APIs.

## World Wide Web

Today, at the time I am writing this, the Web is ubiquitous — it is everywhere!
And there are people alive today that do _not_ know a world with the Web.

Which to me is strange because not only wasn't the Web ubiquitous (yet) when I was young, but computers weren't ubiquitous (yet) when I was young.
Well, other than video game consoles — such as the Atari 2600, the ColecoVision, the Intellivision, the Nintendo Entertainment System (NES), the Sega Master System, etc — as well as various calculators.
But none of these are like the personal-computers, laptops, tablets, or mobile phones that are common today.

In the early days of the Web, it was called the **World Wide Web**.
This (“world wide web”) was often shortened: **“www”**.
Some might recognize this **“www”** initialization in many website Internet domains similar to `www.example.com`.

Back at the beginning of the Web, there were a lot of static HTML files.
The users of the Web back then did a lot of reading, but also did a lot of writing.
There was actually a flourishing of writing back then.

Another of the early popular user-cases for the Web seemed to be downloading and viewing images.
This is something that is simple today, but wasn't in the past.
Some of the web browsers of the time made it easy — you would click on a text-based link that pointed to an image, wait something like 10 to 30 minutes for the image to download, and then be able to see the image right in the web browser.
This was an improvement over the previous user-experience (UX) for downloading and viewing images — namely downloading images using FTP (often from the command-line shell), then trying to find another program that can view the image.

At some point in the 1990s and continuing in the 2000s, it seemed to become more and more common that normal people would have personal-computers (PCs) in their homes.
And with this, it became more and more common that normal people would use the Internet and the Web.
Although this is the Internet from the 1990s and 2000s, which is very different, in many ways, from the Internet of today.

## Web-based User Interfaces (UIs)

Before the 2000s, if someone was using an application, then it was (what today we might call) a “native-application”.
Although back then it would be a native-application running on DOS, or on the very early version of Microsoft Windows, or on Sun's NeWS (Network extensible Window System), or X Windows System (i.e., X11), on NeXTSTEP, on macOS, etc.

In the late 1990s and early 2000s Web-based user-interfaces (UIs) started to become common.
Prior to that the Web was more web-pages oriented, with static content.
In the late 1990s and early 2000s web-application became much more common.

Eventually Web-based user-interface (UIs) took over.
Most (new) applications _only_ had Web-based user-interfaces (UIs).
The Web won — and it became uncommon for programmers to create native-applications.

Although certain native-applications have made a come-back — today, at the time I am writing this, native-applications for mobile phones have become popular.
And have been displacing Web-based user-interface (UIs).

## Front-End Developers

Back in the 1990s it was common for software developers to do everything — they did (what later became known as) the back-end, they did (what later became known as) the front-end, they did the database, the did the servers. etc.
The label “full-stack developer” didn't exist back then, but they were full-stack developers plus a lot more!

These software developers would often work with a **graphics designer** — people who would draw (on a computer) what the user-interface (UI) of the web-application would look like.

They would provide that design to the software developer in the form of images.
The software developer would then (digitally) “cut” up these images into smaller images into usable parts, write some HTML code for the front-end.

Software developers tended to get paid more than graphic designers.
And as a result, it eventually became common to get the **graphic designer** to  “cut” up these images into smaller images into usable parts themselves, **and** to write the HTML code themselves.

This _graphics design_ plus _HTML_ skill set was the origin front-end developer.

Later when CSS became better supported in the web browsers of the day, and it became more accepted to use it, the skill-set of the **front-end developer** became: _graphics design_ plus _HTML_ plus _CSS_.

Some of these types of front-end developer learned a bit of basic JavaScript (after JavaScript got created) (but usually not to the level a software developer would understand it).
And some of these types of front-end developers learned a bit of very basic back-end development (but again, usually not to the level a software developer would understand it).

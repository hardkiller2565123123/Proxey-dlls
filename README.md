# Proxy-dlls

## About

I made this repository to talk about how I use DLLs and why I like them so much.

Proxy DLLs are really useful for me when I want to learn about software try out things and build new programs. They let me work with applications without changing the program and I can still add new features, tools to help me debug systems to log information or my own frameworks.

I do not just want to make something work I want to understand how it works behind the scenes. I want to find ways to build on top of what's already there without throwing it all away.

---

## Why I Use Proxy DLLs

I use proxy DLLs because they are a way to add my own code to a program without breaking the original software.

Of changing the main program a proxy DLL acts like a bridge between the program and the original library. This lets me start my code do some custom setup and then let the original DLL take over.

Over time I have found that this way is:

* easier to keep track of

* easier to update

* easier to debug

* less likely to cause problems

* flexible for different projects

Most importantly it lets me try new things without changing the original software.

---

## Why I Preserve Original Functionality

One thing that is different about my approach is that I try to keep much of the original functionality as I can.

When I make a proxy DLL I usually load the library and let the program work normally. My additions are meant to work alongside the code not replace it.

This is not always the way and it is not always the easiest but it is how I like to work.

I like knowing that:

* the original features still work

* the original behavior is still there

* the program is still compatible

* the original functionality is not removed

I think of proxy DLLs as additions, not replacements.

---

## A Personal Philosophy

I know some people might see this way of working as different especially when it comes to reverse engineering or modifying software.

My Goal is not to re-design the work of the original developers, nor to take over their software. I just want to learn, try things, research, preserve and build on what is already there.

The software should still be recognizable.

The original functionality should still be there.

My code should make the program better not replace it.

That is why I keep using proxy DLLs.

---

## Closing Thoughts

This repository is not a collection of tools or programs.

It is a small explanation of why I use proxy DLLs why I try to keep the original functionality and how I think about my projects.

I build things because I am curious, about how they work.

Proxy DLLs are just one way I like to explore that curiosity.

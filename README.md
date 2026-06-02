# Proxy-dlls

## About

This repository is simply a place to explain my approach to using proxy DLLs and why I've continued to use them throughout many of my projects.

Proxy DLLs have become one of my favorite techniques for learning, experimenting, and building software. They allow me to interact with applications in a way that feels less intrusive than directly modifying executables while still giving me the flexibility to add new functionality, debugging tools, logging systems, or custom frameworks.

For me, it's never just been about making something work. It's about understanding how software works behind the scenes and finding ways to build on top of existing systems without completely replacing them.

---

## Why I Use Proxy DLLs

I use proxy DLLs because they provide a simple and reliable way to introduce custom code into an application while allowing the original software to continue functioning as intended.

Instead of modifying an executable directly, a proxy DLL acts as a bridge between the application and the original library. This allows me to initialize my own code, perform custom setup, and then pass control back to the original DLL.

Over time I've found this approach to be:

* Easier to maintain
* Easier to update
* Easier to debug
* Less invasive than executable patching
* More flexible across different projects

Most importantly, it allows me to experiment without completely replacing the original software.

---

## Why I Preserve Original Functionality

One thing that separates my approach from many others is that I usually try to preserve as much of the original functionality as possible.

When I build a proxy DLL, I typically load the original library, forward its exports, and allow the software to continue operating normally. My additions are intended to exist alongside the original code rather than completely replacing it.

This isn't always the fastest approach, and it certainly isn't always the simplest, but it aligns with how I prefer to develop.

I like knowing that:

* Original features still work
* Original behavior is preserved
* Compatibility remains intact
* Existing functionality isn't unnecessarily removed

In many ways, I see proxy DLLs as extensions rather than replacements.

---

## A Personal Philosophy

I understand that some people may view this style of development differently, especially when it comes to reverse engineering, modification, or software research.

My goal has never been to erase the original work of developers or completely take control of someone else's software. Instead, my interest has always been in learning, experimenting, researching, preserving, and building upon existing systems.

The software should still be recognizable.

The original functionality should still be there.

My code should enhance the experience, not replace it.

That philosophy has influenced nearly every proxy DLL project I've worked on and remains the reason I continue using this approach today.

---

## Closing Thoughts

This repository isn't meant to be a framework, toolkit, or collection of releases.

It's simply a small explanation of why I use proxy DLLs, why I preserve original functionality whenever possible, and the mindset that guides many of my projects.

At the end of the day, I build things because I'm curious about how they work.

Proxy DLLs just happen to be one of my favorite ways to explore that curiosity.

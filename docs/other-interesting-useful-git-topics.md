---
layout: default
title: Useful Git Topics
nav_order: 11
---

# Useful Git Topics
{: .no_toc}

## Table of Contents
{: .no_toc }

1. TOC
{:toc}
## Helix4Git

This is a bridge between Perforce and Git. This is great for developers who have never worked with Perforce before, and artists work well with Perforce too, meaning both groups get the best of both worlds. But you should know there are no GitHub features here. This is just plain Git, so you’ll still have to relearn some things because you’re probably used to GitHub instead of just plain Git.

That’s okay though. Everything is still a learning experience in programming. You can’t know everything well, I think so. Maybe if you do know everything, you’re probably a god. And if that’s the case, I don’t know why you’re reading this, because you should be making some amazing technology that we can’t even think of.

---

### Why use this?

Git has a very tough time dealing with binary files. You can’t see what they look like because they’re just a bunch of binary to you, and sometimes they can cause conflicts inside your code if two people change the same thing.  

Perforce, however, lets you edit your scenes and lock them so other people can’t use them at the same time. Meanwhile, developers can still edit scripts and merge them together as they normally would.

With these two things combined, development becomes much easier for both sides. You don’t have to lock all the scripts, and Perforce can store all the big binary folders.

---

### Local or Cloud Setup

Keep in mind this all runs locally on your computer, just like Perforce does. Or, you can set up a server in the cloud. Either way, make sure you have a backup whether it’s a hard drive, RAID setup, or something else so you don’t lose anything.

---

### Why use this over Git LFS?

Git LFS costs money after a certain point, so it’s usually not an option if you’re a small indie studio, especially if you’re really small, like two to four people. Technically this program costs money too, but it’s free for up to five people.

---

### Final Thoughts

Personally, I haven’t tried it yet. I still have to set it up on a server, but I’ve done the research, and the benefits look great. I just need to try the workflow myself to see how good it actually is.

I hope this convinces you to give it a try. Based on my research, it looks very promising. It’s also nice to have things run locally on your own hardware instead of relying on the cloud, because this way it feels more like your own data instead of someone else’s.

---

I hope you give it a try. I’m out.

## References
- [Helix for Git PDF Manual (Perforce)](ftp.perforce.com/perforce/r17.1/doc/manuals/helix-for-git.pdf#:~:text=n%20stores%20Git%20repos%20in,a%20combination%20of%20cached%20data%C2%A0%C2%A0and)  
- [Working with Git in Helix Core (Perforce Docs)](https://help.perforce.com/helix-core/server-apps/p4sag/current/Content/P4SAG/working-with-git.html#:~:text=The%20Git%20Connector%20enables%20you,of%20the%20P4%20Server)  
- [Git vs Perforce: How to Choose and When to Use Both (Perforce Blog)](https://www.perforce.com/blog/vcs/git-vs-perforce-how-choose-and-when-use-both#:~:text=You%20can%20add%20P4%20Git,also%20supports%20Git%20LFS%20artifacts)  
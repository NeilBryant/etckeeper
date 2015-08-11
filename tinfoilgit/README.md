This is a security 'addon' for etckeeper.

The point is that evrybody isn't a server admin, and some people are going to want to put their repo online.

This is not a good idea.

But we're going to do it, anyway.

And if we're going to do it, it might as well be as safe as possible. So if you do push online, only do so to a secure private repo. Definitely don't push it to github or anything public.

Or; do what you want. I'm not your mother. This sentiment also sums up the liability of this add-on. If you use it, people are probably going to break into your machine. Your use therefore acknowledges your acceptance and welcome of such events.

## Usage

Drop the .gitignore file into /etc before installing etckeeper. That's basically it.

I've aimed to make the rules as secure as possible--and with git, it's easy enough to remove files from .gitignore, and add them into the repo. Doing the opposite, however, is a bit of a challenge.

So if you want to add anything to the repos, just remove/comment it out, and do a standard git add/commit.

## Versions

Currently, there is only one version. For git.

## Security

There are two parts here; secure and tinfoil-hat.

1. Secure is the basics. It ignores all of the passwd files (that I've found), plus things like ssh hash files. It also has a few more extraneous and binary files than stock etckeeper (eg, X11/X).

2. Tinfoil Hat is more serious. It ignores things that might possibly be attack verctors. At the time of this writing, that means the PAM modules. Can anybody work out how to break your system knowing your pam configurations? Maybe, maybe not. But there are some clever people out there, so why not be safe.

Tinfoil Hat is probably overkill for most people. Who even changes those files? And if you don't change them, then they're stock, so everybody has them, anyway.

And if you use etckeeper as it's intended, and only push to local repos, then all of this is overkill (except for the added binaries, etc).

This is also an early version--although possibly the only one--of this addon. I've done a quick search for things, but I've also certainly missed some (cf, "not your mother").
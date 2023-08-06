---
title: Forum Permission System
---

The forum permission system in Cirrusboard is fairly simple. Each forum has three permission settings, which are the following:

- Who can view (`minread`)
- Who can make threads (`minthread`)
- Who can reply (`minreply`)

If `minread` is Member or above, the forum will be labelled "(private)" in order to signify to users that the forum is not accessible to logged out users.

Using these settings, you can control who can read or make posts in a forum. Some examples:

**Members-only forum**
- `minread`: Member
- `minthread`: Member
- `minreply`: Member

**Announcements forum**
- `minread`: Banned
- `minthread`: Admin/moderator
- `minreply`: Member

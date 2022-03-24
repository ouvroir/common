# Zotero (documentation) 



## Auto-hébergement

[adamsmith](https://forums.zotero.org/profile/2433/adamsmith) répond aux questions sur le forum

### Forum

#### how to use Zotero on local network with database ? 

[April 17, 2016](https://forums.zotero.org/discussion/58521/how-to-use-zotero-on-local-network-with-database)

- 2017: I do not see any documentation about self-hosting a Zotero server. Do you know if there is one ?       
- Nothing currently useful, no (all existing  documentation is outdated). Zotero makes the code available but doesn't  provide any support for self-hosted servers. The code is here: https://github.com/zotero/dataserver a Docker package is planned, but no ETA.                        

#### Put a group into lokal Storage on my own Server and not on the zotero Server 

[September 12, 2018](https://forums.zotero.org/discussion/73571/put-a-group-into-lokal-storage-on-my-own-server-and-not-on-the-zotero-server)

- You can set up a local dataserver that replaces Zotero for all syncing activity -- the code is all open: https://github.com/zotero/dataserver -- but there aren't currently good instructions or support available  for this, so you'd be mostly on your own.                        

#### Zotero self-hosted 

[September 21, 2018](https://forums.zotero.org/discussion/73721/zotero-self-hosted)

- ghjs123: We are very interested in having our own self-hosted Zotero. 
  Based on the posts underneath and the two projects on Github I was wondering  what the current status is of these projects is. Would one of the two be the (official?) Docker-version which adamsmith is referring to?<!--c.f. above-->
- kratsching: (September 24, 2021)
  As it is fall 2021 an no answer was given in spring 2019 - i'd like to re-ask the question. 
- adamsmith(September 24, 2021)
  There are no updates on this. **Anything official would be easy to spot on Zotero's GitHub**.
  https://github.com/ZotPrime/zotprime is the best maintained community option              

### Repos

#### mrtcode/zotero-server

mrtcode : travaille chez Zotero? Contribue au code des repos Zotero

- FWIW, mrtcode works for Zotero, so what you see on his repo is either a  Zotero developer trying this out because they're curious, or an early  attempt from Zotero. I'd give that version a shot ([adamsmith sept 2018](https://forums.zotero.org/discussion/comment/316870/#Comment_316870))   
- repo n'existe plus. le contacter pour demander pourquoi il l'a supprimé? (git.martynas@gmail.com)
- il fait des trucs pas mal aussi
  - https://markdowntree.com/
  - https://www.octopusnote.com/

#### gfacciol/zotero_dataserver-docker

- last update may 2019
- Look at https://github.com/SamuelHassine/zotero-prime which is more frequently maintained than this repo

#### [ZotPrime](https://www.zotprime.io/en/)

https://github.com/ZotPrime/zotprime

- ZotPrime is a full packaged repository aimed to make on-premise [Zotero](https://www.zotero.org) deployment easier with the last versions of both Zotero client and  server. This is the result of sleepness nights spent to deploy Zotero  within my organization on a disconnected network. Feel free to open  issues or pull requests if you did not manage to use it.
- last update april 2021
- mêmes contributeurs que zotero dont mrtcode & dstillman

##### Issues

- still maintained? (dec 2021)

> [@danielnbalasoiu](https://github.com/danielnbalasoiu), from my experience I know setting up successfully an own instance of  zotero is pretty challenging. Additionally, the focus of the zotero  developers is the cloud version and, therefore, any solution like  zotero-prime is most likely a community contributed 3rd party niche  offer without any funding behind. However, keeping up with the latest  versions needs efforts which aren't valuable for anyone who already has a running version.
>
> TL;DR: I wouldn't expect much updates here. Except  community contributed fixes in forks of this repository or in the issues of this repository.

#### zotero/dataserver

Official zotero data server 

- no clear documentation
- last modified 18 days ago 

##### Issues

- [issue](https://github.com/zotero/dataserver/issues/105) `self hosting documentation` since sept 2020

  - dstillman

    > This isn't a documentation issue — it's a technical and resource one.  Creating a version that's easy to self-host would just be a completely  different project from running a hosted service for millions of users on a sprawling AWS infrastructure with countless services, databases,  database shards, caches, search clusters, Lambdas, etc., and all the  processes for deploying, debugging, upgrading, and monitoring it, not to mention managing compatibility across different versions of Zotero  clients, would be completely different. We still do hope to make a more  easily self-hostable version at some point, but for now our priority is  maintaining the service for Zotero users. (30 sept 2020) 

    > Just to be totally clear, though, this isn't something  that just needs time allocated once and then would be fixed. It would  need to be a permanent, ongoing effort to keep a self-hostable version  current. We try to document necessary changes in commit messages, with  scripts for DB upgrade steps, notes about new dependencies, etc., but  any sort of update to a self-hosted version would just require a totally different process from what we do internally.
    >
    > It'd be relatively feasible to build a container-based  version of the server environment — we've experimented with that in the  past — but once there are users and existing data, keeping it working  and current and compatible with Zotero clients is a much more difficult  proposition. (4 octobre 2020)

  - edgimar

    > It seems that what Zotero needs is a stable,  well-documented API for the data-server.  Honestly, in order to do good  development, this API is probably already documented somewhere.  Unless  I'm mistaken, however, ~~this API doesn't appear to be publicly available (the APIs published [here](https://www.zotero.org/support/dev/start) are only for read-only access to data on the server).~~  **Correction: the API does support read/write operations.**
    >
    > With the full API publicly available, then anyone can  choose to implement a data-server however they wish, so long as it  complies with the API. (13 dec 2020)





## FileSync

[Zotero file Syncing options](https://www.zotero.org/support/preferences/sync#file_syncing)

### Zotero Storage

Zotero Storage is the recommended file sync option. It has several  advantages over WebDAV syncing, including syncing of files in [group libraries](https://www.zotero.org/support/groups), web-based access to PDFs and other attachments, easier setup,  guaranteed compatibility, and improved upload performance for certain  files. Each Zotero user is given 300 MB of free Zotero Storage for  attached files, with [larger storage plans](https://www.zotero.org/support/storage#storage_pricing) available for purchase.

See the [Zotero Storage](https://www.zotero.org/support/storage) documentation for more information.

**Attention! ** Only Zotero File Storage is supported for group libraries.

### WebDAV

WebDAV is a standard protocol for transferring files over the web, and  it can be used to sync files in your personal library. (Group libraries  cannot use WebDAV.) Your employer or research institution may be able to provide WebDAV storage. Otherwise, there are many third-party options,  both free and paid (see [WebDAV providers known to work with Zotero](https://www.zotero.org/support/kb/webdav_services)).

Once you have your WebDAV account info, enter the URL provided by the service, your username, and your password in the [Sync preferences tab](https://www.zotero.org/support/preferences/sync#file_syncing). Be sure to select 'http' or 'https' as appropriate — if you're not  sure, try 'https' first. After entering the information, click “Verify  Server”. If Zotero successfully verifies the WebDAV account, you're all  set to use file syncing via WebDAV.

Zotero file sync should work with any correctly functioning WebDAV  server. Zotero developers cannot provide support for third-party WebDAV  servers.

### Linked files

With linked files, Zotero only stores a link to the location of the  original file on your computer. Linked files are not synced, nor are  they deleted if the attachment item is deleted in Zotero. They also  can't be used within a group library, as there's no guarantee that other group members would have access to the same file location

### Linked file attachements

you can [attach links to files](https://www.zotero.org/support/attaching_files#linked_files) stored in a cloud-sync folder, such as  Dropbox or Google Drive. When using linked attachments, you should set  up Zotero's [Linked Attachment Base Directory](https://www.zotero.org/support/preferences/advanced#linked_attachment_base_directory) feature so that Zotero can find your files on each computer, even if the path to the cloud-sync folder differs

## Groups

[Groups](https://www.zotero.org/support/groups): There is no limit on how many members may join your groups, and your  full storage subscription is always available to your personal and group libraries.

### Group Types

#### Private Groups

-  Private groups provide a means of **collaboration among group members without creating any public face for the group online**. Only group members and users invited to join the group are able to see the group’s page.
-  Private groups are completely hidden from group searches. They are not shown on members’ public profile  pages and will not appear in search engine results.
-  **If administrators enable file sharing, **group** members can access and share files in addition to references.**

#### Public, Closed Membership

-  Closed-membership groups are useful  for creating a **controlled group environment with a public presence**. This allows a group to publicly present its work and sources, or develop new membership in a controlled fashion.  Anyone can view the group page, but the only way to join the group is by invitation or by requesting an invitation.
-  If the group has a library, administrators can choose to show or hide the library from non-members.
-  If administrators enable file sharing, group members can access and share files in addition to references.

#### Public, Open Membership

-  Open public groups are useful for the broadest discussion and collaboration.  The group page is public, and anyone who wants to can join instantly.
-  If the group has a library, administrators can choose to show or hide the library from non-members.
-  **Open public groups do not allow file sharing**.

### Group settings

- Profile settings: 
  - group name, description, enable/disable comments
  - To transfer group ownership to another user, use the “Transfer Ownership” option from this page. Only the group owner can initiate tranfering ownership. If the member offered accepts ownership, they will become the new group owner (and any group file storage will start to  count against their storage quota).
  - If group file storage is enabled, it will count against the owner's  storage quota. Other group members' storage quotas will not be affected  by the group files.
  - If this is a group for a team, lab, or organization, we recommend  setting up a separate account for the team to function as the owner of  the group, with at least two people knowing the login information. This  way, you will not be locked out of the group if the group owner were to  leave the team or organization.

### Library settings

- libary reading
- library editing
- file editing

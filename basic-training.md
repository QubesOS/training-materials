# Materials

* post-it notes
* markers
* large paper
* projector & Qubes laptop & appropriate connector

# Time
time listed assumes 1 hour training / workshop

# Learning Goals
* understand what Qubes OS is
* understand and apply the concept of domains
* understand strategies for identity management in Qubes OS
* understand strategies for malware protection in Qubes OS

*note*: understanding of Tor and VPNs, common vectors of malware (email, USB, websites) are all very helpful towards using and understanding Qubes OS.

*Prepare*: You should load the relevant domains for **Show: Malware Protection** in one workspace and **Show: Indentity Management** in a second workplace, so that you can easily switch between them.

# Introduction to the training
*2 min*

Introduce the trainers and present the course of the workshop:
  1. brief introduction to Qubes
  2. introduction of domain mapping
  3. application of domain mapping & discussion
  4. synthesis & questions

# Input: Introduction to Qubes
*15 min*

* distribution of Xen the hypervisor
* userland is Debian, Fedora, Whonix, Windows 7
* "security by compartmentalization" -> safe integration
* **Show:** Qubes VM Manager with View NetVM enabled to see qubes with different Templates, Networking, Colors
  * use different colors for qubes to help you manage domains

## Show: malware protection

* disposable VMs
  - for reading untrusted attachments and files
  - editing and saving untrusted .doc
  - for visiting untrusted website (can also use Tor Browser)
  - **Show:** Open PDF in Disposable VM
* **Show:** split-gpg with private key notification
* **Show:** secure copy-and-paste with keepassx and web browser
* **Show:** untrusted PDF converter
* isolate less-trusted, large attack-surface programs (Pidgin, Thunderbird, Firefox)
* firmware protections
  * describe wifi, usb stack isolation (**Show:** Qubes VM Manager)
  * **Show:** plugging in USB, assigning to qube
  * anti-evil-maid, crossing borders / staying in hotels

## Show: identity management 

* compartmentalization also allow for robust management of networking and identities
  * Whonix integration
  * run VPN at same time
  * have non-networked/airgapped qubes (like for keepassx)
  * **Show:** Tor Browser, torified Chromium browser, VPNed Chromium browser, non-networked keepassx instance (open terminal in same qube and run `ping 8.8.8.8`)
* use different colors for qubes to help you manage them

## optional: brief Q&A
*2 min*

this can be a brief opportunity for folks to ask clarifying questions, but you need to strongly triage questions to not go down rabbit holes.

# Activity: Introduction to Domains

## Trainer shows
*10 min*

Trainer walks through partitioning their life domains -- personal, activism, work, banking, shopping, vault, etc. 

## Participants do initial mapping
*10 min*

Participants are then asked to split into groups of two and write down their activities onto post-it notes.

*Note*: we have no interest in you sharing confidential information about your life. This exercise is for you, so feel free to draw pictures or use code words to refer to activities you would prefer not to share with others.

## Participants group activities in domains
*10 min*

Now have participants group their activities in domains based on:

1. shared identity between those activities (work domain for example)
2. assets you want to protect (password domain for example)
3. high-risk activities (untrusted web browsing for example)

and talk through the domains they created with their partners. This section can be combined with the initial mapping if you feel appropriate.

## Participants share with group
*5 min*

Come back together as one group, as group if anyone would like to share any thoughts or "a-ha"s they had doing the mapping of domains for themselves or discussing with their partners.

## Close
*2 min*

Note that domain mapping is:
* useful outside of Qubes context
* the hardest part for new Qubes users to figure out (although Qubes provides some defaults for users: `personal`, `vault`, `work`, `untrusted`)

##Rootkits


Windows Rootkits(excellent writeup/introduction to windows rootkits)
* [Part 1](http://www.programdevelop.com/5408113/)
* [Part 2](http://www.programdevelop.com/5409574/)
* [Part 3](http://www.programdevelop.com/5408212/)


TOC

Cull

* [Developing](#dev)
* [Identifying/Defending](#id)
* [Writeups](#writeups)
* [Tools](#tools)
* [Talks & Videos](#talks)
* [Papers](#papers)


###Cull

[Killing Rootkits](http://blog.ioactive.com/2014/09/killing-rootkit.html)

https://github.com/rrbranco/Troopers2015	




* Many people do not realize the real danger from rootkit technology. One reason for this is probably that publicly available rootkits for Windows OS are relatively easy to detect by conventional methods (i.e.memoryscanningbased). However, we can imagine some techniques of rootkit implementation, which will be undetectable by these methods, even if the rootkit concept will be publicly available. 000In order to convince people that traditional rootkit detection is insufficient it would be desirable to have a working rootkit implementing such sophisticated technology. Besides, it would be fun.

http://www.phrack.com/papers/revisiting-mac-os-x-kernel-rootkits.html

http://www.phrack.org/issues/68/6.html

http://phrack.org/issues/65/4.html#article

http://phrack.org/issues/61/14.html

http://phrack.org/issues/58/7.html
http://phrack.org/issues/62/12.html

Thunderstrike is the name for the Apple EFI firmware security vulnerability that allows a malicious Thunderbolt device to flash untrusted code to the boot ROM
[Homesite](https://trmm.net/EFI)
[Talk at CCC31](https://www.youtube.com/watch?v=5BrdX7VdOr0)



###<a name="dev">Developing</a>
[Android Rootkit](https://github.com/hiteshd/Android-Rootkit)
[Masochist](https://github.com/squiffy/Masochist)
* Masochist is a framework for creating XNU based rootkits. Very useful in OS X and iOS security research.

[Using Kernel Rootkits to conceal infected MBR](https://github.com/MalwareTech/FakeMBR/)
[Hypervisor](https://github.com/ainfosec/more)
[Suterusu](https://github.com/mncoppola/suterusu)




###<a name="id">Identifiying/Defending</a>

[Killing Rootkits](http://blog.ioactive.com/2014/09/killing-rootkit.html)

###<a name="writeups">Writeups</a>
[Shadow Walker - Raising the Bar for Rootkit detection - BH 2005](https://www.blackhat.com/presentations/bh-jp-05/bh-jp-05-sparks-butler.pdf)

[Rise of the dual architecture usermode rootkit](http://www.malwaretech.com/2013/06/rise-of-dual-architecture-usermode.html)
[Killing the Rootkit - Shane Macaulay](http://blog.ioactive.com/2014/09/killing-rootkit.html)
* Cross-platform, cross-architecture DKOM detection
[Raising The Bar For Windows Rootkit Detection - Phrack](http://www.phrack.org/issues/63/8.html)
[TLB Synchronization (Split TLB)](http://uninformed.org/index.cgi?v=6&a=1&p=21)
[Komodia Rootkit Writeupn](https://gist.github.com/Wack0/f865ef369eb8c23ee028)
* Komodia rootkit findings by @TheWack0lian

[Using Kernel Rootkits to conceal infected MBR](http://www.malwaretech.com/2015/01/using-kernel-rootkits-to-conceal.html)

[MoRE Shadow Walker : TLB - splitting on Modern x86](https://www.blackhat.com/docs/us-14/materials/us-14-Torrey-MoRE-Shadow-Walker-The-Progression-Of-TLB-Splitting-On-x86-WP.pdf)
* MoRE, or Measurement of Running Executables, was a DARPA Cyber Fast Track effort to study the feasibility of utilizi ng x86 translation look - aside buffer (TLB) splitting techniques for realizing periodic measurements of running and dynamically changing applications. It built upon PaX, which used TLB splitting to emulate the no - execute bit and Shadow Walker, a memory hidi ng rootkit ; both designed for earlier processor architectures. MoRE and MoRE Shadow Walker are a defensive TLB splitting system and a prototype memory hiding rootkit for the current Intel i - series processors respectively � demonstrating the evolution of th e x86 architecture and how its complexity allows software to effect the apparent hardware architecture.

[Smart TV Security - #1984 in 21 st century](https://cansecwest.com/slides/2013/SmartTV%20Security.pdf)
* This talk is more about security bugs and rootkits than about firmware for TVs. This talk more covers rootkits than security bugs and exploitation thereof, as they�re not different to traditional techniques. This talk is about general security issues of all Smart TV vendors.

[Advanced Bootkit Techniques on Android](http://www.syscan360.org/slides/2014_EN_AdvancedBootkitTechniquesOnAndroid_ChenZhangqiShendi.pdf)

###<a name="tools">Tools</a>

[UEFITool](https://github.com/LongSoft/UEFITool)
* UEFITool is a cross-platform C++/Qt program for parsing, extracting and modifying UEFI firmware images. It supports parsing of full BIOS images starting with the flash descriptor or any binary files containing UEFI volumes.

###<a name="talks">Talks/Videos</a>
[BoutiqueKit: Playing WarGames with Expensive Rootkits and Malware- Defcon 21](https://www.youtube.com/watch?v=gKUleWyfut0)


[Persistent, Stealthy, Remote-controlled Dedicated Hardware Malware [30c3]](https://www.youtube.com/watch?v=Ck8bIjAUJgE)

[Intel Management Engine Secrets by Igor Skochinsky](https://www.youtube.com/watch?v=Y2_-VXz9E-w)

[MoRE Shadow Walker : TLB - splitting on Modern x86](https://www.youtube.com/watch?v=XU1uNGZ7HnY)
* This presentation provides a cohesive overview of the work performed by AIS, Inc. on the DARPA CFT MoRE effort. MoRE was a 4-month effort which examined the feasibility of utilizing TLB splitting as a mechanism for periodic measurement of dynamically changing binaries. The effort created a proof-of-concept system to split the TLB for target applications, allowing dynamic applications to be measured and can detect code corruption with low performance overhead.

[How Many Million BIOSes Would you Like to Infect?](http://conference.hitb.org/hitbsecconf2015ams/sessions/how-many-million-bioses-would-you-like-to-infect/)
* This talk is going to be all about how the automation of BIOS vulnerability exploitation and leveraging of built-in capabilities can yield highly portable UEFI firmware malware. And how millions of systems will be vulnerable for years, because no one cares enough to patch the BIOS bugs we�ve found.  So you think you�re doing OPSEC right, right? You�re going to crazy lengths to protect yourself, reinstalling your main OS every month, or using a privacy-conscious live DVD like TAILS. Guess what? BIOS malware doesn�t care! BIOS malware doesn�t give a shit

[Measurement of Running Executables](http://vimeo.com/81335517)

[From Kernel to VM](https://www.youtube.com/watch?v=FSw8Ff1SFLM)
* Description from stormeh on reddit(https://www.reddit.com/r/rootkit/comments/25hsc4/jacob_i_torrey_from_kernel_to_vmm/): Although it's not directly a lecture about rootkit development, the topics discussed are very much of interest: hardware virtualization, page table and TLB manipulation, hypervisors and privilege levels below ring 0, etc. The speaker does also go on to mention how prior rootkits such as Blue Pill and Shadow Walker leveraged these features, as well as defensive technologies such as PaX. 
* [Slides](http://jacobtorrey.com/VMMLecture.pdf)

[All Your Boot Are Belong To Us - Intel Security](https://cansecwest.com/slides/2014/AllYourBoot_csw14-intel-final.pdf)
[Concepts for the Steal the Windows Rootkit (The Chameleon Project)Joanna Rutkowska2003](http://repo.hackerzvoice.net/depot_madchat/vxdevl/avtech/Concepts%20for%20the%20Stealth%20Windows%20Rootkit%20%28The%20Chameleon%20Project%29.pdf)\



###<a name="papers">Papers</a>
[A Catalog of Windows Local Kernel-mode Backdoors](http://uninformed.org/?v=all&a=35&t=sumry)
* This paper presents a detailed catalog of techniques that can be used to create local kernel-mode backdoors on Windows. These techniques include function trampolines, descriptor table hooks, model-specific register hooks, page table modifications, as well as others that have not previously been described. The majority of these techniques have been publicly known far in advance of this paper. However, at the time of this writing, there appears to be no detailed single point of reference for many of them. The intention of this paper is to provide a solid understanding on the subject of local kernel-mode backdoors. This understanding is necessary in order to encourage the thoughtful discussion of potential countermeasures and perceived advancements. In the vein of countermeasures, some additional thoughts are given to the common misconception that PatchGuard, in its current design, can be used to prevent kernel-mode rootkits.



[Implementation and Implications of a Stealth Hard-Drive Backdoor](https://www.ibr.cs.tu-bs.de/users/kurmus/papers/acsac13.pdf) 
* Modern workstations and servers implicitly trust hard disks to act as well-behaved block devices. This paper analyzes the catastrophic loss of security that occurs when hard disks are not trustworthy. First, we show that it is possible to compromise the firmware of a commercial o-the-shelf hard drive, by resorting only to public information and reverse engineering. Using such a compromised firmware, we present a stealth rootkit that replaces arbitrary blocks from the disk while they are written, providing a data replacement back- door . The measured performance overhead of the compromised disk drive is less than 1% compared with a normal, non-malicious disk drive. We then demonstrate that a re- mote attacker can even establish a communication channel with a compromised disk to infiltrate commands and to ex-filtrate data. In our example, this channel is established over the Internet to an unmodified web server that relies on the compromised drive for its storage, passing through the original webserver, database server, database storage engine, filesystem driver, and block device driver. Additional experiments, performed in an emulated disk-drive environment, could automatically extract sensitive data such as /etc/shadow (or a secret key le) in less than a minute. This paper claims that the diffculty of implementing such an at- tack is not limited to the area of government cyber-warfare; rather, it is well within the reach of moderately funded criminals, botnet herders and academic researchers.


[futo](http://uninformed.org/?v=all&a=17&t=sumry)
* Since the introduction of FU, the rootkit world has moved away from implementing system hooks to hide their presence. Because of this change in offense, a new defense had to be developed. The new algorithms used by rootkit detectors, such as BlackLight, attempt to find what the rootkit is hiding instead of simply detecting the presence of the rootkit's hooks. This paper will discuss an algorithm that is used by both Blacklight and IceSword to detect hidden processes. This paper will also document current weaknesses in the rootkit detection field and introduce a more complete stealth technique implemented as a prototype in FUTo. 
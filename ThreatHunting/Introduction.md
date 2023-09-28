Start date : 28/09/2023 20:55
# Threat hunting : Introduction

## Objectives

- Threat hunting as a structured concept.
- Relation to Incident response.
- The mindset
- General objectives of threat hunting
- How does threat hunting help the organizations security posture
- Data driven intelligence 

### So what is it ??

At a basic form threat hunting is the process of finding security threats by actively looking for them in the form of IoC's (indecators of compromise). However, that being said the above definition does not do it any just for the complexity that can come along with the technical aspects and larger picture it plays in the security posture of an organisation.

## It's Proactive ! But how does it compare to Incident Response (IR

The words "Threat Hunting" may sound like the first part of any response to an threat/incident whereas in reality it is normally done when IR is established and understood. This is largely due to the fact that threat hunting addresses the issue of **not waiting for threats to happen** (A major thought in a security teams mind)

[Mokmokmok](https://tryhackme.com/p/Mokmokmok) the author of the [Intro to Threat hunting room](https://tryhackme.com/room/introductiontothreathunting) summarises the differences between IR and threat hunting perfectly in this simple table:


|Reactive Approach	| Proactive Approach|
|---|---|
|Incident Response|	Threat Hunting|
|Triggered by an initial notification / alert	|Active search for suspicious| events that can become incidents|
|Guided by the initial scope of the incident	|Guided by Threat Intelligence|
|"There's a threat that needs to be dealt with now."	|"There might be a threat that we don't know yet."|

Additionally, [Mokmokmok](https://tryhackme.com/p/Mokmokmok)  uses this awesome flowchart to show that even though the two are **inherintly different** they can achieve a common goal **improving a organisations security posture**

![6a261c19e85bd2df416c81da97b8ea8a.png](:/2a3c5d9a9a1d4aeb85987b56db3f9089)

# All about the mindset

If the blue team mentality is to think like a hacker to stop a hacker, does that mean that we need to think like a threat to hunt for threats ?? (Kind of confusing). Luckily the answer is not really !  the **Basis of our mindset** is to start with a strong set of leads such as accurate pieces of information, some good examples include:
1. Threat intelligence sources (CTi)
2. IoC feeds
3. MISP
4. STIX
5. The list can go on and on ...

Through these strong feeds we can go as advanced as watching adversaries operating in our sectores and securing ourselves against their common attack patters and toolsets to targeting quicker wins by hunting down malicous binaries. [LOLBAS](https://lolbas-project.github.io/) is an awesome resource for this !

Below is a table of some free and some *very* expensive propriatary tools:

|General Hunting Guide|Examples|
|---|---|
|Unique Threat intelligence|IoC's|
|Threat Intelligence Feeds|[MSIP](https://tryhackme.com/room/misp) <br> [Recorded Future](https://www.recordedfuture.com/)<br>[Cognyte Luminar](https://www.cognyte.com/cyber-threat-discovery/cyber-threat-intelligence/)|

<br>

# We've got the mindset, now the Process

To begin we first need to know what we are hunting for and unfortunatley this is the question no blog or learning resource can fully answer for you as you need to evaluate your organisations security posture to determine where your cyber risks are high and then base your direction off the back of that (Perhaps a nicely prioritised list with risk ratings)

There are however some common area's that we can all start with that can provide meaningful actionable results. Below is a list of area's to start with and some resources or tips one can follow:

- Know relevant Malware
	- [The Zoo - Repo of live mawlare samples ](https://github.com/ytisf/theZoo)
	- [Trend Micro's Threat Encylopedia](https://www.trendmicro.com/vinfo/us/threat-encyclopedia/)
- Attack Residues
	- Being attacked is not great, learning from it is.
	- You need to know your enviroment well enought to tell normal artifacts apart from attack residue
- Known Vulnerabilities of in use products
	- Attackers love a good misconfiguration or vulnerability.
	- Scan, Identify, prioritise and patch !

## So how do we HUNT !

That is a broad question with a length answer, at this stage a summary can be given in short simple bullet points:

- IoC's (CTI feeds can provide these, or you can generate your own)
- Logical queries (Tools like Yara can help you hunt down those IoC's - ["Shameless plug" to one of my Repos](https://github.com/JayP232/DynamicRedlineYaraScan))
- Patterns of activity (Mitre Att&ck)

# Practical method of starting and visualing

For this I would reccomended reading through section 5 of the TryHackMe room, here is the [link](https://tryhackme.com/room/introductiontothreathunting) it essentially uses [Att&clk Navitgator](https://mitre-attack.github.io/attack-navigator/) which as awesome resource !

Example screenshot below:
![aa40f7f1950d92eea319f204adb7bcfb.png](:/705496d91c2a4daa895643eea4ce17cf)

End date: 28/09/2023 22:09

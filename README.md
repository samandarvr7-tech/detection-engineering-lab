# Detection Engineering LAB

In this LAB I will be simulating `detection engineering` by `building` my own environment, `exploiting` it, and `defending` from the attack.

## The Overview of the Plan for this LAB

*   First of all, we will start with `DVWA` and `Suricata`. We will open a droplet in Digital Ocean and deploy `Suricata` and `DVWA` there. We will set `DVWA` to the low level; since we are mainly focusing on detection, we will not be doing advanced attacks. After successfully exploiting `DVWA`, we will use `Suricata` logs to analyze packets, find `patterns` of an exploitation, and `write a rule` for further prevention of attacks.

*   The next step will be learning `EDR`. For this, we will use `Wazuh SIEM` with `AD` and a `Windows` host. The cycle of an attack and defense will be the same as in the first phase. After completing Wazuh, we will add Zeek to our stack for behavioral analysis.

*   Finally, after getting to know all tools that allow us to see attacks from all possible angles, we will start doing something more serious. There is a website which publishes real `PCAPs` of real exploitations: `malwaretrafficanalysis.net`. We will use those `PCAPs` in our lab to do the same: analyze `patterns` and `write rules` for prevention.

*   Another resource for imitation of real attacks is `ART (ATOMIC RED TEAM)`, which contains `scripts of real attacks`. This will also help us to `imitate attacks` on our lab so we can log them, analyze `patterns`, and `write a rule`.

*   Also, I consider taking real `CVEs` of enterprise apps (for example `Jira`), the old CVEs of course, so we can deploy that exact `vulnerable version` of the app, `exploit` it, and do our `detection`.

*   The ultimate `GOAL` for this lab is eventually to start taking new `CVEs`, testing them in the lab, `writing rules` for their prevention, and posting on `SOC Prime`.

## How it started

Initially, I was an `Intern` as a `Sysadmin`, and luckily my mentors provided me with resources such as a Mikrotik Router, Netgear Switch, and DELL server. I built a topology imitating real corporate ones. My server was placed between the Router and Switch so it would be in `inline mode`, and `Suricata` could `drop` the `malicious packets`. 

Eventually, I completed what I wanted to do, but after the internship, I no longer had resources and decided to `rebuild` it on the `cloud`, since I had free `credits` from the `Github student pack`. And that's how it started. Eventually, I started to learn about other tools like `SIEM` systems, `EDR/XDR`, and coming up with new ideas for upgrading my lab and enhancing my skills.
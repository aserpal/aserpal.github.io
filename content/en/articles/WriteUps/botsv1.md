---
title: "Boss of the SOC v1"
date: 2023-04-29
draft: false
---

# Introduction

Hi everyone. This will be a simple post about how to solve Splunk's Boss of the SOC v1 CTF. This was my first Splunk CTF.  
You can find it in [Cyberdefenders](https://cyberdefenders.org/blueteam-ctf-challenges/15#nav-questions). You will need to sign in to download the challenge.

## Details

Virtualbox: unzip the VM (pass: cyberdefenders.org), start VM, and access Splunk from host machine via http://127.0.0.1:8000  

SHA1SUM: 89719952101ffdf7ee577aaed9a5f6c98934b812  

Size: 1.9 GB  

VMware: login to the VM using vagrant/vagrant and grab the IP address of the VM using "IP address" command. Access Splunk from the host machine using the IP address assigned to the VM via http://x.x.x.x:8000  

Challenge Files:
bots1.ova (Memory: 4 GB, CPU: 2 Cores, Disk: 5.5 GB)

## Scenario 1 (APT)

The focus of this hands on lab will be an APT scenario and a ransomware scenario. You assume the persona of Alice Bluebird, the analyst who has recently been hired to protect and defend Wayne Enterprises against various forms of cyberattack.

In this scenario, reports of the below graphic come in from your user community when they visit the Wayne Enterprises website, and some of the reports reference "P01s0n1vy." In case you are unaware, P01s0n1vy is an APT group that has targeted Wayne Enterprises. Your goal, as Alice, is to investigate the defacement, with an eye towards reconstructing the attack via the Lockheed Martin Kill Chain.

![Defacement image found when visiting our defending web](https://cyberdefenders.org/static/img/BOTSv1/Defacement.png)

## Scenario 2 (Ransomeware):

In the second scenario, one of your users is greeted by this image on a Windows desktop that is claiming that files on the system have been encrypted and payment must be made to get the files back. It appears that a machine has been infected with Cerber ransomware at Wayne Enterprises and your goal is to investigate the ransomware with an eye towards reconstructing the attack.

![Desktop background image informs of Ransomware and demands payment](https://cyberdefenders.org/static/img/BOTSv1/ransomewere.png)

# Process 


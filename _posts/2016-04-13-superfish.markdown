---
layout: post
title:  "Superfish"
date:   2016-04-12 22:13:22 +0800
categories: jekyll update
---

#### **Superfish** 

**What is it**<br>
According to its inventors, Superfish Visual Discovery was a software that was meant to help users find and discover products visually. However, it was really an adware that injects advertisement into a user's web browser. All is well if it is like other adwares which did not create much problems for the users except make their web browser cluttered and annoys them. Unfortunately, it caused other critical security problems due to the way it attempts to achieve its aim so let us go through the mode of operation the software before the explanation of its problems. 

**How it works**<br>
To achieve its goal of displaying "relevant" ads to the user, Superfish wants to be able to intercept and to be able to modify encrypted HTTPS traffic in order to inject ads into web pages displayed to the user. Under normal conditions a software should not be able to do so, however, Superfish installed its self-signed root CA certificate onto its user's computers which led it to be able to intercept encrypted connections as Man-in-the-Middle (MiTM). Hence, now whenever the user's web browser attempt to connect to a website, the browser will be tricked to think that it has made end-to-end encrypted connected with the website's server although it has in fact established the connection with Superfish. This MiTM does not directly harm the user but it led to vulnerabilities that a adversary can exploit. 

#### **Problem** 
One of the problems with Superfish is hinder the browser's ability to detect malicious websites. In order for it to be an effect MiTM it replaces the certificate of any website that the user is visiting with a certificate signed by Superfish. Since Superfish does not seem to verify the authenticity of a website's certificate before it certifies that website is safe to visit, the browser will now deem every website to be safe. 

Furthermore, in order for Superfish to generate certificates in real-time, the software contains a copy of Superfish's private key. This led to a vulnerability that can be exploited. One attack scenario can be as follows: the adversary can contain Superfish's private key and use Superfish's private key certificates for his spoofed websites. As long as the user's PC contain Superfish as a trusted CA, the user's PC can be tricked to trust the spoofed website. In addition, the Superfish private key can also be used for code signing so an adversary can trick you to trust any software you downloaded from his spoofed website - the adversary can use this chance to infect the user's PC with malware. 

#### **Measures** 
The obvious "solution" to the problem is to uninstall Superfish. However, that is still insufficient to protect the users from attacks as the Superfish Root Certificate is still listed as a trusted root certificate so the user's PC will continue to trust the attacker's spoofed website. Thus, to completely eliminate the possibilities of attacks caused by Superfish, the software has to be uninstalled and the Superfish root certificate has to be removed completely from the list of trusted certificates. 


# Day 2: The Psychology of Consistency

## Daily Reflection
Today’s module shifted focus from raw technical concepts to the cognitive and structural traps that cause most learners to drop out of cybersecurity. 

* **The Trap Identified:** Overwhelm (managing high school workloads while trying to build technical proficiency).
* **Key Takeaway:** Consistency beats intensity every single time; small daily habits outperform erratic bursts of effort.

## Action Plan
* Maintain the 45-minute daily study window.
* Document progress iteratively on GitHub rather than chasing superficial intensity.


 # Day 3 of 90  
 and today I ran my first security audit on myself.

Five-step methodology, real findings, one page report. I found 2 gaps across my own accounts and fixed enabled authenticator-app based 2FA on my primary email account before I finished the report.

The thing that reframed it for me: your email isn't just an account. It's the master key to every account linked to it.


# Day 4: Network Triage & Endpoint Baseline

Day 4 of 90 with . I just watched my own laptop have a conversation with 3 servers around the world that I never knowingly started.

Today's lesson: most people use computers like magic boxes. Cybersecurity people treat them as systems they can reason about.

The exercise: open Activity Monitor (or Task Manager on Windows). Look at the 200+ processes running right now. Pick 3 you don't recognize and Google them.

Most surprising thing I found: A background connection to a DigitalOcean cloud server while no third-party apps were actively being used.

 The gap between "I use a computer" and "I understand a computer" is getting smaller.


# Day 5: Web Traffic Triage & Third-Party Trackers

Day 5 of 90 with . I just opened my browser's dev tools and watched a single news article load over a hundred files from dozens of different domains.

Most of them I didn't know existed. Half of them are tracking me right now.

Today's lesson: when you type a URL and hit enter, your click makes seven stops before the page appears. DNS lookup, TCP handshake, TLS encryption, HTTP request, server response, browser render. Attackers can mess with every single one.

The exercise: open Chrome dev tools (F12), Network tab, reload a news site. Watch what actually loads.

Finding domains like PubMatic and Index Exchange running background cookie syncs on a simple news page made it obvious how heavily monitored everyday web traffic is.

85 days left. The gap between "I use the internet" and "I understand the internet" is getting smaller.


# Day 6: IP Geolocation, Public vs. Private IPs & NAT

Day 6 of 90 with @MyFirstHack. I just looked up my own IP address to see what every website already knows about me.

A website can see the public IP address used for the connection,which can reveal approximate geographic and network information.

Today's lesson: every device on the internet has a public IP address — and that address leaks your rough location, your ISP, and what kind of connection you're on, instantly, to every website you visit. No clicks. No permissions. Just the act of connecting. I also broke down the difference between private local addresses and public ones, how NAT shares a single public IP across a whole home network, and why the transition from IPv4 to IPv6 solves address exhaustion.

84 days left. I'm starting to see the internet the way defenders see it.

# Day 7: One Week Review & Reflection

Day 7 of 90 . One week in.

Realizing how many third-party ad trackers and script endpoints fire silently in the background of every single news page completely changed my view of web browsing. It's wild to see how much telemetry is exchanged before you even start reading an article.

Mapping out the IP address lifecycle showed me just how exposed standard network connections are, leaking rough geographic locations and ISP details instantly. Moving from a passive user to understanding public versus private IPs makes infrastructure visibility feel much more real.

Breaking down DNS vulnerabilities like hijacking, tunneling, and cache poisoning exposed how much the internet relies on trusting underlying translation systems. Recognizing that attackers target the foundational routing of names rather than just brute-forcing encryption makes system defense look completely different.

83 days left. 


# Day 8: Password Security & Human Vectors

Day 8 of 90 with. Week 2 begins — and it starts with passwords.

I just ran the built-in security check on my browser's saved passwords. 3 of them were flagged as compromised. I'd never looked at that list before today.

I used to think that throwing in numbers, uppercase letters, and random symbols made a short password genuinely secure, but length matters infinitely more than punctuation marks.

Today's lesson: complexity rules are security theatre. Length beats complexity. A different password for every site beats both. And two-factor authentication beats everything — because the strongest password in the world dies the moment you type it into the wrong login page.

82 days left. The machines were easier. The humans start now.


# Day 9: Phishing Vectors & Human Defenses

Day 9 of 90 with . Today was phishing — Phishing remains one of the most common ways attackers target users.


Seeing how subtly malicious domains can mimic legitimate services by swapping out standard characters completely changes how much you can trust a URL at a glance.

Today's lesson: phishing defense isn't about being smart enough to spot a fake. AI makes modern phishing too good for that. It's about five structural habits that bypass the trap entirely — hover before clicking, never authenticate from an email link, 2FA on everything, treat urgency as a red flag, verify through a second channel.

You don't have to out-think attackers. You just have to not click.

81 days left.

# Day 10: Data Mapping & Privacy Rights

Day 10 of 90  . Today was about data — the thing every breach is actually about, underneath all the technical detail.

I mapped where my personal data lives across three categories: PII, credentials, and proprietary. I found an old gaming forum account still holding my information, which I hadn't thought about in years.

I also requested a Google data export .

Realizing how precisely location logs stitch together daily routines through my Google Maps history made background telemetry feel a lot more tangible than abstract database records.

Ten days in. The lens is starting to feel like a habit.

80 days left.


# Day 11: Developer Tools & Network Request Inspection

Day 11 of 90 .

I just opened the developer tools on a website I use every single day, and watched it make over 75 separate network requests in the time it took to load.

Seeing tracking and analytics scripts fire off requests to third-party domains milliseconds before the actual user interface even finished rendering completely changed my perspective on how much telemetry is constantly exchanged behind the scenes.

A week ago I would have called that page "loaded." Today I can see it's still talking to a dozen different servers, running scripts from companies I never heard of, and that every one of those connections is a place security has to hold up.

The web is way bigger than what you see.

79 days left.

# Day 12 of 90 .

I've looked at a padlock in my browser thousands of times. Today was the first time I actually opened one up.

What surprised me most was learning that a valid certificate can prove you're connected securely, but it doesn't automatically mean the website itself is trustworthy.

The padlock proves the connection is encrypted. It does not prove the site is who you think it is, and it does not prove the site is safe.The icon attackers fear most is the same icon they hide behind.

Two weeks in. Starting to see how the layers of the web actually fit together.

78 days left.


# **Day 13 of 90 with @MyFirstHack.**
>
 Today I opened the cookie jar of a site I use every day. I'd clicked through a thousand cookie banners without ever looking at what was on the other side.

What surprised me most was that cookies aren't just about remembering preferences — some can actually keep you logged in by identifying your session.

 Cookies are not the dystopian thing the press makes them out to be. They're small pieces of data that let websites remember things about you between page loads. They're also one of the most valuable things for attackers to steal, because if an attacker gets your session cookie, the website may treat them as you — even if you have multi-factor authentication switched on.

 Two weeks in. The web is starting to feel less like magic and more like machinery.

 **77 days left.**



# **Day 14 of 90 

 I've had a Wi-Fi router for over a decade. Today was the first time I logged into the admin panel and audited it the way a security analyst would.

 **What surprised me most was how many security settings were still using defaults that I'd never thought to check.**>
A home Wi-Fi router is one device doing about five different security-relevant jobs at once. Most of us change the Wi-Fi password and never touch any of the rest. Default admin passwords. Firmware from years ago. Smart bulbs sharing a network with the laptop you do your taxes on.

 Two weeks done. Tomorrow's the first real project — analysing an actual phishing email start to finish. Everything from this week converges.

 **76 days left.**

 # Day 15 of 90 

Today I analysed a real phishing email start to finish — the way a SOC analyst would on the job.

URL submission to VirusTotal and URLScan.io. Social engineering breakdown. Final write-up in the format real SOC tickets take.

 What surprised me most was how legitimate the email looked at first, even though the URL behind it told a completely different story.**

Two weeks ago I would have looked at that email and dragged it into spam. Today I produced a one-page incident report on it. The skills feel real now.

 **75 days left.**


# Day 16 of 90 

 Today I audited my own phone the way a security professional would.

 What surprised me most was how many apps had permissions I didn't really remember giving them.**

 The phone is the master key to most of the rest of your digital life. Email, banking, two-factor codes, password manager, work account. Most of us treat it as casual. Today I looked at mine the way an attacker would.

 Also reported a real phishing URL to a public database used by major browsers. Small action, real defender work.

 74 days left.


# Day 17 of 90 


The cloud is just someone else's computer in someone else's data centre. Once you stop thinking of it as magic, the security questions get 
sharper. Whose computer is it? What lives on it? Who is responsible if something goes wrong?

 The Capital One breach in 2019 exposed about 100 million U.S. customers and 6 million Canadian customers. No zero-day was needed. The attacker exploited a misconfigured web application firewall and gained access to data stored in AWS S3.

73 days left.

 # Day 18 of 90 

Today I learned how attacks actually work. Not the movie version. The real one.

What surprised me most was how much of an attack can happen before the victim even realizes they're being targeted.

Real attacks follow seven stages: Reconnaissance, Weaponisation, Delivery, Exploitation, Installation, Command and Control, Actions on Objectives. The damage everyone talks about is stage 7. The real work happens in stages 1–6, often weeks earlier.

I mapped a recent breach to the kill chain, then ran the same exercise against myself. Seeing yourself through an attacker's eyes is uncomfortable and useful.

72 days left.


#  Day 19 of 90 

Today I learned the most uncomfortable truth in cybersecurity. The technology mostly works. The humans are the weakest layer. And the humans include me.

What surprised me most was how little information I needed to make a social engineering scenario sound believable.**

 The MGM Resorts breach in 2023 cost the company around $100 million and reportedly started with a social engineering attack on the help desk. The attackers used publicly available information to impersonate an employee and get access.

I built a pretext against myself today using only public information. It was uncomfortably plausible.

71 days left




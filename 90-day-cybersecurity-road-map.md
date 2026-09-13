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


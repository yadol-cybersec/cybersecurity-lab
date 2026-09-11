# Day 2: The Psychology of Consistency

## Daily Reflection
Today’s module shifted focus from raw technical concepts to the cognitive and structural traps that cause most learners to drop out of cybersecurity. 

* **The Trap Identified:** Overwhelm (managing high school workloads while trying to build technical proficiency).
* **Key Takeaway:** Consistency beats intensity every single time; small daily habits outperform erratic bursts of effort.

## Action Plan
* Maintain the 45-minute daily study window.
* Document progress iteratively on GitHub rather than chasing superficial intensity.


 # Day 3 of 90 with @MyFirstHack 
 and today I ran my first security audit on myself.

Five-step methodology, real findings, one page report. I found 2 gaps across my own accounts and fixed enabled authenticator-app based 2FA on my primary email account before I finished the report.

The thing that reframed it for me: your email isn't just an account. It's the master key to every account linked to it.

Portfolio piece number one. 87 days to go.

#myfirsthack


# Day 4: Network Triage & Endpoint Baseline

Day 4 of 90 with @MyFirstHack. I just watched my own laptop have a conversation with 3 servers around the world that I never knowingly started.

Today's lesson: most people use computers like magic boxes. Cybersecurity people treat them as systems they can reason about.

The exercise: open Activity Monitor (or Task Manager on Windows). Look at the 200+ processes running right now. Pick 3 you don't recognize and Google them.

Most surprising thing I found: A background connection to a DigitalOcean cloud server while no third-party apps were actively being used.

86 days left. The gap between "I use a computer" and "I understand a computer" is getting smaller.

#myfirsthack

# Day 5: Web Traffic Triage & Third-Party Trackers

Day 5 of 90 with @MyFirstHack. I just opened my browser's dev tools and watched a single news article load over a hundred files from dozens of different domains.

Most of them I didn't know existed. Half of them are tracking me right now.

Today's lesson: when you type a URL and hit enter, your click makes seven stops before the page appears. DNS lookup, TCP handshake, TLS encryption, HTTP request, server response, browser render. Attackers can mess with every single one.

The exercise: open Chrome dev tools (F12), Network tab, reload a news site. Watch what actually loads.

Finding domains like PubMatic and Index Exchange running background cookie syncs on a simple news page made it obvious how heavily monitored everyday web traffic is.

85 days left. The gap between "I use the internet" and "I understand the internet" is getting smaller.

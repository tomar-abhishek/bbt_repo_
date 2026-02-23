# Docker
---
# Introduction 
## Why docker?
- to understand , we have to go back a bit and think ,  Think in terms of traditional infra 
what was before it or what was the initial problem and solution to it ? and what was the issue with that particular soln?

Traditional infra had physical Servers: Each environment (Dev, SIT, Prod) required dedicated physical machines, leading to:
	Hardware issue-->
				High Costs:      Purchasing/maintaining identical hardware for each stage.
				Inconsistencies: SIT servers might differ from Dev (e.g., CPU architecture, RAM, OS patches).
				Example:         A Dev team tested on a Dell PowerEdge with 16GB RAM, but SIT used an older HP ProLiant with 8GB → Performance issues surfaced only in SIT.
	Env issues--> {works on my machine}
				Manual Configuration:
								 Devs installed dependencies (e.g., Java SDK, databases) manually on their workstations.
								 SIT teams had to replicate these setups from scratch, often missing critical steps.
				Common Issues:
								 "It works in Dev but crashes in SIT" due to:
								 Missing dependencies | Path/environment variable mismatches | version conflicts (e.g., glibc versions on Linux).

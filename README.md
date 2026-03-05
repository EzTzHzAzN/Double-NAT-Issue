# Double-NAT-Issue
I will discuss how I discovered how double NAT was present on my network, and what I did to resolve it.

### 1. Investigating the Issue
I had just begun studying for the NET+ and wanted to try optimizing my network with what I had learned so far. The first issue that stood out to me was the speed of my computer. My computer is connected via MoCA, with the other end of it being connected to an Xfinity XB8 modem -specifically on the 1 gbps port. The MoCA guarantees speeds up to 2.5 gbps, and coupled with the 1 gbps port and my plan guarantees up to 1.2 gbps, I was expecting at least 800 mbps. When I ran the speed test, the results came back as 300 mbps down, 20 mbps up. This surprised me, given the hardware it was attached to, which prompted me to investigate further.

### 2. Troubleshooting the Issue
This was my first time troubleshooting a network so going into this process I wasn't familiar with many concepts, such as speed-capped ports; Which is why, in hindsight, some of these steps may seem unconventional. I started the investigation with what I thought was the most rational option, logging into the modem where I thought I would find a way to adjust the network speed. When I did login, I only found security options, and a list of connected devices; however I did make sure to take a mental note that the modem did have routing enabled. I then pivoted over the the router, where I adjusted some wireless and security settings, before discovering that routing was also enabled on the router. This meant that both devices were routing, and I discovered my network had double NAT.

### 3. Searching for a solution
I started diagnosing this first by deciding which device to use as a router. This was fairly easy 

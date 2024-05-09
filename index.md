ZiptieAI is my intelligent AI drone project and the (important) documentation I created along the way. There are 4 main URLs:

- **[ziptieai.com](https://ziptieai.com)**. This website. Built with Jekyll on Github pages. 
- **[docs.ziptieai.com](https://docs.ziptieai.com)**. A very minimal documentation website (built with ReadTheDocs/Sphinx). The docs site basically mimics the structure and content of the wiki pages , but in an easier to read format. I will gradually fill this site with more detailed information gleaned from the docx’s (word files) on my Google drive.
- **[Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki)**. The first place to look for udpated project info.
- **[Google drive](https://drive.google.com/drive/folders/1HrzLExPTAL5PIKx_j_y0GJ6_RANR8Tjm)**.  A lot of detailed .docx files (details are everything for this project). I am working alone without (human) assistance, so accurate, useful documentation is critical.  Note: These docs are currently more like lab notes, not finished docs. When learning the tech, it's very important to jot down as many details as possible, so that if needed, you can go back and figure out where you made a mistake. The plan is to eventually "distill" the useful content (and delete the chaff).
  
#### **Why the name "ZiptieAI"?**

The original idea for the name came from the zipties the Ukrainian army uses for their very flexible and mission ready drones. 

![drones](/assets/ziptiedrone2.png)

But it also applies to my approach to building drones, as shown by my first FPV drone with a plywood frame that was flight tested on my kitchen work table. 

![drones](/assets/ziptiedrone3.png)

The second first flight was my x500 with PX4 on 24.0505. I spent a week trying get it flying with Ardupilot, but could not get the motors to spin (same problem with Ardupilot on the plywood drone; I have not figured out the problem yet). With PX4 it took one day. Nice.

![drones](/assets/airborne2.png)


#### **The evolution of the drone project**

I started this project in late 2023 with no assistance, some basic AI experience, and no experience with drones. My learning approach:
- Find anything that you can get working. Search everywhere (Youtube, Google, etc).  
- Get help from Youtube, Stack Overflow, and Google search (without these sources, it would be impossible to do this yourself). 
- Document as much as possible (on the **[Google drive docs](https://drive.google.com/drive/folders/1HrzLExPTAL5PIKx_j_y0GJ6_RANR8Tjm)**).
- Constantly update the plan and concepts (in the **[Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki)**).


The following table summarizes the project stages:


| Project stage (Wiki "part") | Activities |
|-------|--------|
| Part 1 Simulation | Total simulation (of the drone, world, camera, etc)  |
| Part 2 AI on CC | AI with the focus on object recognition / detection on PC / CC's  |
| Part 3 Real FC | Further simulation, but with a real FC  |
| Part 4 Basic platform build | Building a Pixhawk (large) drone and SBee FPV (small) drone | 
| Part 5 Mission platform tech | STM32 tools, FC FW dev and API's, ROS, and stealth (wired) | 
| Part 6 Mission platforms | Specific mission platforms (such as mine clearance, target lock-on) | 



#### **Part 2: Types of AI apps / companion computers**

 **[Wiki part 2 (AI HW)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-2-Real-AI-HW)** focuses on AI on companion computers. This table (WIP) will summarize the AI app / CC combinations tested.

| CC | AI algorithm | Camera/driver |
|-------|--------|---------|
| Jetson Nano | xxx | xxx |
| PI4 | xxx | xxx |
| PI5 | xxx | xxx |


#### **Parts 3/4: Types of FC's / firmware**

Wiki parts **[3 (HITL)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-3-Real-FC-HITL)** and **[4 (Basic platform build)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-4-Platform-build)** focus on the FC/firmware combinations shown below (with status).

| Firmware | Pixhawk (6c) | FPV STM32 (SBee F405v3) |
|-------|--------|---------|
| Ardupilot | (almost) | (almost) |
| PX4 | Working | |
| Betaflight | | Working |
| INAV | | Working |


#### **Part 6: Mission platforms (future)**

Wiki part **[6 (Mission platforms)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-6-Mission-platforms)** will (future) focus on real-world mission platforms. Something like the following.

| Mission | Basic platform | AI components | Additional tech |
|-------|-------|--------|---------|
| Mine clearance | X-500 + PX4 | Infrared + (??) | (??) |
| Target pursuit | 7-inch FPV + INAV | PI5 + Haarcascades | (??) |

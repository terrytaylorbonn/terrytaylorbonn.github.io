ZiptieAI is my intelligent AI drone project and the (important) documentation I created along the way. There are 4 main URLs:

- **[ziptieai.com](https://ziptieai.com)**. This website. Built with Jekyll on Github pages. 
- **[docs.ziptieai.com](https://docs.ziptieai.com)**. A very minimal documentation website (built with ReadTheDocs/Sphinx). The docs site basically mimics the structure and content of the wiki pages , but in an easier to read format. I will gradually fill this site with more detailed information gleaned from the docx’s (word files) on my Google drive.
- **[Wiki](https://github.com/terrytaylorbonn/auxdrone/wiki)**. The first place to look for udpated project info.
- **[Google drive](https://drive.google.com/drive/folders/1HrzLExPTAL5PIKx_j_y0GJ6_RANR8Tjm)**.  A lot of detailed .docx files (details are everything for this project). I am working alone without (human) assistance, so accurate, useful documentation is critical.  Note: These docs are currently more like lab notes, not finished docs. When learning the tech, it's very important to jot down as many details as possible, so that if needed, you can go back and figure out where you made a mistake. The plan is to eventually "distill" the useful content (and delete the chaff).
  
#### **The inspiration for "Ziptie" drones**

The original idea for the "Ziptie" part of "ZiptieAI" came from the zipties the Ukrainian army uses for their very flexible and mission ready drones. 
- KISS ("keep it simple stupid"). Needless complexity is your biggest enemy. 
- Implement the minimal functionality to get the job done. 
- "Ziptie" add on whatever functioality is required. Be flexible, ready to change out parts as required. *This approach is critical for those of you building your first drone(s) at home.*

![drones](/assets/ziptiedrone2.png)


#### **My first build validates the Ziptie approach for new drone builders (like me)**

The "Ziptie" approach was critical for building my first drone, a minimalist setup with a plywood frame that was flight tested on my kitchen work table (photo below). 

This is the way to build your first drone. Why?
- The "experts" overload you with (1) too much functionality and (2) not enough details (missing steps). I focused on one thing: Getting the xxxx thing in the air. The first version had no camera, VTX, GPS, etc. 
- Getting into the air inside (on your workbench) is great for testing (just like wind tunnel testing). WEAR SAFETY GOGGLES. Getting all the channels on the RC (the controller with sticks) working is a major challenge for newcomers (a challenge that most expert bloggers conveniently bypass during in the "it's easy to get started flying" videos). I had some strange arming problem, and temporarily solved it by using the USB connection to air the drone.  
- Trying to scrunch all the components together on some little carbon fiber frame is (1) too difficult, (2) can cause mistakes (broken connections, etc),  (3) very difficult to debug problems, and (4) extremely difficult to make modifications.
- The extra weight of the plywood and the bad aerodynamics of the fat plywood arms reduce the ability of the copter to get out of control on your first flight.

Turned out that this approach saved me a lot of trouble. The SpeedyBee F405 FC/ESC has a (well deserved) bad reputation for quality. I could not get the motors to spin. I thought maybe I had ruined my ESC's because I first plugged in a 6S battery (24V) before I realized that you had to used 4S (16V) (batteries are one of those critical and even dangerous details the experts tend to not mention). I was ready to just order a new ESC, but first started probing around. I discovered that the plastic housing of the female connecter (between FC and ESC) was defective. It had caused a pin (GND) to be bend as possibly short with a neighboring pin (the connectors fragile, tiny, and low quality). I used some very small tweezers to hack around on the connector, and ... wow, it worked.

I was able to try all kinds of hacks because my parts were not all scrunched up into one tiny mess.

![drones](/assets/ziptiedrone3.png)

PS: About the "details" of what I did: I plan to eventually have detailed docs for first time users, unlike the experts who conveniently leave out critical details (their main priority is getting you to watch their videos and manufacturers to send them free stuff to demo how "simple" it is to implement). Dont get me wrong, without these experts I never could have gotten started. I love these guys. I appreciate what they do. But its important to understand their focus. Anyway, I documented what I did. The doc is still rough (sorry), but for the details of the problem above: 
- Open https://drive.google.com/drive/folders/1WlY6zvOpCwWWgh_mhLvZRCXwSPR9WZ7B
- Download and open 4.5a-01_CONFIG_SBEE_BF_brodie_v07_24.0414.docx 
- Search for "problem discovered".

#### **My second build also validates the Ziptie approach**

The second first flight was my x500 with PX4 on 24.0505. I spent a week trying get it flying with Ardupilot, but could not get the motors to spin (same problem with Ardupilot on the plywood drone; I have not figured out the problem yet). With PX4 it took one day. Nice. 

This is why you need to be flexible. Ziptie together whatever components and software you need to get the job done. I had heard all this great stuff about Ardupilot, and frankly I was very surprised at (1) the low quality of the docs and (2) the difficulty of configuration (Mission planner is sheer chaos). If you hit the wall, or get lost in a rabbit hole, search for other options. I will try to tackle Ardupilot later (though, honestly, I now want to focus on PX4; I recommend PX4 over Ardudpilot to any newcomer).

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

 **[Wiki part 2 (AI HW)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-2-Real-AI-HW)** focuses on AI on companion computers. If you aren't into AI, then skip this part. My real focus (at least at first) was AI. I just wanted to use a simple quadcopter as a platform for the AI equipment. 
   
 This table (WIP) will summarize the AI app / CC combinations tested.

| CC | AI algorithm | Camera/driver |
|-------|--------|---------|
| Jetson Nano | xxx | xxx |
| PI4 | xxx | xxx |
| PI5 | xxx | xxx |


#### **Parts 3/4: Types of FC's / firmware**

Wiki parts **[3 (HITL)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-3-Real-FC-HITL)** and **[4 (Basic platform build)](https://github.com/terrytaylorbonn/auxdrone/wiki/Part-4-Platform-build)** focus on the FC/firmware combinations shown below (with status). If you aren't into HITL, then skip part 3.

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

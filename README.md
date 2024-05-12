**The cheapest and easiest Solution i could find for better IRL Streaming (for IPhone)**

# Schematic

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/2ec96f0e-5e8e-4693-a3cf-0f97a35c9f09" height="1000">

> [!NOTE]  
> At first this looks pretty complicated, but we will go Step-by-Step with Pictures *(when available)* trough the whole Setup Process.
> Yes there are completely free methods, but they need more technical expertise and if wrongly configured can be a security risk to your Home PC.
> With this Method you don't open up any holes in your Security. *(OBS srt caller instead of listener on Home PC)*

**Positives**  

- 👍 can be used with a single Internet connection from Phone
- 👍 when connection is failing from Phone to Internet, the Viewer will still see Videos/Clips
- 👍 a second internet can be added to make Phone Stream more reliable
- 👍 when switching from WiFi to Mobile and back stream is not going offline

**Negatives**  

- 👎 Additional monthly cost for Relay Server ($10 USD)
- 👎 Additional monthly cost for 2nd Internet (Optional)
- 👎 Takes some time for first Setup
---
# 1 - Streaming Phone  

> [!NOTE]   
> If you have multiple phones, use the strongest/newest one as Streaming Phone

1.a - Install the **[Moblin App](https://apps.apple.com/us/app/moblin/id6466745933)** from the Apple Play Store

---
# 2 - SRT/SRTLA Relay

> [!NOTE]   
> This Server takes the Two SRTLA Streams and combine them to one
> [!IMPORTANT]   
> This Service costs $10 USD. Completely free alternatives are also available but need more technical knowledge to setup

2.a - Create an Account with [Github](https://github.com/signup) *(If you already have one skip to Login)*
You then need to Verify your E-Mail Address and [Login](https://github.com/login)

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/bafd6a15-7ec2-4f3e-8a1f-7737e41d9a8f" height="600">

2.b - Once logged in open the [Belabox Sponsorship](https://github.com/sponsors/rationalsa) Page  
 - Scroll down and select the **$10 a month** Tier which includes 1x SRT/SRTLA Relay Server
 - Fill out your Billing Info and Set Up your Payment Info *(Only Credit Card or Paypal supported)*
 - Alternatively you can also let your Viewers buy [Vouchers](https://shop.belabox.net/product/belabox-cloud-voucher) for multiple Months.  
2.c - Once you either sponsored or have a voucher open the [Belabox Cloud](https://cloud.belabox.net) Page and Login/Authorize with your Github Account  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/5385a7b6-e1c4-42ac-a5a1-729cf53dc732" height="600">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/f8b19ac5-7862-4097-8701-78001048d003" height="600">

2.d - On the Top of the Page press the **3 Lines** then **SRT(LA) relays**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/4c33128e-253c-493e-8d40-2c19e67a2389" height="600">

2.e - Click on **Add** and change the Name. Change the **Server** to your **closest Location**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/8425c1a1-add3-40d1-8082-b03312429539" height="600">

2.f - Scroll down until you see **Moblin Settings** and tap the **Add automatically to Moblin** Button to automatically add the right Server Info in Moblin.  

---
# 3 - Streaming Phone
3.a - Open the **Moblin App**  and go to **Gear** Symbol *(Settings)* on the top right  
3.b - Go to **Streams** and then tap the **Belabox Cloud** one  
3.c - Go to **Video** and set the following settings  
 - **Resolution:** 1920x1080p  
 - **FPS:** fixed 30fps  
 - **Bitrate:** 4500 kbps  
 - **Codec:** HEVC(h2.65)

3.d - Go back then to **Twitch** and enter your Twitch Name and Twitch ID. You can get the ID from [here](https://www.streamweasels.com/tools/convert-twitch-username-to-user-id/)  
3.e - Next we want to add our Alerts to Moblin. To do this we go to into our Alerts Dashboard via Browser  
 - [Streamlabs](https://streamlabs.com/dashboard#/alertbox) and copy the Widget URL

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/255e3ef7-cbd5-4cfa-84a8-17d68c78ccb6" height="600">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/82365cc6-ade2-458f-b583-ccad4b0b62f1" height="600">

3.f - Head back to Moblin and go to the **Settings** Screen. Tap on **Scenes** then on **Widgets** then **Create**. Name it **Alerts**  
3.g - Set type to **Browser** and paste the Widget URL into **URL** Field.  
and Set Width to 1920 and Height to 1080 *(you change size if the Alerts are too big)*  
3.h - Go back to the **Scenes** Menu. Tap on **My scene** Tap **Add Widget** and add the **Alert**-Widget we just created. Make sure its on the Top of the List.  
3.i - Go back to the **Main View** and **check** that **Chat** is loading and that **Alerts** are **working** *(Test-Alerts are available in the Dashboard)*  

---
# 4 - Home PC
Any normal PC or Laptop can be used, best cabled directly to your Home Internet Router. If you want to buy a new one for this, maybe look into Mini-Pc's.
> [!NOTE]  
> The following Pictures are from Windows, but the steps are mostly the same except additional ones for [MAC](#421-noalbs-on-mac)

## 4.1 OBS
> [!NOTE]  
> This is the Programm that converts the Stream back to old RTMP/h.264 Standards and streams it directly to Twitch. Here you have a lot of Options to set Videos, Text, Music to entertain your viewers while you reconnect*

4.1.a - **Download [OBS Studio](https://obsproject.com/download)** for your System  
4.1.b - **Install OBS** Studio and **Launch** it.  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/3555ea78-d6bd-440b-9bdc-15a91799f1a2" height="400">

4.1.c - In the Auto-Wizard 
 - Optimize for Streaming
 - **Resolution:** 1920x1080
 - **FPS:** 30
 - **Service:** Twitch
 - Connect Account
 - Log in the newly popped up Window.
 - Uncheck the **Estimate bitrate** and enter manually **5900** *(7900 if you're Twitch Partner)*
 - **Finish** the Wizard

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/a6164a26-5ba9-4219-9c22-c2eb6abfa0e1" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/bafb9a3c-1d6e-4909-9c78-d0381c521b30" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/4bf17fc2-00ad-40b0-b262-0334f62d978a" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/c7e714a3-fd5a-4783-aaff-9c82ea227f59" height="400">

4.1.d - **In OBS** on the bottom left **add** now following **scenes**
 - Starting
 - Live
 - Low
 - Disconnected
 - Privacy
 - Ending

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/344aaedc-92df-41c1-9e65-1dd6223deb0d" width="600">

4.1.e - Click on the Live Scene, and add a **Media Source** and with name **Belabox Cloud**. 
 - A new Window with settings will open

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/dedc65b3-03c6-4ad0-a2f6-ef907ff541cc" width="600">

4.1.f - Open the **[Belabox Cloud](https://cloud.belabox.net/#relays)** Page  
 - go to **SRT(LA) relays** and
 - scroll down until you see **OBS Media Source Settings**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/d6669e01-035c-4879-aa2e-df7ebe333b9a" width="600">

4.1.g - **Go back** to **OBS** and **set** the **same settings**
 - Uncheck Local File
 - Set Network Buffering to 1 MB
 - Copy Input from Belabox Cloud Page
 - Set Reconnect Delay to 2S
 - Check Close file when inactive

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/fb5d68c6-b45b-4b40-8f70-ad1aaf224e78" width="600">

4.1.h - Right-click on the **Belabox Cloud**-Source, then **Transform** and **Fit to Screen** *(or select it and hit CTRL+F)*  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/c993bb43-a3ea-4bc5-a75a-c46858d2305e" width="600">

4.1.i - Then Copy *(CTRL+C)* the **Bellabox-Cloud**-Source over to the **Low** Scene  
4.1.j - Go To **Settings** on the bottom right. In the new Video select **Audio** and **Disable all Global Audio Devices**  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/20b58802-fc64-491d-9d74-3bd0aef2d93d" width="500">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/87a30f26-a525-47c2-9427-b0a1ffbe7067" width="500">

4.1.k - On the top menu bar click on **Tools** then on **Websocket Server Settings**. Check the **Enable WebSocket Server** and hit **OK**  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/cec9078c-a2e2-45dc-9bec-24041f19a98f" width="500">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/918e7d93-3191-4080-b5e3-3d1c8c4b9d85" width="500">

---
## 4.2 NOALBS
> [!NOTE]  
> This is the Program controls the scene switching via Chat and automatically if no incoming Stream is detected

4.2.a - **Download [NOALBS](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching/releases)** for your System and unpack them to a location of your liking  
4.2.b - Inside this Folder you should have at least 3 files (4 for [MAC](#421-noalbs-on-mac))  
 - .env
 - config.json
 - noalbs

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/98043a2b-2497-40af-88c7-873ce2d85848" height="100">

4.2.c - For NOALBS to respond to our Chat commands we need to give access to a Twitch Account. Once you logged in with your preferred Account in Twitch click on this **[Link](https://twitchapps.com/tmi)**, then hit **Connect** and copy the **oauth:xxxxxxx** Code  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/6eac3092-a208-438e-ac08-c68faf69151c" height="300">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/c52f6156-e52f-4ea7-a115-36d488648555" height="130">

4.2.d - **Open** the **.env** File with a Text-Editor
 - Username of the used Account
 - replace the *oauth:YOUR_OAUTH_HERE* with your copied data
 - save and close the file

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/33dabd80-1a70-4ac1-8451-b942200767b0" height="40">

4.2.e - Download the File and replace it with your **config.json**  
[config.json](config.json)  
4.2.f - **Open** the **config.json** File with a Text-Editor  
 - replace all 3x of *REPLACE_STREAMER_NAME* with your Twitch Account Name

4.2.g - open the Open the **[Belabox Cloud](https://cloud.belabox.net/#relays)** Page and go to **SRT(LA) relays**  
 - Scroll down to **NOALBSv2 configuration**
 - replace *REPLACE_BELLABOX_URL* with the URL from the Belabox Page
 - replace *REPLACE_BELLABOX_INGEST_KEY* with the last Part of the URL

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/fe194e73-c223-4327-9680-af1b570869b1" height="350">

4.2.h - Go back to OBS into the Websocket Settings and click on **Show Connect Info**. 
 - Copy the **Server Password**
 - replace *REPLACE_OBS_WEBSOCKET_PASSWORD* with the copied data

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/ab6652a4-7ff0-41f6-8746-1290e2d243ba" height="200">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/7f04f75c-0611-43d6-8831-5fc8487981db" height="300">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/f16885ce-8c51-4bb4-92fa-b0e7311f3b41" height="100">

4.2.i - Save and close the file. *Detailed Infos [NOALBS Github](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching)*  
4.2.j - Start the **noalbs** programm. It should look like the picture below. Errors are also shown here  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/0329e383-07f3-40e8-8f80-de3d0fa3391d" height="270">

### 4.2.1 NOALBS on MAC
You must have these 4 files in the *same folder*
- .env
- noalbs
- config.json
- launch.sh

To keep the files together i recommend to make new folders under Documents -> Stream -> NOALBS

Sometimes .env will not show or download due to the . in the name
[.env](env)
Just Download it from here again and place it in the same folder

Open up a Terminal Window and enter command
`cd /Users/`yourusername`/Documents/Stream/NOALBS`
where **yourusername** = your username on the MAC and the Path to the folder, if you have a different one. Then hit **Enter**
`mv env .env` and hit **Enter**
env File should now vanish in Finder *(You can show it in Finder by pressing* **Command + Shift + .** *)*

4.2.1.a - Make sure .sh files are **always opened** with the Terminal app  
4.2.1.b - Follow these instructions from Developer  
`You have to first open the NOALBS executable, and confirm that the developer is not verified, NOALBS should run with Errors. Close it. After that you can start it with .sh file`  
> [!NOTE]  
> Opening the launch.sh in the Terminal app will always start up NOALBS from within the directory it is in.

> [!TIP]
> You can also make an Alias to the launch.sh and put it on the desktop to not forget to run it. 

---
# 5 - Make OBS pretty
We are finished with the basic Setup, but the Scenes are pretty emtpy.
Following is an Explanation on what Scene is used for what and what People normally put in. 
> [!NOTE]  
> Following are just recommendations. Feel free to design however you want.

**Starting**
- Every time the Stream starts with this scene until the phone is live
- Video+Music is often used as Background
- simple Text "Starting Soon ..."

**Live**
- As soon as there is a connection from the Phone to OBS this will be shown
- No additional things needed, since Overlays should run on the Phone

**Low**
- When connection to the Phone is bad quality
- simple Text "low bitrate"
  
**Disconnected**
- When the connection to Phone is lost completely this is shown
- old Stream or Clips are often used (For Clips i recommend a Folder named Clips and adding a VLC Media Source *requires [VLC Media Player](https://www.videolan.org/vlc/)*)
- simple Text "Lost connection..." on Top
- simple Text "Be right back"
  
**Privacy**
- Can be activated by writing !privacy in Twitch-Chat
- Similar to Disconnected
- Can be switched to when you go to Toilet or have private Conversation for a few Minutes
  
**Ending**
- Can be activated by writing !ending in Twitch-Chat
- Similar to Starting Video+Music
- Simple Text "Ending Stream"

---
# 6 - First Test  
6.a - to Start the stream, go into your Twitch Chat and enter **!start**  
OBS will now start the Stream in the **Starting**-Scene  
6.b - Go to your Streaming Phone into the **Moblin**-App and start your Stream there  
6.c - After a few Seconds the Stream from the Phone reaches the OBS and NOALBS switches to **Live-Scene**  
6.d - When you loose Connection or you stop the Stream in **Moblin**-App,
it should automatically switch to **Disconnected** and back as soon as Phone Stream is ok again.  
6.e - You can manually switch to **Privacy** with the Chat-Command **!privacy** and back with **!live**  
6.f - To End your Stream you either put **!stop** into Twitch-Chat or you make a Raid to another Streamer  

---
# 7 - Normal Operation 
> [!NOTE]  
> Before **every** IRL-Stream you need to do the following

7.a - **Start** your **PC** at Home an make sure it has a Internet Connection and doesn't turn off automatically  
7.b - **Go outside** to where you want to start to stream  
7.c - Enter **!start** in **Twitch-Chat** to start Stream to Twitch  
7.d - **Start Stream in Moblin App**, after a few seconds you are live  
7.e - Enter **!stop** in **Twitch-Chat** or **Raid another streamer** to stop Stream  

---
# 8 - 2nd Internet Connection  
As seen in the Plan there should be 2x Internet Connection for your phone to reduce the chance of outtages for the Live Stream.  
Either a Mobile WiFi Router or a Second Phone with Mobile Hotspot active.    
> [!IMPORTANT]  
> For this second SIM a different Provider is highly recommended.
> The 2nd Sim will also consume about ~50% of the overall Data

---
# 9 - Additional Help  
### Moblin App 
Here is their [Discord](https://discord.gg/Tm6kf778)
### OBS 
you can check their [Forum](https://obsproject.com/forum/) or just look up one of the hundreds of Youtube Tutorials
### NOALBS
Here is the Guide on [Github](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching) and their [Discord](https://discord.gg/efWu5HWM2u)


---
title: Using the Oculus Quest without an Account
layout: post
post-image: /assets/images/posts/Account-Removal.png
description: This tutorial will show you how to remove you Oculus/FaceBook account from your quest
tags:
- oculus
- oculus quest
- quest
- sideloading
- tutorial
---

## Please read before you continue
This tutorial has been tested on multiple Quest 1 and 2 devices, but there is always the chance that something might not work on your device and that something will break. If you just want to use your Quest 2 without FaceBook account and are ok with using an Oculus / Oculus Developer account follow this [Video Tutorial](https://www.youtube.com/watch?v=5cyijb7CJZU), which has *no* sideeffects. ~~Then do the "Disabeling additional Telemetry" and maybe "Prevent logging back in and disable killswitch" of this tutorial.~~ (This part has been removed, as it doesn't work after update V25)

I'd like to thank [u/fisk47](https://www.reddit.com/user/fisk47) and [u/doctor_blob](https://www.reddit.com/user/doctor_blob) for testing this on their Quests

##### What does work?
- Handtracking
- Using sideloaded apps and sideloading apps still works
- Casting from your Quest wirelessly to a PC via ADB / SideQuest
- Using the Quest as a PCVR headset via ALVR, VRidge or Link (you still have to be logged into an account on your PC to use Link)

##### What doesn't work?
- You will have to use a third party app launcher like [Quest App Launcher](https://github.com/tverona1/QuestAppLauncher) to open apps from the Oculus Store
- Most apps downloaded through the Oculus Store won't work because of entitlement errors (Including Virtual Desktop :/)
- You will have to have logged into an account on your quest at least onece to enable developer mode.
- You won't be able to use the Oculus Store while not logged in
- FaceBooks social (media) features don't work.
- The normal casting options
- The build in Browser
- Oculus TV

##### Positive sideeffects
- Disables *some* FaceBook Telemetry
- The [Piracy Killswitch](https://www.reddit.com/r/OculusQuest/comments/dnuxfs/just_a_heads_up_that_the_latest_quest_90_update/) won't work anymore


# Tutorial
### Setting up the Quest 2 with an Oculus/Oculus Dev Accound instead of a FaceBook account (optional)
This step is optional and the tutorial will work with a FaceBook account, but you can follow this [Video Tutorial](https://www.youtube.com/watch?v=5cyijb7CJZU) by "No Borscht For You" (original tutorial by [u/Tiger-Hobbes](https://www.reddit.com/r/OculusQuest/comments/jd6cfi/the_quest_2_has_allegedly_successfully_been_rooted/g9617l2?utm_source=share&utm_medium=web2x&context=3)) to set up your Quest 2 without a FaceBook account. 
*Maybe that's all you have been looking for, as just using an Oculus account doesn't have the sideeffects of this method (except not working FaceBook social features)*

### Sideloading the apk
If you already know how to sideload an APK to the Quest just download the APK from step 1.
1. Download the Oculess.apk from [here](https://github.com/basti564/Oculess/releases)
2. Follow this this [Video Guide](https://youtu.be/RoIXxIfRNTw?t=125) by "Virtual Reality Oasis"
3. Click this icon in sidequest 

![Install APK from folder](/assets/images/posts/install.PNG)
4. Select the .apk file you have downloaded in step 1
5. Wait for the upload to finish

### Logging out
1. Put on your Quest headset
2. Select the "Apps" tab
3. In the top right select "Unknown Sources" from the drop down menu
4. Open the "Oculess" app (com.bos.oculess)
5. Click the "DISABLE COMPANION" Button
6. Choose "Companion Server" from the List
7. Click "Deactivate this device admin app" 
8. Restart your Quest

### ~~Prevent logging back in and disable killswitch (optional)~~
~~This will prevent you from logging back in and will also disable other unwanted stuff like the developer mode killswitch~~
1. ~~Open the "Oculess" app~~
2. ~~Disable the Oculus Companion Server (again) if it's active~~
3. ~~Open SideQuest on your PC~~
4. ~~Click this icon in sidequest~~
![Run ADB commands](/assets/images/posts/run.PNG)
5. ~~Click "CUSTOM COMMAND" in the drop down menu~~
6. ~~Paste the following command in the "Command To Run..." box :~~
~~``` adb shell pm disable-user --user 0 com.oculus.companion.server ```~~
7. ~~Click on "RUN COMMAND"~~

~~To reverse this just run the folloging command:~~
~~``` adb shell pm enable com.oculus.companion.server ```~~


### ~~Disabeling additional Telemetry (optional)~~
~~Do the steps from "Prevent logging back in" up to step 5 and paste the following command and click "RUN COMMAND"~~
```
adb shell pm disable-user --user 0 com.oculus.unifiedtelemetry & adb shell pm disable-user --user 0 com.oculus.gatekeeperservice & adb shell pm disable-user --user 0 com.oculus.notification_proxy & adb shell pm disable-user --user 0 com.oculus.bugreporter & adb shell pm disable-user --user 0 com.oculus.os.logcollector & adb shell pm disable-user --user 0 com.oculus.appsafety
```

### Logging back in
1. Check in the "Oculess" app if the Companion Server is started
2. If it isn't click on the "ENABLE COMPANION", select "Companion Server" from the List and click "Activate this device admin app".
3. Check that your Quest is on the same network as your phone
4. Open the "Oculus" app on your phone
5. Got to the "Settings" tab
6. Click on your Quest and wait for your Quest to connect
7. Restart your Quest


The title image background was made by [kyu3](https://kyu3.blog.jp/profile.html) under the Creative Commons Licence (CC - BY - SA)

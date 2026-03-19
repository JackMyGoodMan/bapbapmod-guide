---
{"dg-publish":true,"permalink":"/how-to-set-up/","tags":["gardenEntry"]}
---

1. Install Visual Studio or some other IDE
2. Install BAPBAP through the BAPBAP launcher and run the game once.
3. the .NET framework should have installed automatically when you ran the modded game, if it didn't install it.
4. open Visual Studio or your IDE of choice and create a new project using "Class Library (.net Framework)"
![Pasted image 20260319201844.png](/img/user/Images/Pasted%20image%2020260319201844.png)
5. In the solution explorer right click on references, the click add reference.
6. find the following references, in your instance files.
7. ![Pasted image 20260319205330.png](/img/user/Images/Pasted%20image%2020260319205330.png)
   note:
   some of these have 2 or 3 versions in your instance files, I use the versions found in the "net35" and the "Il2CppAssemblies" folder when I can. "Il2CppInterop.Runtime.dll" isn't in net35 so I used the net6 one which seemed to work, I wouldn't recommend mixing them unless you have too though.
   *not all of these are required for every project however I needed them for my small mod and I don't remember which ones aren't necessary.
8. click the "Properties" dropdown in the solution explorer and open "AssemblyInfo.cs"
9. just under the using declarations copy and paste this:
   "[assembly: MelonInfo(typeof(*Name of your Class*), "*Name of your Mod*", "*Version Number formatted the same as 2.1.4*", "*Author Name*")]
   [assembly: MelonGame("gg.bapbap", "BAPBAP")]"
10. you are now set up, this video documents how to install unity explorer and how to program a basic mod. 
    https://youtu.be/F7kuby5JuJI?si=xzeG_G9w2F_mHRZL 
    please use this link to download unity explorer instead of the one the video supplies: [UnityExplorer.MelonLoader.IL2CPP.CoreCLR.zip](https://github.com/yukieiji/UnityExplorer/releases/download/v4.13.5/UnityExplorer.MelonLoader.IL2CPP.CoreCLR.zip)

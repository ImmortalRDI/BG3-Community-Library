# **Visual Effects** <!-- omit from toc -->
Also known as VFX. You generally find these as UUIDS you attach to data nodes such as `"PrepareEffect"`, `"CastEffect"`, and so on. Now, these are all things created by Larian, but did you know, you can create your very own visual styles for your spells, statuses and much more? Stay tuned  to find out more!

***
# **Table of Contents** <!-- omit from toc -->
1. [**Introductions**](#introductions)
2. [**Getting Started**](#getting-started)
3. [**Effects**](#effects)
4. [**MultiEffectInfos**](#multieffectinfos)
5. [**Root Templates**](#root-templates)
6. [**Merged Files**](#merged-files)
7. [**LSFX Files**](#lsfx-files)
8. [**Hot Testing**](#hot-testing)
9. [**Advanced Tips**](#advanced-tips)
10. [**Useful Resources**](#useful-resources)
11. [**Summary**](#summary)


## **Introductions**
It's me, ***ImmortalRD***, the Coolest Custom VFX guy around! Ok, I'm only joking, but never-the-less, I am here today to teach you how to create your very own visual effects for your spells, statuses and more. In case you're worried I lack the qualifications to teach you jack, diddly OR squat, you can find some of my work as referenced:
- [**Whispers of the Divine - Aasimar Race**](https://www.nexusmods.com/baldursgate3/mods/4159/) by [**Tripsadin**](https://www.nexusmods.com/baldursgate3/users/121922323)

    Created Transformation Effects for Harbinger Wings spell
- [**Followers of Zerthimon - Githzerai**](https://www.nexusmods.com/baldursgate3/mods/3460) by [**KazSuhra**](https://www.nexusmods.com/baldursgate3/users/129454108)

    Created Effects for Psychic Lance Spell

- [**Mythical Power**](https://www.nexusmods.com/baldursgate3/mods/4095?tab=posts) by [**ImmortalRD**](https://www.nexusmods.com/users/1601537)

Now, hopefully, you are sufficiently convinced that I might be able to help guide you through this seemingly arduous task. Moving on to our next topic:

## **Getting Started**
Alright, let's get started with creating your very own visual effects? What? You're feeling overwhelmed by all of the things you might need, and so forth? Relax, take a deep breath. I got you. Just take a look below on what you'll need to get started making the best darned effects this side of the (Insert Location Here). Go check it out.
>## **Requirements**
*   [**Baldur's Gate 3**](https://baldursgate3.game/) by [**Larian Studios**](https://larian.com/)
*   [**BG3ModManager**](https://github.com/LaughingLeader/BG3ModManager) by [**LaughingLeader**](https://github.com/LaughingLeader)
*   [**lslib**](https://github.com/Norbyte/lslib/releases) by [**Norbyte**](https://github.com/Norbyte)
*   [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool) by [**ShinyHobo**](https://github.com/ShinyHobo)
*   [**VSCode**](https://code.visualstudio.com/), [**Notepad++**](https://notepad-plus-plus.org/) or any other text/code editor.
*   A spell, Status, Passive, Equipment, etc that you want to apply visual effects to.
*   A [**MultiEffectInfos**](#multieffectinfos) File AND/OR  A [**RootTemplate**](#root-templates) File
*   A [**_merged**](#merged-files) File
*   An [**lsfx**](#lsfx-files) File
*   <ins>**Patience**</ins>
*   <ins>**Imagination**</ins>
>### [**Baldur's Gate 3**](https://baldursgate3.game/)
If you managed to find your way here on accident, this is a visual effects tutorial page for the game [**Baldur's Gate 3**](https://baldursgate3.game/) by [**Larian Studios**](https://larian.com/). So, without this masterpiece of a video game, none of this would even be possible, or matter.
>### [**BG3ModManager**](https://github.com/LaughingLeader/BG3ModManager)
To begin any sort of modding, whether or creating mods or playing the game with them, you will need this handy dandy mod manager tool by [**LaughingLeader**](https://github.com/LaughingLeader). This fantastic tool helps organize your active and inactive mods all in the comfort of a single application.
>### [**lslib**](https://github.com/Norbyte/lslib/releases)
This wonderful tool, created by [**Norbyte**](https://github.com/Norbyte), will be needed for a variety of things, from paking mods and  [**LSFX Files**](#lsfx-files), to [**Hot Testing**](#hot-testing). You will be using this tool a lot.
>### [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool)
This brilliant little doodaad is a must have for any modder on the go. Created by [**ShinyHobo**](ShinyHobo), it will allow you to accomplish a variety of tasks. Using  [**lslib**](https://github.com/Norbyte/lslib/releases) to handle functions, this allows you to pack your mod, search base game files, generate UUIDs and more.
>### [**VSCode**](https://code.visualstudio.com/)
This is a text/code editor that you will need to get anything done. It is my preferred editor.
>### [**Notepad++**](https://notepad-plus-plus.org/)
This is another option for code editing. It does mostly the same thing as [**VSCode**](https://code.visualstudio.com/), only with a different layout and color scheme. Pick one, or another of your choice.
>### **Something to Apply the Effect to**
This can be anything from a spell, status, passive, weapon, armor or more. The possibilities are endless! Well, not really, but there are a lot of possibilities.
>### [**MultiEffectInfos**](#multieffectinfos)
This is an .lsf file that contains a collection of effects, attached to different things for different reasons. All gathered together in a neat little package, that comes with a UUID. We'll get more into that later.
>### [**RootTemplate**](#root-templates)
This is similar to a [**MultiEffectInfos**](#multieffectinfos) in that it can contain various Visual effects. However, there are some major differences that we will discuss momentarily.
>### [**_merged**](#merged-files)
This, quite simply, is the games reference point. It will tell your [**MultiEffectInfos**](#multieffectinfos), [**RootTemplate**](#root-templates) and other stuff where to look for the [**lsfx**](#lsfx-files). More on that after these messages from our Sponsors </Play_30Minute_Advertisement(PreperationH).>
>### [**.lsfx**](#lsfx-files)
This is the core. You will find all of the bits and pieces associated with a particular VFX File. I'll tell you why it's so important in a bit.
>### <ins>**Patience**</ins>
You're going to need this. One, because this can end up being time consuming. But also, you have to put up with my awful jokes if you want to get through the rest of this tutorial.
![](../../GitHub/BG3-Community-Library/VFX-Tutorial/Patience.png)
>### <ins>**Imagination**</ins>
If you didn't really have this, you probably wouldn't have read this far in the first place, so congratulations, you're about ready to make some magic!
>### **Final Requirement Notes**
Alright, now that you know everything you need, we can finally move on to the next stage of my plan for world domi-...crap, wrong post. I mean let's get you on your way to making fun visual effects:
## **Effects**
Alright! You still with me? Hope you didn't give up because we've finally reached the meat and potatoes where it all starts. This is where things are going to start to get really fun. Of course, this is also where it can get a little overwhelming. However, that's why I'm here, to bore you to tears with my bad jokes and monotone guide. Let's do this.

Alright, the first thing you're 
## **MultiEffectInfos**
## **Root Templates**
## **Merged Files**
## **LSFX Files**
## **Hot Testing**
## **Advanced Tips**
## **Useful Resources**
## **Summary**
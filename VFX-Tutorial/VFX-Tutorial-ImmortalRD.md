# **Visual Effects** <!-- omit from toc -->
Also known as VFX. You generally find these as UUIDS you attach to data nodes such as `"PrepareEffect"`, `"CastEffect"`, and so on. Now, these are all things created by Larian, but did you know, you can create your very own visual styles for your spells, statuses and much more? Now...before you go all

![Not Readin' Em](https://i.imgur.com/jgZhvkd.png)

Stay tuned to learn more!

***
# **Table of Contents** <!-- omit from toc -->
1. [**Introductions**](#introductions)
2. [**Getting Started**](#getting-started)
   1. [**Requirements**](#requirements)
   2. [**Baldur's Gate 3**](#baldurs-gate-3)
   3. [**BG3ModManager**](#bg3modmanager)
   4. [**lslib**](#lslib)
   5. [**BG3-Modders-Multitool**](#bg3-modders-multitool)
   6. [**VSCode**](#vscode)
   7. [**Notepad++**](#notepad)
   8. [**Something to Apply the Effect to**](#something-to-apply-the-effect-to)
   9. [**MultiEffectInfos**](#multieffectinfos)
   10. [**RootTemplate**](#roottemplate)
   11. [**merged**](#merged)
3. [**Effects**](#effects)
4. [**MultiEffectInfos**](#multieffectinfos-1)
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
### **Requirements**
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
### [**Baldur's Gate 3**](https://baldursgate3.game/)
If you managed to find your way here on accident, this is a visual effects tutorial page for the game [**Baldur's Gate 3**](https://baldursgate3.game/) by [**Larian Studios**](https://larian.com/). So, without this masterpiece of a video game, none of this would even be possible, or matter.
### [**BG3ModManager**](https://github.com/LaughingLeader/BG3ModManager)
To begin any sort of modding, whether or creating mods or playing the game with them, you will need this handy dandy mod manager tool by [**LaughingLeader**](https://github.com/LaughingLeader). This fantastic tool helps organize your active and inactive mods all in the comfort of a single application.
### [**lslib**](https://github.com/Norbyte/lslib/releases)
This wonderful tool, created by [**Norbyte**](https://github.com/Norbyte), will be needed for a variety of things, from paking mods and  [**LSFX Files**](#lsfx-files), to [**Hot Testing**](#hot-testing). You will be using this tool a lot.
### [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool)
This brilliant little doodaad is a must have for any modder on the go. Created by [**ShinyHobo**](ShinyHobo), it will allow you to accomplish a variety of tasks. Using  [**lslib**](https://github.com/Norbyte/lslib/releases) to handle functions, this allows you to pack your mod, search base game files, generate UUIDs and more.
### [**VSCode**](https://code.visualstudio.com/)
This is a text/code editor that you will need to get anything done. It is my preferred editor.
### [**Notepad++**](https://notepad-plus-plus.org/)
This is another option for code editing. It does mostly the same thing as [**VSCode**](https://code.visualstudio.com/), only with a different layout and color scheme. Pick one, or another of your choice.
### **Something to Apply the Effect to**
This can be anything from a spell, status, passive, weapon, armor or more. The possibilities are endless! Well, not really, but there are a lot of possibilities.
### [**MultiEffectInfos**](#multieffectinfos)
This is an .lsf file that contains a collection of effects, attached to different things for different reasons. All gathered together in a neat little package, that comes with a UUID. We'll get more into that later.
### [**RootTemplate**](#root-templates)
This is similar to a [**MultiEffectInfos**](#multieffectinfos) in that it can contain various Visual effects. However, there are some major differences that we will discuss momentarily.
### [**merged**](#merged-files)
This, quite simply, is the games reference point. It will tell your [**MultiEffectInfos**](#multieffectinfos), [**RootTemplate**](#root-templates) and other stuff where to look for the [**lsfx**](#lsfx-files). More on that after these messages from our Sponsors </Play_30Minute_Advertisement(PreperationH).>
>### [**.lsfx**](#lsfx-files)
This is the core. You will find all of the bits and pieces associated with a particular VFX File. I'll tell you why it's so important in a bit.
>### <ins>**Patience**</ins>
You're going to need this. One, because this can end up being time consuming. But also, you have to put up with my awful jokes if you want to get through the rest of this tutorial.

![BadTime](https://i.imgur.com/9mi8c0b.png)
>### <ins>**Imagination**</ins>
If you didn't really have this, you probably wouldn't have read this far in the first place, so congratulations, you're about ready to make some magic!
>### **Final Requirement Notes**
Alright, now that you know everything you need, we can finally move on to the next stage of my plan for world domi-...crap, wrong post. I mean let's get you on your way to making fun visual effects:
## **Effects**
Alright! You still with me? Good. Hope you didn't give up because we've finally reached the meat and potatoes where it all starts. Before we begin, however

![Explosions?!](https://i.imgur.com/l59NIZK.png)

This is where things are going to start to get really fun. Of course, this is also where it can get a little overwhelming. Remember that thing I said about **Patience**? Here's where you'll start to need it. However, that's why I'm here, to bore you to tears with my bad jokes and monotone guide. Let's do this.

Alright, the first thing you're going to want is a spell, status, passive, or whatever it is you want to attach an effect to. The general idea is to find a spell or status with an effect you like, and get the UUID from the particular status you like. In the case of this tutorial, we'll use Black Hole as our visual effect:

```
new entry "Target_TAD_BlackHole"
type "SpellData"
data "SpellType" "Target"
using "Target_TADPOLE"
data "Cooldown" "OncePerShortRest"
data "SpellProperties" "Force(-6, TargetToEntity, Neutral, false, true);GROUND:ApplyStatus(SELF,TAD_BLACK_HOLE_AURA,100,5)"
data "TargetRadius" "18"
data "AreaRadius" "9"
data "SpellRoll" "not SavingThrow(Ability.Intelligence, SourceSpellDC())"
data "SpellSuccess" "ApplyStatus(TAD_BLACK_HOLE_SLOW,100,1)"
data "TargetConditions" "not Self() and not Ally()"
data "AoEConditions" "Character() and not Self() and Enemy()"
data "Icon" "TadpoleSuperPower_BlackHole"
data "DisplayName" "he71b1f23gc2bdg45f0g99c1g9f476ec396b6;2"
data "Description" "h3a37227bgeba3g476egbb82gfcbbfc2eca6e;7"
data "ExtraDescription" "hb90e7fe5g9771g40d3gbffcg91bcbcb61856;1"
data "TooltipAttackSave" "Intelligence"
data "TooltipStatusApply" "ApplyStatus(TAD_BLACK_HOLE_SLOW,100,1)"
data "CastSound" "Spell_Cast_Tadpole_BlackHole_L1to3"
data "TargetSound" "Spell_Impact_Tadpole_BlackHole_L1to3"
data "SpellAnimation" "f94542d9-a79c-478a-92de-573cead9260e,,;,,;24894b2d-ae8c-4bd3-8dab-d75a3c83c710,,;d5efa641-3b51-4824-a0bd-96ae047aeb19,,;bd339475-d2b5-46e8-8d0c-9f2ad6a91328,,;,,;7a28f440-1b0b-4a18-96a8-3767959b601a,,;,,;,,"
data "VerbalIntent" "Control"
data "HitAnimationType" "MagicalNonDamage"
data "SpellAnimationIntentType" "Peaceful"
data "TargetEffect" "becd29e0-0520-4842-b8d9-a1a46ac87ab9"
data "PositionEffect" "94280a3f-4d08-453d-be6a-1a3282d46db1"
data "Sheathing" "Sheathed"
```

Here we want the:

 `data "PositionEffect" "94280a3f-4d08-453d-be6a-1a3282d46db1"`
***
><h2><ins><bold>NOTICE</bold></ins></h2>
***
At this point you can choose to either simply use the UUID you found and put it in your own Effect spot, or you can dig deeper. If you chose **Dig Deeper**, Continuie reading:
***
><h1>Warning!!!</h1>
***
**Make sure you have <ins><bold>INDEXED</bold></ins> the files before proceeding.**
***

From here, you would want to use [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool) to index search the highlighted.



Again, we're using:

`data "PositionEffect" "94280a3f-4d08-453d-be6a-1a3282d46db1"`

With [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool)  open, click the Search Index button.

![IndexSearch](https://i.imgur.com/O4xqbYm.png)

A new window will pop up, with a search bar and some other buttons. Insert the UUID we selected into the Search Bar, and Click Search Files. For now, leave the selection options at All.

![IndexSearch2](https://i.imgur.com/NdJ9yeI.png)

With this particular effect, our search will pull up 2 results. The spell we pulled from, and the [**MultiEffectInfos**](#multieffectinfos).

![ConvertOpen](https://i.imgur.com/yBVQ6gE.png)

Now we've finally come to the point where we are going to talk about [**MultiEffectInfos**](#multieffectinfos). Brace yourselves, this is going to be a completely regular, non-fear inducing ride.

#### **File Structure**<!-- omit from toc -->
Before we move on, let's discuss File Structure for the status or spell you want to make shinier. For the next step, you'll want to save your new file as a <b>.txt</b> in the folder shown below. You can name this file whatever you want, as long as it is saved as a <b>.txt</b>.

![SpellFileStructure](https://i.imgur.com/DSwDgvN.png)

## **MultiEffectInfos**
Alrighty! Now we've reached the point of basic levels of crafting our own visual effects. MultiEffectInfos, or <b>MEI</b>'s for short! This particular step is an easy one, but it can throw you off if you're not prepared. There's Good news, great news and Bad news, sort of:

<h4>The Good News </h4>

If your goal is merely to mix and match previous effects without getting too complicated, this is the place to do it. The same can be said for the [**Root Templates**](#root-templates), but we'll discuss that later.
***
<h4>The Bad News </h4>
These effects can be very particular about the targetbone placements.

***
<h4>The Great News</h4>
I have already previously released a <b>MEI</b> guide on nexus, with a brief tutorial and templates for free use. You can find that here:

- [**MultiEffects Templates**](https://www.nexusmods.com/baldursgate3/mods/2408) by [**ImmortalRD**](https://www.nexusmods.com/baldursgate3/users/1601537)

***
Now that we have access to the <b>MEI</b>, we can see how they're set up. Since we were using Black Hole as our base earlier, you should have a file that looks like this

```
<?xml version="1.0" encoding="utf-8"?>
<save>
	<version major="4" minor="0" revision="9" build="320" lslib_meta="v1,bswap_guids" />
	<region id="MultiEffectInfos">
		<node id="MultiEffectInfos">
			<attribute id="UUID" type="guid" value="94280a3f-4d08-453d-be6a-1a3282d46db1" />
			<attribute id="Name" type="LSString" value="TAD_BlackHole_PositionEffect" />
			<children>
				<node id="EffectInfo">
					<attribute id="UUID" type="guid" value="00faf96a-b8d6-4335-8304-b38315dee369" />
					<attribute id="EffectResourceGuid" type="guid" value="dfa88d8b-b79a-27ca-2cc2-0f48830505e4" />
					<attribute id="DetachSource" type="bool" value="False" />
					<attribute id="DetachTarget" type="bool" value="True" />
					<attribute id="KeepRotation" type="bool" value="False" />
					<attribute id="UseOrientDirection" type="bool" value="False" />
					<attribute id="UseDistance" type="bool" value="False" />
					<attribute id="UseScaleOverride" type="bool" value="False" />
					<attribute id="KeepScale" type="bool" value="True" />
					<attribute id="MainHand" type="bool" value="False" />
					<attribute id="OffHand" type="bool" value="False" />
					<attribute id="MinDistance" type="float" value="0" />
					<attribute id="MaxDistance" type="float" value="0" />
					<attribute id="BindSourceTo" type="FixedString" value="SourceEntity" />
					<attribute id="BindTargetTo" type="FixedString" value="TargetEntity" />
					<attribute id="Pivot" type="FixedString" value="Target" />
					<attribute id="DamageType" type="uint32" value="0" />
					<attribute id="VerbalIntent" type="uint32" value="0" />
					<attribute id="StartTextKey" type="LSString" value="VFX_Cast_01" />
					<attribute id="Enabled" type="bool" value="True" />
				</node>
				<node id="EffectInfo">
					<attribute id="UUID" type="guid" value="f7492887-557d-4e49-a3c7-f4b8cf860b63" />
					<attribute id="EffectResourceGuid" type="guid" value="24161a33-9ef2-5220-79d8-4ac6c5fb4a14" />
					<attribute id="DetachSource" type="bool" value="False" />
					<attribute id="DetachTarget" type="bool" value="True" />
					<attribute id="KeepRotation" type="bool" value="False" />
					<attribute id="UseOrientDirection" type="bool" value="False" />
					<attribute id="UseDistance" type="bool" value="False" />
					<attribute id="UseScaleOverride" type="bool" value="False" />
					<attribute id="KeepScale" type="bool" value="True" />
					<attribute id="MainHand" type="bool" value="False" />
					<attribute id="OffHand" type="bool" value="False" />
					<attribute id="MinDistance" type="float" value="0" />
					<attribute id="MaxDistance" type="float" value="0" />
					<attribute id="BindSourceTo" type="FixedString" value="SourceEntity" />
					<attribute id="BindTargetTo" type="FixedString" value="TargetEntity" />
					<attribute id="Pivot" type="FixedString" value="Target" />
					<attribute id="DamageType" type="uint32" value="0" />
					<attribute id="VerbalIntent" type="uint32" value="0" />
					<attribute id="StartTextKey" type="LSString" value="VFX_Cast_03" />
					<attribute id="Enabled" type="bool" value="True" />
				</node>
			</children>
		</node>
	</region>
</save>
```
In the case of Black Hole, it has no targetbones to worry about, which probably isn't that helpful for the sake of this tutorial, but we'll get there in the end. The first thing you want to notice is that it is in <b>XML</b> format. This is a requirement if you want them to function. Another requirement, depending on the tool you use to pack your mod, is that they are saved as :

>[**lslib**](https://github.com/Norbyte/lslib/releases)

```
.lsf
```
This is because if you are packing your mod contents via [**lslib**](https://github.com/Norbyte/lslib/releases), you will need to manually pack all of your files.

or

>[**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool)
```
lsf.lsx
```
This is because if packing with [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool), it has a built in converter that when you pack the mod folder as a whole, it will automatically convert `lsf.lsx` to `.lsf`.

Now, before we discuss the `attribute id`s, I want to put out the top of the <b>MEI</b>. 
***
```
<?xml version="1.0" encoding="utf-8"?>
<save>
	<version major="4" minor="0" revision="9" build="320" lslib_meta="v1,bswap_guids" />
	<region id="MultiEffectInfos">
		<node id="MultiEffectInfos">
```
***
The first line `<?xml version="1.0" encoding="utf-8"?>` defines to the text editor the language used for the form.

The second line `<save>` is the opening block of any <b>XML</b>, followed by the `<version major="4" minor="0" revision="9" build="320" lslib_meta="v1,bswap_guids" />`. The numbers in the *major*, *minor*, *revision*, and *build* aren't important, as long as the *major* is 1 or higher.

The next line `<region id="MultiEffectInfos">` is our region id. This tells the game what the entire block will focus on. Unlike [**_merged**](#merged-files) files, you won't see a region id besides `MultiEffectInfos`. The same will apply to the `<node id="MultiEffectInfos">`. 

Let's take a look at the attribute ids and define, to the best of my ability, what they mean and do. Our first culprit is:



Our first Attribute ID
`<attribute id="UUID" type="guid" value="94280a3f-4d08-453d-be6a-1a3282d46db1" />`
is the unique identifier. That's the one you'd find in the Spell attributes such as `data "PositionEffect" "94280a3f-4d08-453d-be6a-1a3282d46db1"` for a spell. If you want to add or make any changes to this, first you will need to change this value to a new, unique UUID, which will later be put in that same, aforementioned effect data. The most simple way to do so is to use [**BG3-Modders-Multitool**](https://github.com/ShinyHobo/BG3-Modders-Multitool) to generate a new, unique UUID, by clicking the Generate button, as such:

![GenerateUUID](https://i.imgur.com/rSV48PF.png)

Make sure the Handle Checkbox is unchecked, like so:

![GenerateUUIDNoHandle](https://i.imgur.com/N4WIwD5.png)

After you have clicked Generate, it should look something like this, only with a different UUID:

![GenerateUUID2](https://i.imgur.com/ZJdqrop.png)

Once you have your new UUID, you will replace the value attribute:

From

`<attribute id="UUID" type="guid" value="94280a3f-4d08-453d-be6a-1a3282d46db1" />`

To

`<attribute id="UUID" type="guid" value="186d5709-de2a-4738-9b08-30065f17800e" />`

Only with your new UUID instead of this one specifically. You may then feel free to change the value of `<attribute id="Name" type="LSString" value="TAD_BlackHole_PositionEffect" />` to whatever you want.

Your next step will be to take the UUID of the `<node id="EffectComponent">` found here:

`<attribute id="UUID" type="guid" value="00faf96a-b8d6-4335-8304-b38315dee369" />`

and repeat the same steps as you did with the master UUID for the <b>MEI</b>.
***
><h1><b>WARNING!!!</b></h1>
>Do not replace the UUID in the <b>EffectResourceGUID</b> just yet.
***
 
 The first thing to note about the attribute id's inside the `EffectInfo` are mostly `bool`(ean) values, which mean True or False. Also note, that the bool values are in relation to whatever they are attached to. So an effect, say, normally meant for the Root (or Caster Base), that gets attached to the CastFX (Often depicted as a spell casting animation before the spell trigger.), might need different boolean sets.
 The attribute IDs `DetachSource` and `DetachTarget` are generally for determining if an effect remains attached to a specific `TargetBone`. We will get into `TargetBone` in a moment.  

The next attribute id we'll look at is `KeepRotation`. For effects that are not intended to be attached to specific things, you will want this set to `True`. At least, if you don't want a specific effect rotating around every time your character moves, this tells the game to let the lsfx stick to it's initial rotation patterns.

Following up, we have `UseOrientDirection`. This attribute is in relation to A) The direction your character is facing, and B) The direction the lsfx has defined for the effect components. More on that later.

The attribute ids `UseDistance` and `UseScaleOverride` are referencing specialized nodes inside the lsfx. The id `UseDistance` determines effects changes by distance travelled, and the id `UseScaleOverride` is for the size change in relation to `UseDistance` scale settings, inside the lsfx.

One of the more important attribute ids is `KeepScale.` This tells the game to maintain the scale to the attached `TargetBone` in relation to the <b>MEI</b> and the lsfx.

The following attributes should often be left as is:
***
```
<attribute id="MainHand" type="bool" value="False" />
<attribute id="OffHand" type="bool" value="False" />
<attribute id="MinDistance" type="float" value="0" />
<attribute id="MaxDistance" type="float" value="0" />
<attribute id="BindSourceTo" type="FixedString" value="SourceEntity" />
<attribute id="BindTargetTo" type="FixedString" value="TargetEntity" />
<attribute id="DamageType" type="uint32" value="0" />
<attribute id="VerbalIntent" type="uint32" value="0" />
```
***

Furthuremore, the attribute id `Pivot` is associated with whether or not something is a Beam Effect. This should generally be set to `Target` unless the effect is a direct beam, such as Lightning Bolt or SunBeam.

One of the more unique attribute ids is `StartTextKey`. It's interesting for a variety of reasons. To start, it's the only attribute id besides the <b>MEI</b> name that has a variety of values it could be. Not every `EffectInfo` will have one of these. The purpose of this id is to ***schedule*** a trigger time. So, if you want one effect to play after another, rather than at the same time in a Prepare effect, you might place the value at `"VFX_Prepare_01"`. This would tell the effect with this `StartTextKey` to trigger after the first effect triggers, giving a chain reaction effect. There are a lot of `StartTextKey` values, and I encourage you to look through the various <b>MEI</b>'s to find ones that might fit your needs for an effect chain.

The next attribute id is `Enabled`. It's fairly self explanatory. If set to false, that `EffectInfo` will not trigger at all. This is only really useful if you are attempting to test the visuals if individual `EffectInfos` without deleting an entire block.

The FINAL attribute id we'll discuss is the `EffectResourceGuid`. Without this, the `EffectInfo` is useless. You will find these `EffectResourceGuid`s in an /Assets/Effects/`-merged` VisualBanks section. With this, you can browse to your hearts content, experimenting with different VFX uuids.
***
><h4><b>Notice!!!</b></h4>
Not all VFX will work simply by placing the UUID into the `EffectResourceGuid`. Also, some will not work for the `TargetBone` they are attached to.
***

Now, you've seen me repeatedly mention `TargetBone` without any reference. Well, it's time I cleared that up. To begin, as their name suggests, they are what an `EffectInfo` is attached to. They usually look something similar to this:
***
```
<node id="EffectInfo">
	<attribute id="BindSourceTo" type="FixedString" value="SourceEntity" />
	<attribute id="BindTargetTo" type="FixedString" value="TargetEntity" />
	<attribute id="DetachSource" type="bool" value="False" />
	<attribute id="DetachTarget" type="bool" value="False" />
	<attribute id="EffectResourceGuid" type="guid" value="50678fd2-db36-ee2e-89a8-672f88985f52" />
	<attribute id="Enabled" type="bool" value="True" />
	<attribute id="KeepRotation" type="bool" value="False" />
	<attribute id="KeepScale" type="bool" value="False" />
	<attribute id="MainHand" type="bool" value="False" />
	<attribute id="MaxDistance" type="float" value="0" />
	<attribute id="MinDistance" type="float" value="0" />
	<attribute id="OffHand" type="bool" value="False" />
	<attribute id="Pivot" type="FixedString" value="Target" />
	<attribute id="UUID" type="guid" value="a0d59380-583d-4f20-8b7c-83cae56b14b9" />
	<attribute id="UseDistance" type="bool" value="False" />
	<attribute id="UseOrientDirection" type="bool" value="False" />
	<attribute id="UseScaleOverride" type="bool" value="False" />
	<children>
		<node id="TargetBone">
			<attribute id="Value" type="LSString" value="Dummy_OverheadFX" />
		</node>
	</children>
</node>
```
***
As you can see, there is a new bit of information called `<node id="TargetBone">` followed by `<attribute id="Value" type="LSString" value="Dummy_OverheadFX" />`. In this case, the visual effect would be attached just over the head.

There are a large quantity of `TargetBones` to choose from, giving you endless possibilities when creating visual effects. There is also a node id called `SourceBouune`, but this is exclusively for an effect that departs its source, in a sense. Usually projectiles and beams count here. In some cases, you'll also come across this:
***
```
<children>
	<node id="TargetBone">
		<attribute id="Value" type="LSString" value="Dummy_EyeFX_01" />
	</node>
    <node id="TargetSkeletonSlot">
        <attributeid="Value" type="LSString" value="1">
    </node>>
</children>
```
***

This particular node ID is generally reserved for Eye sockets, and other special occasions. Some commonly used `TargetBones` and their locations are listed below:
-   Dummy_CastFX: Just in Front of the Character
-   Dummy_BodyFX: The whole body
-   Dummy_Root: The base of the character, or ground.
-   Dummy_FX: The Weapon.

There are many more, too many to list here, even. Again, I encourage you to explore those <b>MEI</b>'s and find those effects that suit you.

#### <ins><b>Folder Structure</b></ins>   <!-- omit from toc -->

The Folder structure you want for your <b>MEI</b>s is as follows:

![MEIFolderStructure](https://i.imgur.com/GpCwUJP.png)

Now, as we have learned <b>MEI</b>'s can do a lot, and lead to a lot interesting results. However, they are limited in that there are a few things they cannot do, at least not effectively. That's where [Root Templates](#root-templates) come in.

## **Root Templates**
Root Templates, while similar to [MultiEffectInfos](#multieffectinfos) in many ways, they are also quite different. While an <b>MEI</b> exclusively handles visual effects, a `RootTemplate` handles visual effects, sounds, and a wide variety of other things. You can find `RootTemplates` as Items, `SpellAnimations`, `Trajectories` and more. In this particular section we will be covering `Trajectories`.

#### <ins><b>Folder Structure</b></ins>   <!-- omit from toc -->

The Folder structure you want for your `RootTemplate` is as follows:

![MEIFolderStructure](https://i.imgur.com/bhGCIlx.png)


## **Merged Files**
## **LSFX Files**
## **Hot Testing**
## **Advanced Tips**
## **Useful Resources**
## **Summary**
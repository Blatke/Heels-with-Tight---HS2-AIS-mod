# Heels-with-Tight---HS2-AIS-mod
This is a shoe mod for Honey Select 2/AI-Shoujo.

![AI_2024-05-03-15-50-55-694](https://github.com/Blatke/Heels-with-Tight---HS2-AIS-mod/assets/125734582/181db1ce-c188-4af0-b289-a16e5998a77f)

## Content
1. Heels with Tight
2. Heels with Tight MultiMask

## Installation
Check the latest version on the [Release](https://github.com/Blatke/Heels-with-Tight---HS2-AIS-mod/releases) page and download the mod file. Put the .zipmod file into directory **/mods/** .

In Chara Maker mode, go to Outfit panel, add Shoes to the chara, and search for "**blake**", "**heels**" or "**tight**" in the selection box to find it. 
Then, add it to the shoes.

Use MaterialEditor to adjust its main and emission colors, glossiness, metallic values as well as the main texture and normal maps.

For the maps, the transparent (alpha channel) part on the texture will be culled to appear the chara's body.

## In StudioNeo
When playing with the chara wearing Heels with Tight in StudioNeo, if some poses result in clipping between the chara and the tight, you can select the chara and enable its adv.mode of HS2PE/AIPE, go with Blend Shapes tab, choose the **Tight** block, and then, drag the slider of the **Fatter** to make the tight fatter till it doesn't clip with the chara.

Another way to avoid clipping is to turn OFF this option to disbale the renderer of the chara's body, so the body will not be rendered.
![image](https://github.com/Blatke/Heels-with-Tight---HS2-AIS-mod/assets/125734582/b26468de-6dbd-4549-89cf-3f0cb8439ebb)

Also, there is a **Smoothness** block on Blend Shapes tab. It helps when the toes is rotated and let the heads of the heels not be smooth.

## UV Template
Here is the UV map of this mod as a template for you to draw patterns on it.

![Heels with Tight](https://github.com/user-attachments/assets/43fcb2c4-b145-4e0c-bea0-4bd13e7a88ee)

## For MultiMask
On Nov.2, 2024, there was a significant update in which the mod was added with two normal maps that made some folds on the tight. If you don't need them, just adjust the intensities of Normal and DetailNormal to 0 on MaterialEditor tab.

Also, it added with a new pair of shoes namely **Heels with Tight MultiMask**, which had the same mesh as the earlier one, but used a different shader, **[Blake/Multi-Masks](https://github.com/Blatke/Multi-Mask-Shader-for-ME)**. You need to go to the shader's [release page](https://github.com/Blatke/Multi-Mask-Shader-for-ME/releases) to download the mod file for the latest version to put it into your **/mods/** folder and thus it lets MaterialEditor show the shader's properties, then you can adjust their values by yourself.

Check the **demonstration video**: https://youtu.be/v_ogmAXFKD8. The shader the new shoes are using uses RGB images as normal masks to decide which parts of the normal map to show or hide the bump effect.

I made 3 normal masks namely normalMask1, normalMask2 and normalMask3. You can check the following figures to know which parts these masks are referring to and affect:



## Me
My discord server: https://discord.gg/nc5pmnf8X3

My Tencent QQ Chatgroup for modders: 904857543

My front page: http://www.blatke.cc

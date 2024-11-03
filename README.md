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

In Studio, go to the adv.mode of HS2PE/AIPE, then choose Blend Shapes, and click the **Tight** block, adjust its blendshape values if there's a need for making the tight a little fatter to prevent clipping into the body, or demand for smoothen the bottoms of the heels.

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
### Normal Maps and Normal Masks
On Nov.2, 2024, there was a significant update in which the mod was added with two normal maps that made some folds on the tight. If you don't need them, just adjust the intensities of Normal and DetailNormal to 0 on MaterialEditor tab.

When intensity of Normal and DetailNormal is 1.0:

![AI_2024-11-02-00-10-42-056](https://github.com/user-attachments/assets/b8c26115-565b-4a93-b90b-5fb1ec920f8b)

When DetailNormal is 0 with Normal remaining 1.0:

![AI_2024-11-02-00-10-35-937](https://github.com/user-attachments/assets/4c681881-927a-4904-b581-d80f10fadb52)


Also, it added with a new pair of shoes namely **Heels with Tight MultiMask**, which had the same mesh as the earlier one, but used a different shader, **[Blake/Multi-Masks](https://github.com/Blatke/Multi-Mask-Shader-for-ME)**. You need to go to the shader's [release page](https://github.com/Blatke/Multi-Mask-Shader-for-ME/releases) to download the mod file for the latest version to put it into your **/mods/** folder and thus it lets MaterialEditor show the shader's properties, then you can adjust their values by yourself.

Check the **demonstration video**: https://youtu.be/v_ogmAXFKD8. The shader the new shoes are using uses RGB images as normal masks to decide which parts of the normal map to show or hide the bump effect.

I made 3 normal masks namely **normalMask1, normalMask2 and normalMask3**. You can check the following figures to know which parts these masks are referring to and affect. For instance, if you want to hide the folds on the character's left shoulder that was painted blue on normalMask1, you need to find the property of _NormalMask1_Blue_ to adjust its value. 

![AI_2024-11-02-21-00-28-355](https://github.com/user-attachments/assets/7c681293-a5ea-45df-a58a-38fe52251a41)

![AI_2024-11-02-21-01-03-299](https://github.com/user-attachments/assets/d0492814-d07c-4efc-868d-2fff50f687fe)

![AI_2024-11-02-21-01-36-567](https://github.com/user-attachments/assets/763cc4bc-d760-4a01-83a9-4ba7a85c765a)

![AI_2024-11-02-21-01-53-808](https://github.com/user-attachments/assets/7833cacc-7de0-4a4b-bb13-3aa9d3cacfbc)

![AI_2024-11-02-21-02-32-801](https://github.com/user-attachments/assets/a6dae683-2d76-4809-ae4f-f585d3a77674)

![AI_2024-11-02-21-02-45-885](https://github.com/user-attachments/assets/a9c20260-2bac-49a3-99c0-e27ff0cf7610)

#### Use Custom Normal Masks
You can draw your own masks and replace the original mask textures on MaterialEditor if you want to. 
1. You can use Red, Green, Blue, Cyan, Purple, Yellow and White colors to paint your normal mask textures, thus you can have at least 7 different parts to independently affect the display of bump effect.
2. Black color means no bump effect should be shown.
3. It suggests making gradient color between one of those mask colors and black color in order to reduce the hard edges between the bump parts and no bump ones. Such like Red(1,0,0) color, you can make the gradient colors from (0,0,0) to (1,0,0) or something like this.
4. It suggests .png format for the mask image instead of .jpg to prevent Moire patterns or color deviation interfering the mask's performance.
5. If more than one masks refer to the same one part of the normal map that means the parts indicated by masks are overlapped, each of the masks will exert the same influence on it, but the total influence will not be greater than the intensity of normal map strength.

### Color Masks
In the update on Nov.2, 2024, with adopting **[Blake/Multi-Masks](https://github.com/Blatke/Multi-Mask-Shader-for-ME)**, the function of color masks was introduced. Color masks are used to affect the colors on the Albedo texture (main texture) as well as the tint by indicating which part to paint what color. Let us say if using a RGB flag as a color mask, there are Red (1,0,0), Green (0,1,0) and Blue (0,0,1) colors. We import it into **Albedo Mask 1** on MaterialEditor tab, and adjust the colors for Mask1_Red, Mask1_Green and Mask1_Blue to any colors, then the parts of the material overlapping with those parts in these three colors are changed.

For **Albedo Mask 2**, the options with the names starting with "**Mask2_**" can manipulate. But note that **Albedo Mask 1** is to **blend** color with the Albedo texture and tint color, whereas **Albedo Mask 2** is to **replace** the color with a designated one.

In addition, **Albedo Mask 2** supports emission. You can adjust the values in Mask2_Red_Emission or some other options like this to strenghen the light intensity on the corresponding parts indicated by this color mask.

You can check the demonstration video: https://youtu.be/-1iLz9M2pEI

#### Use Custom Color Masks
The images using as color masks should be:
1. Including the patterns in at least one of Red, Green, Blue, Cyan, Purple, Yellow and White colors, and the gradient colors between one of them and black color such like the colors from (0,0,0) to (1,0,0).
2. All the parts in black color means no effect exerted by the color mask, so Tint Color and Albedo texture have the total control.
3. It suggests .png format for the mask image instead of .jpg to prevent Moire patterns or color deviation interfering the mask's performance.

## Me
My discord server: https://discord.gg/nc5pmnf8X3

My Tencent QQ Chatgroup for modders: 904857543

My front page: http://www.blatke.cc

# VFSKeyboard
###### tags: VFSKeyboard, ReadMe, Unity Asset, VR, Unity, SHING MING STUDIO

### **:tiger: VR, Fast and Simple :cat:**

VFSKeyboard is an open-source keyboard, as its name, suitable for VR development environment, fast and simple to use.



| Supported Engine                  | Unity                                                                                                                                                                                                                         |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Supported  Version                | 2019.4.14f1 +                                                                                                                                                                                                                 |
| Download Source                   | Unity Asset Store                                                                                                                                                                                                             |
| Download Link (Click the picture) | [![Asset_store_2](https://github.com/SHING-MING-STUDIO/VFSKeyboard/assets/65477270/c7535386-2da8-4971-a06c-9f5f48118994)](https://assetstore.unity.com/packages/tools/input-management/vfskeyboard-vr-fast-and-simple-198320) | 


## FEATURES
![](https://i.imgur.com/DXDvLVN.png)
- Autofill to the corresponding inputField which is the last time select by user
- Cross-platform building by Oculus Integration, SteamVR Plugin, Unity XR Interaction Toolkit
- "One seconds" setup
- Easy-to-use
- Auto enable/disable the virtual keyboard when trigger/untrigger* the “InputField” UI component
- Customize the keyboard button color when the user release, select, and press

*Untrigger means the VR controller (or laser pointer) leave to point the keyboard area for about 3 seconds (default setting)


## FAST INSTALLATION
1. [important] **Make sure that your VR controller (or laser pointer) can interact with the UI component (e.g. click the button) in the scene first before using this asset**
2. Add the “InputField” gameObject and then add the “InputFieldDetection” script at this gameObject
3. Add the “Virtual Keyboard Controller” prefab in the scene
4. Drag the “Virtual Keyboard” prefab to the Canvas UI gameObject, become the childObject of the Canvas UI gameObject
5. Fine-tuning the UI component to a suitable position, and now you can play it now :)

**p.s. In our unitypackage, our example scene is made by Unity XR Interaction Toolkit framework and using the Oculus Quest 2 for our testing. Install the Unity XR Interaction Toolkit framework and double-click the example scene to try it out!**

## INSTALLATION IN DETAILS

### Step 1 - Set Up your VR development environment
1. According to the VR device you are using and you're expected to develop the VR framework, install the corresponding package and plugin. As our example, we first open the **Package Manager**, and then click **Advanced button**, select **Show preview packages**
2. Search XR Interaction Toolkit and then install it
3. Go to **Edit -> Project Setting -> XR Plug-in Management -> install XR Plug-in Management**
4. Select the corresponding **Plug-in Providers** which match your VR device. In our example, we select **Oculus**, and then it will automatically install Oculus XR Plugin

### Step 2 - Set Up the VR controller (or laser pointer) that can interact with the UI component in the scene

5. For how to make the VR controller (or laser pointer), pls check out this ReadMe session: **The Details of the Demo - Building the laser pointer**

### Step 3 - Download and import VFSKeyboard packages

***The part that our components are responsible for***


6. Download and import **"VFSKeyboard"**
7. Add two "**InputField**" gameObject in the scene and then add the "**InputFieldDetection**" script at those gameObject. This script is mainly responsible for sending the signal that opens the "Virtual Keyboard" when the laser pointer click the InputField gameObject
![](https://i.imgur.com/6WgLvyd.png)
8. Add the **"Virtual Keyboard Controller"** prefab in the scene. This gamObject mainly control the "Virtual Keyboard" open or not
![](https://i.imgur.com/Uh74bcK.png)
9. Drag the "**Virtual Keyboard**" prefab to the **Canvas** UI gameObject, become the childObject of the **Canvas** UI gameObject
![](https://i.imgur.com/U8Q4e1C.png)
10. Fine-tuning the UI component to a suitable position, and now you can play it now :)

### Step 4 - Fine-tuning the VFSKeyboard setting(Optional)
Ther have some setting that let you modify such customize the keyboard button color when the user release, select, and press and the automatically closing time of the Virtual Keyboard

11. You can set the automatically closing time of the Virtual Keyboard of what you want. This setting is in the gameObject path, "Virtual Keyboard/Background"
![](https://i.imgur.com/TuV9Sa5.png)


13. For color setting of the Virtual Keyboard button, you can select the gameObject that path is "Virtual Keyboard/Background/{row1, row2, row3...}/{A, B, C, D, E...}", then modify the "GetKeyCode" script parameter {mNormalColor, mHoverColor, mDownColor}
![](https://i.imgur.com/q1hhvDr.png)


### KNOW ISSUE / IMPROVEMENT
- Can’t get the cursor (or laser pointer) position (in characters) within a text InputField if the project using Oculus Integration and XR Interaction Toolkit to develop
- Add more punctuation key to the keyboard in the future

## Demo - Try it out!
Demo builds from the different framework and using the Oculus Quest 2 for testing are available here

0. The Unity Project File
    - [Download link](https://drive.google.com/drive/folders/1uwvCfkKxcsQLHnR7yxN_agglMzws_VGH?usp=sharing)

1. Building by Oculus Integration:
    - [Running on Windows Platform(.exe) and using Oculus Link to play](https://drive.google.com/file/d/1qNCtgYQCs5Hp4kmA-vJRxou2Seip9uR7/view?usp=sharing)
    - [Running on Oculus(.apk)](https://drive.google.com/file/d/1TC3xcVgx_XekGe3--sP2T2XJVGaFGCN6/view?usp=sharing)
2. Building by SteamVR Plugin:
    - [Running on Windows Platform(.exe) and using Oculus Link to play](https://drive.google.com/file/d/1514QedY8KkCONoppiGpdPEpUtvpRq8m8/view?usp=sharing)
3. Building by Unity XR Interaction Toolkit
    - [Running on Windows Platform(.exe) and using Oculus Link to play](https://drive.google.com/file/d/1BcC3yIbShIFdgT4LKN52LiDIWnmS_Fiy/view?usp=sharing)
    - [Running on Oculus(.apk)](https://drive.google.com/file/d/1u5RlT1aHP_sHOmgy2BXEB8WEcZV9K8H1/view?usp=sharing)
4. General input(Physical Mouse) **(Not VR Development)**
    - [Running on Windows Platform(.exe)](https://drive.google.com/file/d/1cuLwexPr7ex6HyXI2xx0yibXqXS_9C4z/view?usp=sharing)

||Building by Oculus Integration | Building by SteamVR Plugin | Building by XR Interaction Toolkit |General input (by Physical Mouse)|
| ------------------ | ------------------ | -------------- | ---------------------- |----------------------|
| Running on Windows | V                  | V              | V                      |V|
| Running on Android(Oculus)       | V                  |               | V                      ||
| Having a know issue  | V                  |               | V                      ||
| Version | 29.0                  | v2.7.3 (sdk 1.14.15)   | 0.10.0-preview.7                     |N/A|
| *Press the keyboard key by  | 1 or 2                  |     3          | 3                      |Physical Mouse|


***In the Demo, we set some button events on Oculus Controller to trigger the event when the button is down such as press the keyboard key**

![](https://i.imgur.com/pbWRrK3.png)

## The Details of the Demo - Building the laser pointer
The above Demo follows the following tutorial to set the laser pointer that can interact with the UI component in the scene and then add VFSKeyboard to interact InputField and Virtual Keyboard components

1. Making the laser pointer with **Oculus Integration**
https://www.youtube.com/watch?v=8fT478uopco

2. Making the laser pointer with **SteamVR Plugin**:
(I). https://www.youtube.com/watch?v=3mRI1hu9Y3w&t=314s
(II). https://www.youtube.com/watch?v=h_BMXDWv10I
(III). https://www.youtube.com/watch?v=vNqHRD4sqPc&t=881s

3. Making the laser pointer with **Unity XR Interaction Toolkit**
https://www.youtube.com/watch?v=BZt74PVb7sM

## Update History
- v1.0 Jun 22, 2021: First release

## **:bug: Issue report :spider:**
If you encounter any software issues, please feel free to report via this [link](https://github.com/SHING-MING-STUDIO/VFSKeyboard/issues). Thank you.

## **:tiger: About Author / Contact Information :dog2:**
- Web - https://shingming.co/
- Mail - shingming.cs@icloud.com
- Donation

[![paypal](https://hackmd.io/_uploads/S16qytwCp.png)](https://www.paypal.com/paypalme/ShingMing)

## LICENSE
MIT License
Create by Wong, Shing Ming

# Huawei Matebook 14s - TigerLake (i7-11370H) Hackintosh

## 2026 Update
This repository is part of the Hackintosh community's efforts to achieve full acceleration for Intel Gen 11+ processors.
Previously, this repository followed the InsanelyMac thread, which was inactive for a while.

New projects emerged attempting to achieve full acceleration using their own methods, such as [AppleIntelTGLDriver](https://github.com/pawan295/Appleinteltgldriver.kext) of pawan295. However, a new project, [NootedGreen](https://github.com/sgiammori/NootedGreen), was recently launched, which is the predecessor to NootedBlue.

You can check the NootedGreen InsanelyMac thread [here](https://www.insanelymac.com/forum/topic/362634-nootedgreenkext-is-on-air-85-complete/).

## IMPORTANT
The **Intel Iris Xe iGPU (Tiger Lake)** is **not officially supported by macOS**.
Although partial workarounds exist, **hardware acceleration is not stable or reliable**.  
For this reason, **this setup is not recommended for daily use**. **Consider this repository as an experimental resource only**.

## Experimental Project
Although the EFI provides a bootable environment and allows macOS to be installed, **it is not recommended to use this installation as your daily operating system**, in fact, it's nearly impossible due to the lack of graphics acceleration.

This repository is experimental and provides an EFI ready for installing macOS and testing different methods for graphics acceleration using projects like NootedGreen.

## Repository Structure
#### Main EFI Folder (Installation & Recovery)
The primary EFI folder is designed as a baseline configuration:

- **Vesa Mode:** Configured for a minimal boot in VESA mode. This ensures UI visibility without hardware acceleration, providing a stable environment for the initial macOS installation.
- **Installation Workflow:** Graphics acceleration attempts **should only be performed post-installation.** The provided EFI is intended to facilitate the OS installation process first.

#### EXP EFI Folder (Only for NootedGreen + Hookcase + Bundles and kexts in /L/E)
This EFI is exclusively for use with everything NootedGreen specifies. It is configured for use with TGL, therefore:

- Hookcase is compiled with ```
uint32_t registerValue = callback->readReg32(0x44470);
```
to load TGL.

- AppleIntelTGLGraphics and AppleIntelTGLGraphicsFramebuffer have ``` IOPCIPrimaryMatch: 0x9A498086 ``` to work with TGL. 

- It should only be used after post-installation, with csrutil disabled, Apple* bundles and kext in /L/E, and Hookcase in /L/E/ Don't forget to apply the permissions to Apple* and Hookcase.

More details in [NootedGreen Repository](https://github.com/sgiammori/NootedGreen).

With all that ready, you should be able to boot with NootedGreen, Hookcase, and AppleIntelTGLGraphics/Framebuffer.kext loaded.

![](media/Screenshot%202026-04-27%20at%206.00.26%E2%80%AFAM.png)

**If you have boot problems, delete AirportItlwm.kext from /OC/Kexts/ and OC Snapshot in the config.plist.**


## Working
- [x] Touchpad ELAN2605
- [x] Intel WI-FI 6 AX201
- [x] FN Keys
- [x] USB 3.x
- [x] USB C Thunderbolt

## Not Working
- [ ] Intel Iris Xe Graphics (3D Acceleration)
- [ ] Sound (Conexant CX8070 Speaker) but recognized.
- [ ] Internal Microphone (Not tested)
- [ ] Brightness (Backlight)
- [ ] Intel AX201 Bluetooth - Disabled 

## References

- [Samsung-NT750XDA-KF59U Hackintosh by lshbluesky (GitHub)](https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh)  
- [InsanelyMac - Iris Xe iGPU on Tiger Lake thread](https://www.insanelymac.com/forum/topic/358305-80-solved-iris-xe-igpu-on-tiger-lake-successfully-loaded-icllp-frambuffer-and-vram-also-recognizes-1536mb-however-some-issues/)
- [NootedGreen Repository](https://github.com/sgiammori/NootedGreen)
- [NootedGreen InsanelyMac Thread](https://www.insanelymac.com/forum/topic/362634-nootedgreenkext-is-on-air-85-complete/)

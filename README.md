### Huawei Matebook 14s - TigerLake (i7-11370H) Hackintosh

## ⚠️ IMPORTANT NOTICE
The **Intel Iris Xe iGPU (Tiger Lake)** is **not officially supported by macOS**.
Although partial workarounds exist, **hardware acceleration is not stable or reliable**.
For this reason, this setup is **not recommended for dialy use**.
Consider this repostory as an educational and experimental resource only.

## 🚧 Experimental Project
This Hackintosh build is part of ongoing community efforts to enable Tiger Lake iGPU support.
Especially the [InsanelyMac Tiger Lake iGPU thread](https://www.insanelymac.com/forum/topic/358305-80-solved-iris-xe-igpu-on-tiger-lake-successfully-loaded-icllp-frambuffer-and-vram-also-recognizes-1536mb-however-some-issues/).
Although that forum thread has not shown recent activity, this project would not exist without the community’s contributions.

The documentation here reflects **my own experimentation and testing** on the Huawei Matebook 14s, with the goal of recording possible improvements and sharing results in an organized way.

## 📌 Current Status
- [x] macOS installation from USB  
- [x] OpenCore boot from USB  
- [ ] Boot from internal disk (in progress due)  
- [ ] Intel Iris Xe acceleration (unsupported, experimental)  
- [x] Touchpad functional with VoodooI2C (patched Info.plist)  
- [ ] Audio configuration (work in progress)  

## Working
- [x] Touchpad ELAN2605
- [x] Intel WI-FI 6 AX201
- [x] FN Keys
- [x] USB 3.x
- [x] USB C Thunderbolt

## Not Working
- [ ] Intel Iris Xe Graphics (3D Acceleration)
- [ ] Sound (Conexant CX8070 Speaker)
- [ ] Internal Microphone (Not tested)
- [ ] Brightness
- [ ] Intel AX201 Bluetooth

## 🙏 Acknowledgments / References
This project would not be possible without the work and research shared by the Hackintosh community:

- [Samsung-NT750XDA-KF59U Hackintosh by lshbluesky (GitHub)](https://github.com/lshbluesky/Samsung-NT750XDA-KF59U-Hackintosh)  
- [InsanelyMac - Iris Xe iGPU on Tiger Lake thread](https://www.insanelymac.com/forum/topic/358305-80-solved-iris-xe-igpu-on-tiger-lake-successfully-loaded-icllp-frambuffer-and-vram-also-recognizes-1536mb-however-some-issues/)

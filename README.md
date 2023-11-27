# This a simple instuctions list for Hackintosh.
----------------

**Ok, let's hack!**

## Prerequisites or Tools
----------------

- [OpenCore](https://github.com/acidanthera/OpenCorePkg)
  - [OC Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
  - [Post Install](https://dortania.github.io/OpenCore-Post-Install/)
  - [ACPI Things](https://dortania.github.io/Getting-Started-With-ACPI/#a-quick-explainer-on-acpi)

- [Configurators](https://github.com/ic005k/OCAuxiliaryTools)
  - [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools)
  - [OC Configurator](https://mackie100projects.altervista.org/download-opencore-configurator/), only for MacOS.
  - [ProperTree](https://github.com/corpnewt/ProperTree)

- [Installer Flasher](https://etcher.balena.io/)
  - [BalenaEtcher](https://etcher.balena.io/)
  - [Rufus](https://github.com/pbatard/rufus)
  - [Ventoy](https://github.com/ventoy/Ventoy), which doesn't support darwin directly.

- [IASL Tools](https://github.com/ic005k/Xiasl), in case you need to compile your modified ACPI files for hot patching.
  - [For Windows](https://www.intel.com/content/www/us/en/developer/topic-technology/open/acpica/download.html)
  - [For MacOS](https://github.com/HelllGuest/acpica-tools-macos)
  - [For win/mac/linux](https://github.com/ic005k/Xiasl), with GUI, can save/edit/compile/decompile ACPI files.

- [USBToolBox](https://github.com/USBToolBox/tool), If you have USB 3.0, you will need this.

- [SSDTTime](https://github.com/corpnewt/SSDTTime), which helps you to collect your own SSDT files.

- [HackinTool](https://github.com/benbaker76/Hackintool)

## Some guides for kexts/ssdt collection
-----------------

- [Gathering files](https://dortania.github.io/OpenCore-Install-Guide/ktext.html)
- [国光](https://apple.sqlsec.com/3-%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C/3-3/)
- [Noot](https://chefkissinc.github.io/guide/gathering-files/kexts), with AMD laptops supported.
- [NootedRed](https://chefkissinc.github.io/nred), for AMD iGPU.
- [GenericUSBXHCI for Ryzen](https://github.com/RattletraPM/GUX-RyzenXHCIFix), makes your trackpad work properly on Ryzen platform.
- [AMD GPU sensor](https://github.com/ChefKissInc/RadeonSensor)
- [AMD GPU Spoof](https://dortania.github.io/Getting-Started-With-ACPI/Universal/spoof.html), you may need this for Faking AMD GPU ID.
- [Get RX550 with lexa cores to work](https://www.youtube.com/watch?v=xb5yKRhOtp0)
  - [issue_264](https://github.com/dortania/bugtracker/issues/264)
  - [issue_129](https://github.com/dortania/bugtracker/issues/129)
- [How to adjust PowerPlayTable for AMD GPU](https://www.reddit.com/r/hackintosh/comments/hg56pv/guide_polaris_rx_560_580_etc_custom_powerplay/)
  - [video](https://www.bilibili.com/video/BV1ZT4y1v7Ac/?spm_id_from=333.337.search-card.all.click&vd_source=1835c845bf533ce47c2b4d33db3419b5)
- [各种kext的功能列表](https://macoshome.com/hackintosh/hcourse/7656.html)

## Special workarouds for Ryzentosh
------------------

- [Docker workaround for Ryzentosh 1](https://gist.github.com/sergeycherepanov/cbe82132b2064cc62b16793b6c61e6c8)
- [Docker workaround for Ryzentosh 2](https://gist.github.com/slykar/e92732be9bf81a71e08068245656d70e)
- [VSCode/Chrome/Chromium-based workaroud for Ryzentosh](https://chefkissinc.github.io/nred#chrome-chromium-based-browsers-and-apps-like-sublime-text-cause-graphical-artefacts-amongst-other-problems)
- [Wechat/QQ workaroud for Ryzentosh](https://pan.xunlei.com/s/VNhkaG568VndHC4GhWdbW0nhA1?pwd=ng2g#)
- [Android simulator workaroud suggestions](https://github.com/allansrc/AMD-OSX-Ryzentosh-B350)

## My examples
------------------

1. iMac Ventura
    - Hardwares:
      - Motherboard: B360
      - CPU: i5-10400F
      - GPU: RX560
      - RAM: 32G
    - Status:
      - Just works fine.
    - EFI
     - [Download](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Ventura_RX560_P310S/OC_P310S.zip).

![Hackintosh1](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Ventura_RX560_P310S/iMac_RX560_32G.png)
1. iMac Monterey
   - Hardwares:
     - Motherboard: B360
     - CPU: i5-10400F
     - GPU: RX550(lexa)
     - RAM: 16G
   - Status:
     - Just works fine.
   - EFI
     - [Download](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Monterey_RX550_P310S/EFI_RX550.zip).

![Hackintosh2](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Monterey_RX550_P310S/pics/screen_shot.jpg)
1. MacBook Pro Ventura
   - Hardwares:
     - Acer AN515-43(Ryzen 3550H, Vega8, RX560X, HID I2C touchpad)
     - Wifi: Intel 7260AC
   - Status:
     - Just works fine. However, there are some limitations from Ryzen platform, see [NootedRed](https://chefkissinc.github.io/nred/).
 - EFI
   - [Download](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Ventura_Ryzen5_AN515-43/OC_AMD_AN515-43.zip)

![Ryzentosh](https://github.com/moqsien/mq_hackintosh/blob/main/EFI_Ventura_Ryzen5_AN515-43/macbook.png)

## Docker-OSX(using MacOS in docker)
----------------------

- [Docker-OSX](https://github.com/sickcodes/Docker-OSX)

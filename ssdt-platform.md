# What SSDTs do each platform need

Please see the **specific ACPI section of your config.plist**, all SSDTs needed are covered there with a brief explainer. But here's a very quick TL;DR:

- [What SSDTs do each platform need](#what-ssdts-do-each-platform-need)
  - [Desktop](#desktop)
  - [Laptop](#laptop)
  - [SSDT Creation](#ssdt-creation)

## Desktop

| Platforms | **CPU** | **EC** | **AWAC** | **NVRAM** | **USB** |
| :-------: | :-----: | :----: | :------: | :-------: | :-----: |
| SandyBridge | [CPU-PM](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html#sandy-and-ivy-bridge-power-management) (Run in Post-Install) | [SSDT-EC](/Universal/ec-fix.md) | N/A | N/A | N/A |
| Ivy Bridge | ^^ | ^^ | N/A | N/A | N/A |
| Haswell | [SSDT-PLUG](/Universal/plug.md) | ^^ | ^^ | ^^ | ^^ |
| Broadwell | ^^ | ^^ | ^^ | ^^ | ^^ |
| Skylake | ^^ | [SSDT-EC-USBX](/Universal/ec-fix.md) | ^^ | ^^ | ^^ |
| Kaby Lake | ^^ | ^^ | ^^ | ^^ | ^^ |
| Coffee Lake | ^^ | ^^ | [SSDT-AWAC](/Universal/awac.md) | [SSDT-PMC](/Universal/nvram.md) | ^^ |
| Comet Lake | ^^ | ^^ | ^^ | N/A | [SSDT-RHUB](/Universal/rhub.md) |
| AMD (15/16h) | N/A | ^^ | N/A | ^^ | N/A |
| AMD (17h) | [SSDT-CPUR for B550](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-CPUR.aml) | ^^ | N/A | ^^ | N/A |

## High End Desktop

| Platforms | **CPU** | **EC** | **AWAC** |
| :-------: | :-----: | :----: | :------: |
| Nehalem and Westmere | N/A | [SSDT-EC](/Universal/ec-fix.md) | N/A |
| Ivy Bridge-E | [SSDT-PLUG](/Universal/plug.md) | ^^ | ^^ |
| Haswell-E | ^^ | [SSDT-EC-USBX](/Universal/ec-fix.md) | ^^ |
| Broadwell-E | ^^ | ^^ | ^^ |
| Skylake-X | ^^ | ^^ | [SSDT-AWAC](/Universal/awac.md) |

## Laptop

| Platforms | **CPU** | **EC** | **Backlight** | **I2C Trackpad** | **AWAC** | **USB** | **IRQ** |
| :-------: | :-----: | :----: | :-----------: | :--------------: | :------: | :-----: | :-----: |
| SandyBridge | [CPU-PM](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html#sandy-and-ivy-bridge-power-management) (Run in Post-Install) | [SSDT-EC](/Universal/ec-fix.md) | [SSDT-PNLF](/Laptops/backlight.md) | N/A | N/A | N/A | [IRQ SSDT](/Universal/irq.md) |
| Ivy Bridge | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ |
| Haswell | [SSDT-PLUG](/Universal/plug.md) | ^^ | ^^ | [SSDT-GPI0](/Laptops/trackpad.md) | ^^ | ^^ | ^^ |
| Broadwell | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ |
| Skylake | ^^ | [SSDT-EC-USBX](/Universal/ec-fix.md) | ^^ | ^^ | ^^ | ^^ | N/A |
| Kaby Lake | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ |
| Coffee Lake (8th Gen) and Whiskey Lake | ^^ | ^^ | [SSDT-PNLF-CFL](/Laptops/backlight.md) | ^^ | ^^ | ^^ | ^^ |
| Coffee Lake (9th Gen) | ^^ | ^^ | ^^ | ^^ | [SSDT-AWAC](/Universal/awac.md) | ^^ | ^^ |
| Comet Lake | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ | ^^ |
| Ice Lake | ^^ | ^^ | ^^ | ^^ | ^^ | [SSDT-RHUB](/Universal/rhub.md) | ^^ |

Continuing:

| Platforms | **NVRAM** | **IMEI** |
| :-------: | :-------: | :------: |
| Sandy Bridge | N/A | [SSDT-IMEI](/Universal/imei.md) |
| Ivy Bridge | ^^ | ^^ |
| Haswell | ^^ | N/A |
| Broadwell | ^^ | ^^ |
| Skylake | ^^ | ^^ |
| Kaby Lake | ^^ | ^^ |
| Coffee Lake (8th Gen) and Whiskey Lake | ^^ | ^^ |
| Coffee Lake (9th Gen) | [SSDT-PMC](/Universal/nvram.md) | ^^ |
| Comet Lake | N/A | ^^ |
| Ice Lake | ^^ | ^^ |

## [SSDT Creation](/ssdt-methods/ssdt-methods.md)

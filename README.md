# The 3MS

The 3MS is short for MMMS, which stands for **M**odular **M**ulti **M**aterial **S**ystem

![GitHub Repo stars](https://img.shields.io/github/stars/3dcoded/3MS)
![GitHub forks](https://img.shields.io/github/forks/3dcoded/3MS)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/3dcoded/3MS)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/3dcoded/3MS)
![GitHub contributors](https://img.shields.io/github/contributors/3dcoded/3MS)
![GitHub License](https://img.shields.io/github/license/3dcoded/3MS)


<img src="logo.png" alt="drawing" width="200"/>

## Happy Hare Migration

In the next few weeks to months, the 3MS will be migrated to run on [Happy Hare](https://github.com/moggieuk/Happy-Hare) firmware. This will add many new features and make the 3MS more relaible. 

Here are a couple things to keep in mind to make the transition from the current software to Happy Hare as smooth as possible:

- New users should use the [BTT MMU Board](https://3dcoded.github.io/3MS/setup/controllers/bttmmb/) setup, as this is natively supported by Happy Hare.
- Existing 3MS mainboards configurations will be converted to be compatible with Happy Hare, but the MMU board is still recommended.

## Documentation

Documentation is available [here](https://3dcoded.github.io/3MS)

[![Built with Material for MkDocs](https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white)](https://squidfunk.github.io/mkdocs-material/)

## Support

If you want to support the 3MS project, click the link below. Anything you give goes directly into the development of the 3MS and my other projects. Thank you!

[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/3dcoded)


## More Projects

If you like this project, don't forget to give it a star! Also, check out my other projects:

- [DynamicMacros](https://github.com/3dcoded/DynamicMacros), never restart Klipper again for simple macros
- [KlipperMaintenance](https://github.com/3DCoded/KlipperMaintenance), maintenance reminders for Klipper

## Inspiration

- Prusa MMU1
- Bambu AMS

## Sample Prints

If you like this project, don't forget to star it!

<img src="https://github.com/3DCoded/3MS/blob/docs/docs/assets/images/sampleprints/sampletrex.jpeg?raw=true" width="200">

Model: [T-rex by Cipis](https://www.printables.com/model/5481-t-rex-multi-material)

---


<img src="https://github.com/3DCoded/3MS/blob/docs/docs/assets/images/sampleprints/samplecalendar.jpeg?raw=true" width="200">

Model: [Monolith Cryptic Calendar by Sevro](https://www.printables.com/model/698341-monolith-cryptic-calendar)

---

<img src="https://github.com/3DCoded/3MS/blob/docs/docs/assets/images/sampleprints/samplevoron.jpeg?raw=true" width="200">

Model: Voron Cube (bundled with OrcaSlicer), painted by me

## Why 3MS?

Why use the 3MS when there are many other multi-material systems? 

Here are a few reasons:

- **Simplified Design**: Minimal mechanical complexity for increased reliability.
- **Comprehensive Documentation**: Step-by-step guides to ensure smooth setup and operation.
- **Slicer-Agnostic**: No need for custom toolchange G-Code in your slicer.
- **Scalable**: Easily expand the system to handle any number of filaments.
- **Auto-Retries**: Automatic retries on failed tool changes to reduce downtime.
- **No Filament Cutter Needed**: Achieve clean tool changes without the need for filament cutters.
- **In Development: Rapid Tip Shaping**: Achieve even faster tool changes!

With that said, there are a few reasons why you might **not** want to/be able to use the 3MS:

- Klipper firmware is a requirement, so Marlin and RRF setups are a no go

## How it works

Here is a example step by step of what goes on during a single 3MS toolchange from T0 to T1:

1. Tip shaping and filament unload is performed by the slicer
2. The 3MS unloads T0 200mm at 4500mm/min (75mm/s)
3. The 3MS desyncs T0 from the extruder
4. The 3MS syncs T1 with the extruder
3. The 3MS loads T1 210mm at 4500mm/min
5. The printer loads the filament to the nozzle

The 3MS's motors work together with your printer's extruder. This way, there won't be any additional resistance from pulling the filament through a disabled extruder. Also, unloads and loads to/from the printer's extruder are fully synchronized with the 3MS. This allows for even faster toolchanges!

## What about the 3DChameleon?

I recently created a klipper plugin for the 3DChameleon after purchasing a unit. I'm sure my Chameleon could have worked if I had tuned it further, but after several months with only partial success, I gave up. I am still open to pull requests for **[3dchameleon-klipper](https://github.com/3dcoded/3dchameleon-klipper)** and will do my best to respond to issues there, but I won't be able to test it myself anymore.

## Stats

![Alt](https://repobeats.axiom.co/api/embed/d670d6f2eae5970f20cf34f40eb933c446089e6a.svg "Repobeats analytics image")

[![cc-by-sa](https://img.shields.io/badge/License-CC%20BY%20SA%203.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/3.0/)  [![mit](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# THT-Frames

THT-Frames is a through hole version of [Mutable Instruments Frames](https://mutable-instruments.net/modules/frames/).
For the MCU a **128KB** STM32F103C8T6/STM32F103CBT6 "bluepill type" module is used.
**Warning! Most of the conventional boards floating around on ebay, aliexpress, etc. are 64KB. Those won't work with the provided firmware.**
I'd recommend picking one up from robotdyn ([website](https://robotdyn.com/)/[aliexpress](https://robotdyn.aliexpress.com/store/1950989)), these are the ones I use and they work without any problems.
You can also pickup a matching APM32 board if you want for a little cheaper. I've tested them and they also seem to work fine.

It also uses a different dac than the original, because it isn't available as a DIP package.

## Panels

Be sure to check out my [printable-instruments](https://github.com/30350n/printable-instruments) repository, which contains pcb panels for several Mutable Instuments modules including Frames.
That being said, any third-party panels should also fit with these boards.

## How to use

### Quickstart

To get started quickly, you can just download the gerbers for both pcbs and the compiled software `.hex` file from the [Releases](https://github.com/30350n/tht-frames/releases) section.

### Hardware

If you want to export the gerbers yourself or modify them, just clone the repository and open the hardware files with KiCad.

### Software

This project requires slightly modified software, because it uses two 2-channel DACs instead of the single 4-channel DAC the original uses.

If you want to build the software yourself, clone the [mutable-dev-environment](https://github.com/pichenettes/mutable-dev-environment) repository and follow the provided instructions to set it up.
After that, copy the patch from this repository (`software/tht-frames.patch`) to `mutable-dev-environment/eurorack-modules` and also `cd` to that directory.
Finally apply the patch via `git apply tht-frames.patch` and build the firmware as usual.

## Credits
- **[Mutable Instruments](https://github.com/pichenettes/eurorack)** provided the original hardware design files and software which this projects builds upon.
- **[SoundForce - Braids Through-hole](http://sound-force.nl/?page_id=3179)** gave me the idea for this project.

## License
- Hardware: cc-by-sa-3.0
- Software: MIT

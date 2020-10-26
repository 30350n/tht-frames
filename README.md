[![cc-by-sa](https://img.shields.io/badge/License-CC%20BY%20SA%203.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/3.0/)  [![mit](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# THT-Frames

THT-Frames is a through hole version of [Mutable Instruments Frames](https://mutable-instruments.net/modules/frames/).
For the MCU a **128KB** STM32F103C8T6/STM32F103CBT6 "bluepill type" module is used.
**Warning! Most of the conventional boards floating around on ebay, aliexpress, etc. are 64KB. Those won't work with the provided firmware.**
I'd recommend picking one up from robotdyn ([website](https://robotdyn.com/)/[aliexpress](https://robotdyn.aliexpress.com/store/1950989)), these are the ones I use and they work without any problems.
You can also pickup a matching APM32 board if you want for a little cheaper. I've tested them and they also seem to work fine.

It also uses a different dac than the original, because it isn't available as a DIP package.

## Credits
- **[Mutable Instruments](https://github.com/pichenettes/eurorack)** provided the original hardware design files and software which this projects builds upon.
- **[SoundForce - Braids Through-hole](http://sound-force.nl/?page_id=3179)** gave me the idea for this project.

## License
- Hardware: cc-by-sa-3.0
- Software: MIT

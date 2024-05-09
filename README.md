# WAV File Volume Adjustment🔊

##### Warning ⚠️
Avoid using excessively large numbers for the refactoring factor (`factor`) as it may result in audio distortion or clipping. It is recommended to use values between 0.1 and 3 for best results. Experiment with different values to achieve the desired volume adjustment without compromising audio quality.


## Overview

This program, `volume.c`, is designed to modify the volume of a WAV audio file. It reads an input WAV file, scales the volume by a given factor, and writes the modified audio to an output WAV file. 

Try using this feature with your own .WAV files too!

## Usage

To use this program, follow these steps:

1. Compile the program using a C compiler. For example:
   ```
   gcc -o volume volume.c
   ```

2. Run the program with the following command-line arguments:
   ```
   ./volume input.wav output.wav factor
   ```
   - `input.wav`: The path to the original WAV audio file.
   - `output.wav`: The path to the new WAV audio file that will be generated.
   - `factor`: The factor by which to scale the volume. For example, a factor of `2.0` will double the volume, while a factor of `0.5` will halve it.

## Example

To double the volume of an audio file named `input.wav` and save the result as `output.wav`, run the following command:
```
./volume input.wav output.wav 2.0
```

## Implementation Details

- The program checks the command-line arguments and opens the input and output files.
- It reads the header from the input file and writes it to the output file.
- It reads the audio samples from the input file, scales them by the factor, and writes the modified samples to the output file.

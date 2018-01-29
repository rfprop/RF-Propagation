# RF-Propagation
A command line tool to predict RF propagation

This tool has been developed to analyse point to point loss, line of sight coverage, and RF propagation coverage within the communications frequency range. It had to work well on a Windows 10 PC and utilise easily available elevation data.
The application SPLAT! which has been around for a number of years, fulfils most of the requirements and has been compiled for Windows at various times. The source for this was easily available and offered with a GNU GPL, so was used as a starting point for the development.

1. The latest code base was compared to a code base that had been compiled for Windows, and most of the changes pulled across. This produced a working tool with some limitations.

2. The program was profiled and a couple of functions that used more than expected CPU were made faster.

3. The outer loop was modified to allow it to be split across multiple threads.  Most modern computers have multiple cores, so this significantly improves execution time.

4. Routines were added to allow the saving of the output to .bmp files to make it compatible with more windows tools.

Work to be completed.

1. Improve the ease of loading terrain data.

2. Move the .bmp writing code into a separate function, and reduce the huge amount of code repetition.

3. Add in more propagation models

4. Change the format of the reports, to provide the information in a more easily parsed manner. 



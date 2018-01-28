# RF-Propagation
A command line tool to predict RF propagation

This tool has been produced to fullfil a need to have a tool to analyse point to point loss, line of sight coverage, and RF propagation coverage.  The tool had to work well on a Windows 10 PC and with easily available elevation data.

There is a tool called SPLAT! which has been around for a number of years, which fulfills most of the requirements and which has been compiled for Windows at various points.  This was used as a starting point for the development.
1) The latest code base was diffed against the last code base that I could find that was compiled for Windows, and most of the changes pulled accross.  This produced a working tool with some limitations.
2) The program was profiled and a couple of functions found to use a substancial amount of the CPU, and some optimisatin carried out.
3) The outer loop was changed to allow it to be split accross multiple threads.
4) Routines were added to allow the saving of the output to .bmp files to make it compatible with more windows tools.

The improvements in speed from 2) and 3) between them produced around a 10 fold speed increase on the test computer.

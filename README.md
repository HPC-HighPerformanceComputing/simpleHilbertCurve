#simpleHilbertCurve

**simpleHilbertCurve** is a Python script that uses matplotlib to create [Hilbert curve](http://en.wikipedia.org/wiki/Hilbert_curve) plots. Hilbert curves are space filling fractals that can be used to map a one dimensional set into two dimensions. Hilbert curves mostly maintain locality meaning that clusters in the 2D representation are most likely close together in the 1D scale too. Hilbert curves can be a useful way of visualy summarizing and comparing large time series or large linear maps (like genomic data).

##Author
[Dent Earl](https://github.com/dentearl/)

##Dependencies
* Python 2.7
* [matplotlib](http://matplotlib.sourceforge.net/) 1.1.0

##Installation
1. Download the package.
2. <code>cd</code> into the directory.
3. Type <code>make</code>.
    
##Usage
    Usage: simpleHilbertCurve.py --max=MAX --level=LEVEL [options] inputFile

    simpleHilbertCurve.py takes a two column input, col1 is a position long a
    scale with values in [0, MAX] and col2 is a value in (-inf, inf).
    The LEVEL determines the length of the side of the square by
    2**LEVEL. By default levels greater than 10 are disallowed, though
    this restriction may be overrided.

    Options:
      -h, --help            show this help message and exit
      --max=MAX             the maximum length of the linear scale.
      -n LEVEL, --level=LEVEL
                            determines the length of one side of the square by 2^n. default=6
      --override            overrides the provision on --level <= 10. Using large level values can take
                            a long time or create enormous / resource intensive plots. default=False
      --normalize           subtracts off the mean and divides by the std dev.default=False
      --demo                creates a demonstration image based on the --level parameter. default=False
      --dpi=DPI             dots per inch of raster outputs, i.e. if --outFormat is all or png.
                            default=300
      --outFormat=OUTFORMAT
                            output format [pdf|png|eps|all]. default=pdf
      --out=OUT             path/filename where figure will be created. No extension needed.
                            default=myPlot

##Example
![Example image]()

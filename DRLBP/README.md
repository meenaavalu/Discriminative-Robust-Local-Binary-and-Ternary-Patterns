Author: Amit Satpathy (amit0001@gmail.com)

CAA 11042014

Version 1.1

Note that this code is only for academic use. Please contact the author, Nanyang
Technological University or Agency for Science, Technology and Research for commercial 
use.

Codes are based on the following papers:

[1] Amit Satpathy, Xudong Jiang and How-Lung Eng, “LBP Based Edge-Texture Features for 
Object Recognition”, regular paper, IEEE Transactions on Image Processing, Accepted, 2013.

[2] Amit Satpathy, Xudong Jiang and How-Lung Eng, “Human Detection Using Discriminative 
And Robust Local Binary Pattern”, Proc. of the IEEE Int. Conf. on Acoustics, Speech, and 
Signal Processing (ICASSP’2013), pp. 2376-2380, May 2013, Vancouver, Canada.

If you are using DRLBP in your work, kindly cite [1] - [2] in your publications.

IMPORTANT NOTE
The code is provided as it is. Piotr Dollar's modified toolbox which is used for 
gradient computation is provided (zip file). This version is modified from Version 3.01. As 
of writing this txt, the current version of Dollar's toolbox is 3.25. If time permits, I
will update the modified toolbox to the latest version of Piotr's Toolbox.

If you find any bugs, please inform me and I will fix them.

The codes work fine for Windows-based MATLAB. It has NOT been tested for Linux systems.

INSTALLATION

First, you will need to install the modified Piotr's MATLAB Toolbox. To do so, just do the 
following:

1)	Simply unzip, then add all directories to the Matlab path: 
	>> addpath(genpath('c:\piotrtoolboxmod_v3.01')); savepath;

2)	Run the compile script for the mex files: 
	>> toolboxCompile; 
  
Please install a C++ compiler (preferably Visual Studio) to compile the mex files for 
use.
 
USAGE
 
Please refer to the MATLAB script file, demo.m to view the procedures.

I have provided the C/C++ files for computing the DRLBP features. The files will need to be compiled to mex in MATLAB to run with the demo script. Alternatively, you can use the pre-compiled binaries in the bin folder to run if you do not have a C++ compiler.

Currently, only different circular radius of R is supported. The neighbourhood is strictly
fixed to 8 as the codes are heavily optimized for this. Only colour images are supported. If
you are using a grayscale image, replicate the image to 3 channels before sending to the mex 
function.

CHANGES FROM EARLIER VERSION
1) Added radius parameter as input for feature generation. Was omitted from earlier version.
2) Added some error checking codes for the mex files to make sure rogue parameters are not input.

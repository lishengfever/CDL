This is the code for CDL (collaborative deep learning). It consists of two
parts: a matlab component and a C++ component.

To run this code you need to make sure:
0. you have the mult_nor.mat file located in cdl-release/example (can be downloaded from wanghao.in/code/cdl-release.rar)
1. you have matlab with GPU support
2. you have installed the GSL library (see www.gnu.org/software/gsl/)

After installing GSL, please remember to add the path of the dynamic library
(the directory with files like libgsl.so.0.10.0) to LD_LIBRARY_PATH in your
.bashrc. Or you can directly change the code in cdl.m around Line 586 where
LD_LIBRARY_PATH is exported.

To save the pain of handling memory and variables in mex, we directly
compiled a C++ program for the updates of U and V and call the program
from matlab. If your program runs without trouble, congratulations! If not,
you may have to re-compiled the C++ component which is in the folder
'ctr-part'. You will need to install the GSL before doing that. 

To quickly run the program you can directly call the cdl_main.m.

To quickly know what CDL is doing click on collaborative-dl.ipynb (demo in this notenook uses the MXNet-version code, not this matlab/C++ version).

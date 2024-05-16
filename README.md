# <div align="center"> SFP: A Spectral Filter Predictor with Progressive Feedback Method for Latent Fingerprint Restoration </div>

```
The installation and executable files will be made available once the paper is accepted 
```

We're sharing the executable file to ensure a user-friendly experience. Our software combines MATLAB and Python.

The software comprises two parts:

<b> 1. Preprocessing with Total Variation </b> This step enhances latent fingerprints by reducing noise.

<b> 2. Progressive Feedback Method for Restoration </b> This method combines a new spectral filter predictor within a feedback framework. The spectral filter predictor PyTorch model is converted to ONNX for CPU, no GPU required.

We understand the importance of transparency and reproducibility in research. By offering the executable, we simplify its use, making it convenient, especially for result comparisons.


<br/>

## <div align="center">Requirements</div>
 
- Windows 10 or 11 operating system.

- Storage 14 GB 
    
    - ksip_lfp_enh_installer 300 MB
    - MATLAB_Runtime_R2022a_Update_6_win64 (installer 4 GB and install space required 8 GB)


<br/>

## <div align="center">Installation</div>

### Install MATLAB Runtime version R2022a (9.12)

1. Download MATLAB Runtime from [www.mathworks.com](https://www.mathworks.com/products/compiler/matlab-runtime.html) Or MATLAB_Runtime_R2022a_Update_6_win64.zip <b>(Coming soon)</b>.

2. Extract files and install MATLAB Runtime using `setup.exe`.

### Install KSIP Latent Fingerprint Enhancement

1. Download ksip_lfp_enh_installer.exe <b>(Coming soon)</b>.

2. Install `KSIP LFP ENHANCEMENT` using `ksip_lfp_enh_installer.exe`. The installation directory will be `C:\Program Files (x86)\KSIP LFP ENHANCEMENT`

3. Setup environment path 
	- Go to `Environment Variables`
	- Add `C:\Program Files (x86)\KSIP LFP ENHANCEMENT` in the `Path` variable under System variables. 

    If KSIP LFP ENHANCEMENT installed in a different location, add that specific path to System variables instead of C:\Program Files (x86)\KSIP LFP ENHANCEMENT.


<br/>

## <div align="center">Usage</div>

0. Please ensure the latent fingerprint image resolution is set to 500 DPI.

1. Open `Terminal` or `Windows Powershell`

2. Run `ksip_sfp.exe --help` and Enter to show the program usage 

        usage: ksip_sfp.exe [-h] [-s START_INDEX] [-e END_INDEX] -fp
                                FINGERPRINT_DIR [-seg SEGMENT_DIR] -out OUTPUT_DIR

        optional arguments:
        -h, --help            show this help message and exit
        -s START_INDEX, --start_index START_INDEX
                                Start index
        -e END_INDEX, --end_index END_INDEX
                                End index
        -fp FINGERPRINT_DIR, --fingerprint_dir FINGERPRINT_DIR
                                Fingerprint Directory
        -seg SEGMENT_DIR, --segment_dir SEGMENT_DIR
                                Segment Directory
        -out OUTPUT_DIR, --output_dir OUTPUT_DIR
                                Output Directory
	
### Example

<b> Run NIST SD27 Enhancement </b>

    ksip_sfp.exe -fp D:\NIST_SD27\Latent -seg D:\NIST_SD27\GlobalDict -out D:\NIST_SD27\Enhancement


<b> Run NIST SD27 Enhancement without Segment </b>

    ksip_sfp.exe -fp D:\NIST\NIST_SD27\Latent -out D:\NIST_SD27\Enhancement

<b> Run NIST SD27 Enhancement without Segment first 10 images </b>

    ksip_sfp.exe -fp D:\NIST_SD27\Latent -out D:\NIST_SD27\Enhancement -s 0 -e 10

<b> Run NIST SD27 Enhancement without Segment 10 images start at image no. 15 </b>

    ksip_sfp.exe -fp D:\NIST_SD27\Latent -out D:\NIST_SD27\Enhancement -s 15 -e 25

### Output Example

    0001/0001 | Image Path: C:\Users\Administrator\Desktop\test\img\001L2U.bmp
    0001/0001 | Segment Path: C:\Users\Administrator\Desktop\test\seg\001L2U.png
    0001/0001 | Start Enhancement
    0001/0001 | Enhancement Success
    0001/0001 | Save enhanced image to C:\Users\Administrator\Desktop\test\out\enhanced\001L2U.png
    0001/0001 | Execution time: 26.39 second
    0001/0001 | Average Execution time: 26.39 sec. Total time: 0:00:26.391823. Estimating Time to Complete: 2023-08-07 07:34:30.650199

<br/>

## <div align="center"> Acknowledgements </div>

This work was supported in part by the Department of Electrical Engineering, Faculty of Engineering, Kasetsart University, and in part by the Siew-Sngiem Karnchanachari Research Leadership and Young Professorship Awards.

<br/>


## <div align="center">License</div>

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

<br/>

## <div align="center">Citing SFP</div>

If you are using SFP or benchmarks in your research, kindly reference the following.

	@ARTICLE{10526230,
	  author={Kriangkhajorn, Supakit and Horapong, Kittipol and Areekul, Vutipong},
	  journal={IEEE Access}, 
	  title={Spectral Filter Predictor for Progressive Latent Fingerprint Restoration}, 
	  year={2024},
	  volume={12},
	  number={},
	  pages={66773-66800},
	  keywords={Fingerprint recognition;Image restoration;Friction;Frequency-domain analysis;Filtering;Image matching;Deep learning;Image restoration;Image forensics;Machine learning;Fingerprint recognition;image restoration;image enhancement;image filtering;image forensics;machine learning},
	  doi={10.1109/ACCESS.2024.3397729}}

or

	S. Kriangkhajorn, K. Horapong and V. Areekul, "Spectral Filter Predictor for Progressive Latent Fingerprint Restoration," in IEEE Access, vol. 12, pp. 66773-66800, 2024, doi: 10.1109/ACCESS.2024.3397729.

<br/>

## <div align="center">Contact</div>

If you have any questions or need assistance, reach us fengvpa@ku.ac.th / supakit.kr@gmail.com.


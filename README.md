# FISM_data
FISM File Process via IDL language
1. Download FISM file in (*.sav) to proceed
2. Open IDL application
3. Close open projects (if any) to avoid any overlapping
4. Create a new project from File Menu
	4.1 Name it as FISM (DOY) in workspace
	4.2 Update IDL path when open/close
5. Click Open and Select FISM (*.sav) from workspace
6. Go to variable Explorer to see the output of (*.sav) file
7. The following variables can be seen from the explorer
IRRADIANCE = Array of (1900, 1440) matrix
UNCERTAINITY = Array of (1900, 1440) matrix
UTC = Vector of length (1440) 
WAVELENGTH = Vector of length (1900)
YDOY = DOY
8. Type in console
> help, IRRADIANCE to get the array info.
> print, IRRADIANCE to print on screen (not recommended)
9. Open files and write corresponding variables.

openw, 5, ‘file-DOY.dat’;
printf, 5,IRRADIANCE (or WAVELENGTH or UTC)
close, 5

10. Use same steps for other parameters as well.

IDL uses Fortran-like formatting so you can also write FORMATTED output.
Abbreviations
FISM – Flare Irradiance Spectral Model
IDL – Interactive Data Language
DOY – Day of Year
UTC ¬– Universal Time

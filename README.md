# TI-Phasor
TI-84+ CE program for converting sinusoidals from their rectangular form to phasor notation and vice-versa. The archived program will persist after ram is cleared.

## Code
```bash
Disp "1. PHASOR TO RECT"
Disp "2. RECT TO PHASOR"
Prompt A
If A=1
Then
	Disp "ENTER MAGNITUDE:"
	Prompt M
	Disp "ENTER ANGLE:"
	Prompt theta
	Disp ""
	Disp "RECTANGULAR FORM:"
	Mcos(theta)->R
	Msin(theta)->J
	Disp toString(round(R,3))+"+"+"[i]"+toString(round(J,3))
	Disp ""
	Disp "STORED IN MEMORY:"
	Disp "R=REAL"
	Disp "J=IMAGINARY"
End
If A=2
Then
	Disp "ENTER REAL PART:"
	Prompt R
	Disp "ENTER IMAGINARY PART"
	Prompt I
	Disp ""
	Disp "PHASOR FORM:"
	sqrt(R^^2+I^^2)->M
	tan^-1(I/R)->P
	Disp toString(round(M,3))+"<"+toString(round(P,3))+"^^o"
	Disp ""
	Disp "STORED IN MEMORY:"
	Disp "M=MAGNITUDE"
	Disp "P=PHASE"
End
:"
```

## Features
- Converts rectangular to phasor notation, and phasor notation back to polar
- Output is rounded off to 3 digits
- Real and imaginary parts (rectangular form) are saved in `R` and `J`, respectively
- Phasor magnitude and phase (phasor form) are saved in `M` and `P`, respectively
- Complete, un-rounded values are saved in those variables^^^

## Installation

### Using TI-Connect Software
Pretty simple, save the `phasor.8xp` program somewhere on your computer, and use the TI-Connect software to send the program to the calculator. You'll need a usb to _mini_ usb cable for this. You can unarchive it by hitting `2nd -> + -> 6` (or `UnArchive`). Give it the program as an argument by hitting `prgm` and selecting it from the list.

### Manually
Create a new program and type in this code. The software I used to convert it to text swapped out some things that can only be presented on the calculator (`theta` is actual letter, `^^o` is the degree symbol, etc).
Archive it with `2nd -> + -> 5` (or `Archive`) and giving the program as an argument. It will persist after clearing RAM.

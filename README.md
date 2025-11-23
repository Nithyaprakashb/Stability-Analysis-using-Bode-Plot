# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![DocScanner 23 Nov 2025 4-59 pm_1](https://github.com/user-attachments/assets/031d5fb1-42f4-4578-b1d9-9f679cca0eff)
![DocScanner 23 Nov 2025 4-59 pm_1(1)](https://github.com/user-attachments/assets/1b55f7fe-c718-46dd-aa5a-8407810a3682)

## Graph:
![DocScanner 23 Nov 2025 4-59 pm_1(2)](https://github.com/user-attachments/assets/228810b1-7e27-4d3f-9700-bc3160ecc8e3)


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:
<img width="707" height="631" alt="image" src="https://github.com/user-attachments/assets/e1060f83-c438-46eb-805f-9f878133cdb3" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =12.0000 dB <br>
Phase Margin =  60.4231 deg<br>
Gain crossover frequency = 0.9070 rad/s<br>
Phase crossover frequency = 4.4721rad/s<br>
The system is stable

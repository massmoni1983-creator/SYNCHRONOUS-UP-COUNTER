### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
```
1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.
```

**UP_COUNTER PROGRAM**

<img width="507" height="297" alt="Screenshot 2025-12-18 082841" src="https://github.com/user-attachments/assets/c5baeb8e-0f37-4e79-8beb-ac21de7607fc" />

```
Developed by: MURUGA S
RegisterNumber: 25010785
```

**RTL LOGIC UP COUNTER**

<img width="931" height="315" alt="Screenshot 2025-12-18 083039" src="https://github.com/user-attachments/assets/c1c3772a-da74-4e35-94bb-6f09ac1cdb59" />

**TIMING DIAGRAM FOR IP COUNTER**

<img width="1037" height="171" alt="Screenshot 2025-12-18 083226" src="https://github.com/user-attachments/assets/cfa8f55f-94bd-469c-9e12-7775aae25dce" />

**TRUTH TABLE**

<img width="618" height="811" alt="image" src="https://github.com/user-attachments/assets/78a9ae91-cf33-48a4-b94e-460374cbe331" />

**RESULTS**
 Hence a 4 bit synchronous up counter is implemented correctly

**DOWN_COUNTER PROGRAM**

<img width="580" height="290" alt="Screenshot 2025-12-18 083426" src="https://github.com/user-attachments/assets/b3ac3852-893f-49e5-aaac-05429c3adf74" />
<img width="552" height="292" alt="Screenshot 2025-12-18 083509" src="https://github.com/user-attachments/assets/0ee0bed8-e92e-40e3-a3cc-99ed1713c7e4" />

```
Developed by: MURUGA S
RegisterNumber: 25010785
```

**RTL LOGIC UP COUNTER**
<img width="764" height="304" alt="image" src="https://github.com/user-attachments/assets/e00e9aad-cdaa-4467-bae3-928a2456b03d" />

**TIMING DIAGRAM FOR IP COUNTER**

<img width="1029" height="304" alt="Screenshot 2025-12-18 083804" src="https://github.com/user-attachments/assets/a87aed9b-d436-4730-b21d-e48824d86142" />

**TRUTH TABLE**

<img width="707" height="710" alt="image" src="https://github.com/user-attachments/assets/b743d6ae-b49d-4b80-b553-6acb9a3aa4f0" />

**RESULTS**
 Hence a 4 bit synchronous down counter is implemented correctly


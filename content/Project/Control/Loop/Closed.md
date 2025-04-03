---
title: Closed-Loop Control System
alias: Closed-Loop
---

### Introdution

> [!abstract]
> 
> - Responding to change requires measuring outputs to influence inputs
> - Called **Feedback Control**[^1]
---

### Structure

- The process forms a **Loop** and is called **Negative feedback** because it subtracts the measurement from the baseline.

> [!NOTE]
> 
> - Measure the output with a **Sensor**
> - Compare the measured output to a **Reference signal** or target value **Comparator**
> - Generate an **Error signal**, which is the difference between the reference signal and the measured value
> - Input the error signal to the **Controller**
> - Based on this error, the controller calculates and generates a new input to the plant

---

### Feature & Example

> [!example] Dishwasher
> 
> <details style='padding-left: 25px'>
>   <summary><b>Sensor</b></summary>
>   
>   - Measure the cleanliness of a dish
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Reference Signal</b></summary>
> 
>   - Desired cleanliness level
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Comparison</b> & <b>Error</b></summary>
>   
>   - Difference between actual and desired cleanliness
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Controller</b></summary>
>   
>   - Adjusts the cleaning time based on the error, running until **the error goes to zero**[^2]
> </details>
> 
> <p></p>


> [!example] Sprinkler
> 
> <details style='padding-left: 25px'>
>   <summary><b>Sensor</b></summary>
> 
>   - Soil moisture sensor
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Reference Signal</b></summary>
>   
>   - Desired soil moisture level
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Comparison</b> & <b>Error</b></summary>
> 
>   - Difference between actual and desired humidity
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Controller</b></summary>
> 
>   - Adjust sprinkler run times based on tolerance, stopping when desired humidity is reached
> </details>
> 
> <p></p>

> [!example] Car Cruise Control
> 
> <details style='padding-left: 25px'>
>   <summary><b>Sensor</b></summary>
>   
>   - Speedometer<sup>(measures actual speed)</sup>
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Reference Signal</b></summary>
> 
>   - The desired speed set by the driver
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Comparison</b> & <b>Error</b></summary>
> 
>   - Difference between actual speed and desired speed[^3]
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Controller</b></summary>
>   
>   - Automatically adjust the **accelerator pedal**<sup>(input)</sup> position to zero error
> </details>
> 
> <p></p>

---

### Merit & Simplify Block Leading

> [!check] Merit
> 
> - That it **automatically reacts** to changes or disturbances in the system and tries to make the **error zero**

> [!check] Simplify Block Leading
> 
> - The entire **Closed-Loop System** can be represented by a single **Equivalent Transfer Function**
> - This means that the original **plant**$\small (G)$ can be viewed as a new equivalent system whose behavioral characteristics have changed due to feedback.
> 
> > [!NOTE]- Representation
> > 
> > - **Reference Signal** : $\small (V)$
> > - **Controller** : $\small (D)$
> > - **Plant** : $\small (G)$
> > - **Output** : $\small (Y)$
> > - **Sensor** : $\small (H)$
> > - **Error** : $\small (E)$
> 
> > [!NOTE]- Equivalent Transfer Function
> > 
> > - $\small (DG / (1 + DGH))$


[^1]: Also known as **Negative Feedback**, **Automatic Control**
[^2]: (when the desired cleanliness is reached)
[^3]: speed↓ → error+ on uphill, speed↑ → error- on downhill

---
title: Open-Loop Control System
alias: Open-Loop
---

> [!abstract]
> 
> - Simple structures where the **inputs do not depend on the outputs**[^1] 

> [!caution]
> 
> - No way to compensate for **changes in the system's internal** or **external environment**<sup>(disturbances)</sup>
> 
>     -> Because we **don't know the actual output**

---

### Feature & Example

- Mainly used for simple processes with well-defined input and output relationships

> [!example] Dishwasher
> 
> <details style='padding-left: 25px'>
>   <summary><b>Plant</b></summary>
>   
>   - dishwasher
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Output</b><sup>(goal)</sup></summary>
>   
>   - Clean Plate
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Input</b></summary>
>   
>   - User-set cleaning time
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Limitation</b></summary>
>   
>   - Works only for a set time,<br>regardless of whether the dish is already clean or dirty enough to not get clean in the set time
>   <span style='display: block; margin-top: 0.5em; margin-bottom: 0.5em'></span>
> 
>       -> In other words, **it doesn't check the output**<sup>(the cleanliness of the plate)</sup>
> </details>
> 
> <p></p>

> [!example] Lawn
> 
> <details style='padding-left: 25px'>
>   <summary><b>Plant</b></summary>
>   
>   - Grass/Soil
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Output</b><sup>(goal)</sup></summary>
> 
>   - Soil with appropriate humidity
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Input</b></summary>
> 
>   - User-set duration of operation<sup>(timer)</sup>
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Limitation</b></summary>
> 
>   - Works for the set time even if the soil is already wet enough due to rain.
>   <span style='display: block; margin-top: 0.5em; margin-bottom: 0.5em'></span>
>   
>       -> **Not checking the output**<sup>(soil moisture)</sup>
> </details>
> 
> <p></p>

> [!example] Maintain Car Speed
> 
> <details style='padding-left: 25px'>
>   <summary><b>Plant</b></summary>
>   
>   - Car
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Output</b><sup>(goal)</sup></summary>
>   
>   - Constant speed
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Input</b></summary>
>   
>   - Fixed accelerator pedal position
> </details>
> 
> <p></p>
> 
> <details style='padding-left: 25px'>
>   <summary><b>Limitation</b></summary>
>   
>   - Speed changes when encountering hills or downhills
>   - Doesn't adapt to **external changes**<sup>(disturbances)</sup><br>because it doesn't adjust the **accelerator pedal**<sup>(input)</sup> based on **actual speed**<sup>(output)</sup>
> </details>
> 
> <p></p>


[^1]: The inputs are not adjusted by seeing the outputs

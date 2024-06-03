[[Laws of Thermodynamics]]

## Thermodynamic System

| System | Energy exchange | Matter exchange |
|--------|-----------------|-----------------|
|Isolated|       no        |       no        |
| Closed |       yes       |       no        |
| Open   |       yes       |       yes       |


## Isothermal process
In thermodynamics, an isothermal process is a type of thermodynamic process in which the temperature T of a system remains constant: ΔT = 0. This typically occurs when a system is in contact with an outside thermal reservoir, and a change in the system occurs slowly enough to allow the system to be continuously adjusted to the temperature of the reservoir through heat exchange (see quasi-equilibrium). In contrast, an adiabatic process is where a system exchanges no heat with its surroundings (Q = 0).

In an isothermal process,
$$
T = \text{const.}
$$

## Adiabatic process
In thermodynamics, an adiabatic process (Greek: adiábatos, "impassable") is a type of thermodynamic process that occurs without transferring heat or mass between the thermodynamic system and its environment. Unlike an isothermal process, an adiabatic process transfers energy to the surroundings only as work. As a key concept in thermodynamics, the adiabatic process supports the theory that explains the first law of thermodynamics.

**Some processes occur too rapidly for energy to enter or leave the system as heat, allowing a convenient "adiabatic approximation".**


## Adiabatic relation
In an adiabatic process,
$$PV^\gamma = \text{constant}$$
This is called the **adiabatic relation**
or
$$P\rho^{-\gamma} = \text{constant}$$
With ideal gas law, adiabatic relation can also be written as
$$
T\rho^{1/(\gamma-1)} = \text{constant}
$$

Where $\gamma$ is called adiabatic index. It is defined as
$$
\gamma := \frac{C_P}{C_V}
$$
For monatomic gas $\gamma = 5/3$

### Application: derivation of sound speed
$$
c_s^2 \sim \left.\frac{dP}{d\rho}\right|_{ad}
$$
Differentiating the adiabtic relation $P\rho^{-\gamma} = \text{constant}$,
$$ \left.\frac{dP}{d\rho}\right|_{ad} = \gamma\frac{P}{\rho} $$
For ideal gas
$$ P = \frac{\rho}{\mu m_p} kT $$
Therefore
$$ \left.\frac{dP}{d\rho}\right|_{ad} = \gamma\frac{kT}{\mu m_p} $$
Finally, sound speed is
$$c_s = \sqrt{\frac{\gamma kT}{\mu m_p}}$$
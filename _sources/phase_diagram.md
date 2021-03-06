# Phases and phase diagram

We start the discussion from the general public understanding of what is a phase and phase transitions. Then, we will discuss why we are doing the model studying from a logical point of view. After that, we will introduce some formal definition of thermodynamic limit that is crucial for our later discussion. In the next section, we will use Ising model as a concrete examples to discuss what is the physical meaning of those concepts.

## What is a phase? What is a phase diagram?

We learn the concept of phases before we enter the university. We were told that there are three phases for water. The solid phase(ice), the liquid phase(water) and the gas phase(vapor).

Those phases can be achieve via different physical condition. For example, we can have ice when we are below 0$^\circ$C. When we are at room temperature, we can observe phase transition from solid to liquid phase--the ice melts. The diagram that tells us what are the stable phase under different physical parameters is the phase diagram. In an abstract sense, the phases are different pattern of collective behavior. The phase diagram is the diagram that describe what are the physical parameters such that specific pattern of collective behavior is stable and how the system changes their collective behavior when the physical parameters are adjusted.

In fact, there are more than three phases for a many-body system. We could have ferromagnetic for magnetic systems, we could have insulator as plastic, we could have plasma as our sun. There are so many phases out there. How to understand them? How to characterize the transition between different phases? Why the transition between different phases could be an interesting subject to understand? We will try to elaborate this part.

## The spirit of model studying

In the study of phases or phase transitions, one will encounter various models. Ising model, Heisnberg model, Potts model, dimer models, height models, etc. They are related to various interesting concepts including topology and gauge theories. However, why should we study those models? What can we learn from studying of those models?

We will discuss one of the important models -- the Ising model. After we study the Ising model, one will soon realize that the model are quite ``simple''. It is so simple that it is not clear why such a simple model would be relevant to describe our nature. Other above mentioned models also share similar features that they seem to be ad hoc models for special purposes. There should be some physical arguments about why we should study such models and how such ad hoc models could help us understand certain physical phenomena.

Conceptually, it is tied with the idea that we are looking for a simplest nontrivial model to help us understand specific physical phenomena.
From this perspective, the Ising model is the simplest non-trivial model to study phase transitions.
To study phase transitions, at least the model needs to have two phases.
Ising model host a disordered phase at high temperature and a ordered phase at zero temperature limit. 
Surprisingly, Ising model also demonstrate two types of phase transitions: the first order phase transition and continuous phase transition depends on whether the $Z_2$ symmetry is explicitly broken. 
However, with only discrete symmetry, we don't expect Ising model to demonstrate the behavior of phase transition with continuous symmetry.
To study those phenomena, one needs to find a simplest nontrivial model with continuous symmetry.

We describe the model as 'simple' models in a sense that the physical meaning and the expression of the model can be related clearly. But that does not mean they are easy to study or understand. However, because of the 'simplicity', one can go pretty far to understand those models. Sometimes, one can even solve it exactly.

On the other hand, one could feel studying those models are usually far away from physical reality.
How could such highly simplified models gives us hints about what happened in nature? The traditional approach is to start from microscopic physics and include different effects one by one.
If certain phenomena is not captured, we include more parameters into our model.
Such bottom up approach usually have very strong connection with microscopic details.
However it usually also leads to a complicated Hamiltonian which can only be solved approximately.
Comparing with the idealistic models which can be solved exactly, one might reach the conclusion that we should just give up those beautiful structure and use computers to help us solving those complicate but realistic model.

The problem about this approach is about the generality. Starting from realistic but complicate models, one can make some predictions. Or even fit the experimental data pretty well by tuning parameters. However, what is the general structure for the model is usually hidden behind the complicated competing effects. The simple toy models might not give us quantitatively correct answers. However, the simple structure helps us to identify the universal behavior and the mechanism behind the universal behaviors.

From this point of view, studying those simple but nontrivial models actually is quite valuable to understand the general behavior without the microscopic details. However, how to get the simplest non-trivial model as a starting point is an art. The theoretical framework that address this question is the concept of renormalization group(RG) and effective theory. One can use RG to identify the relevant ingredients for constructing a simplest non-trivial model. The two approach has their pros and cons, one should keep that in mind and use them according to different purposes.


## The formal description of our system

To set the stage, we will formulate our problem formally and use the specific example--Ising model to demonstrate the point of view.

Consider a sample region $\Omega$ the Hamiltonian of the system is $H_{\Omega}$. The surface and the volume of $\Omega$ is $S(\Omega)$ and $V(\Omega)$. For the sample with linear dimension $L$. In $D$ dimensional system, we know $V(\Omega)\propto L^D$ and $S(\Omega)\propto L^{D-1}$.

We will use $H_{\Omega}$ to define our system

$$
-\beta H_{\Omega}[\{K_n\}]=\sum_n K_n\Theta_n\text{.}
$$
Here,
* $-\beta H_{\Omega}[\{K_n\}]$ is the object that is important for us to construct the partition function.
* The partition function is parameterized by dimensionless parameters $K_n$.
* $\Theta_n$ is the n-body operators for the dynamical degrees of freedom. *e.g.* two-spin coupling as $S_iS_j$, three-spin coupling as $S_iS_jS_k$, etc.

The partition function of our system is

$$
Z[\{K_n\}]=Tr\left[e^{-\beta H_{\Omega}[\{K_n\}]}\right]\text{.}
$$
Here $Tr[]$ means the summation over all possible microscopic configuration. For Ising model with $N$ spins, the trace corresponds to $\sum_{S_1}\sum_{S_2}...\sum_{S_N}$.

The free energy of our sample $\Omega$ is

$$
F_{\Omega}[\{K_n\}]= \underbrace{V(\Omega)}_{\sim L^D} \underbrace{f_b[\{K_n\}]}_{\text{bulk free energy density}}+\underbrace{S(\Omega)}_{\sim L^{D-1}} \underbrace{f_s[\{K_n\}]}_{\text{surface free energy density}}+O(L^{D-2})\text{.}
$$

## The thermodynamic limit

The thermodynamic limit of the system is well defined if the bulk free energy density is well defined and is independent of the system size $\Omega$ at the following limit.

$$
f_b[\{K_n\}]\equiv \lim_{V(\Omega)\to\infty} \frac{F_{\Omega}[\{K_n\}]}{V(\Omega)}\text{.}
$$

Another usually used definition for thermodynamic limit is when the system size and number of degrees of freedom increases, *i.e.* $N(\Omega)\to\infty$ and $V(\Omega)\to\infty$, in a way that the density of the number of degrees of freedom, $\frac{N(\Omega)}{V(\Omega)}$, is kept fixed, the bulk free energy density is finite with no dependence on $\Omega$.


```{admonition} What?
:class: tip
Most of the system we considered has a well defined thermodynamic limit. So let's take a example which has no well defined thermodynamic limit.

Consider a ball with uniforml charge density $\rho$ with radius $R$. We can ask what is the energy of the system as a function of $R$? Will the system have a well defined thermodynamic limit when $R\to\infty$? 

Suppose the potential energy of charge Q and q is $V(r)=\frac{AQq}{r}$. The total potential energy of the ball is

$$
E(R)=\int_0^R \left( \rho \frac{4\pi}{3}r^3 \right)\frac{A}{r}\left(\rho 4\pi r^2\right) dr\propto R^5\text{.}
$$
So we have

$$
\lim_{R\to\infty} \frac{E(R)}{V(R)}\sim\lim_{R\to\infty} R^2\text{.}
$$

Therefore, we conclude the system does not have a proper thermodynamic limit. We can also see the fact that the system does not have a proper thermodynamic limit is because we consider potential energy due to long range interaction. Because of that, we will only focus on system with short range interaction with a well defined thermodynamic limit.
```


## The continuous and discontinuous phase transition ( formal definition)

From the expression

$$
Z[\{K_n\}]=Tr\left[e^{-\beta H_{\Omega}[\{K_n\}]}\right]; -\beta H_{\Omega}[\{K_n\}]=\sum_n K_n\Theta_n\text{.}
$$

We know that the system is controlled by the dimensionless coupling constants $K_n$. When we change $K_n$, we could change the pattern of the collective behavior. Therefore, we can go from one phase to another. So, how to change $K_n$? Usually, $K_n$ is related to the ratio between the microscopic coupling energy scale and the thermal fluctuation controlled by macroscopic temperature $T$. For example, for Ising model, the Hamiltonian is $\sum_{i,j} JS_iS_j$, the corresponding dimensionless coupling is $K=-\beta J$. To change $K$, we can either adjust $J$ or change the temperature $T$. In practice, changing how spins coupled with each other is more difficult comparing with changing the temperature of the system. Therefor, the easiest way to drive the system from one phase to the other is by changing temperature.

The phase diagram is therefore, a diagram described in the coupling constant space. The dimension of this coupling constant space depends on the model. In general, we could have a high dimensional space. However, as we already pointed out, the coupling constants are functions of the inverse temperature $\beta=(k_BT)^{-1}$. As we change the temperature $\{K_n(\beta)\}$, which controls the partition function, will traverse the phase diagram from one region to the other in the coupling constant space. It is possible that the system will cross the phase boundary and phase transitions happened.

At the phase boundary, the free energy must be continuous. We can characterize the phase transition as continuous or discontinuous phase transitions according to the following criteria
1. Continuous phase transition: $\frac{\partial f_b[{K_n}]}{\partial K_i}$ are all continuous across the phase boundary. Sometimes it is called second order phase transition. However, this is a bad nomenclature. So we mentioned this term just in case you read it in some old references.
2. Discontinuous phase transition: One or more $\frac{\partial f_b[{K_n}]}{\partial K_i}$ are discontinuous across the phase boundary. Sometimes it is called first order phase transition. Similarly, we should avoid using this term during our discussion.

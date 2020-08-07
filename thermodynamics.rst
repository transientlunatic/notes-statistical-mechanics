The First Law
=============

We can reach a microscopic understanding of the First Law starting with
the Canonical Distribution,

.. math::

   \label{eq:14}
     P_i = \frac{e^{-\beta E_i}}{Z}

 with the expression for :math:`U = \ev{E} = \sum_i E_i P_i`. For a
reversible change of :math:`E_i` in a system due to a change in volume,

.. math::

   \begin{aligned}
     \dd{u} &= \sum_i E_i \dd{P_i} + \sum_i P_i \dd{E_i} \\
   &= \sum_i E_i \dd{P_i} + \sum_i P_i \qty( \pdv{E_i}{V} ) \dd{V} \\
   &= \sum_i E_i \dd{P_i} - p \dd{V}\end{aligned}

 This is equivalent to

.. math:: \dd{u} &= {\dd{Q}} + {\dd{w}}

 for :math:`{\dd{u}} = \sum_i E_i \dd{P_i}`, and
:math:`{\dd{u}}~{rev} = T \dd{S} =
\sum_iE_i \dd{P_i}`, for :math:`S` the entropy of a system.

Relating :math:`\beta` and :math:`T`
====================================

We can show that :math:`\beta` is a function of :math:`T` by onstruting
a canonial ensemble in which each system is a composite of two
subsystems. These must be in thermal equilibrium, and so the subsystems,
:math:`A` and :math:`B`, must have the same temperature,
:math:`T_A = T_B`. We have the constraints

.. math:: \sum_i a_{A,i} = A \qquad \sum_i a_{B,i} = A

 Then

.. math:: \sum a_{A,i} E_{A,i} + \sum_i a_{B,i} E_{B,i} = E~{tot}

 The total energy in an ensemble is fixed but can be transferred between
subsystems. These three constraints imply three Lagrange multipliers on
the system, and we end up with

.. math::

   P_{A,i} = \frac{e^{-\beta E_{A,i}}}{Z_A}, \qquad P_{B,i} =
   \frac{e^{-\beta E_{B,i}}}{Z_B}

 where, as a result of the total energy constraint :math:`\beta` is the
same for each expression. If the two subsystems always have the same
:math:`\beta` and :math:`T` then

.. math:: \beta = \beta(T)

 Now, consider the function

.. math::

   \label{eq:15}
     H = - \sum_i P_i \log(P_i)

 then, for a change,

.. math::

   \begin{aligned}
     \dd{H} &= - \sum_i \dd{P_i} - \sum_i \dd{P_i} \log{P_i} \\
     &= - \sum_i \dd{P_i} -\sum_i \dd{P_i} \qty( log(e^{-\beta E_i}) - \log(z) ) \\
     &= - \sum_i \qty( \dd{P_i} \qty( - \beta E_i - \log(z) + \dd{P_i} )) \\
     &= - \sum_i \dd{P_i} \qty( 1 - \log(z) ) + \beta \sum \dd{P_i} E_i \\
     \text{since } & \sum P_i = 1 \implies \sum \dd{P_i} =0 \\
     &= \beta \sum_i \dd{P_i} E_i \\
     \shortintertext{then, assuming that $\beta T = \text{const} = k~B^{-1}$,}
     k~B \dd{H} &= \dd{s} \\
   \therefore s &= k~B H = -k~B \sum_i P_i \log(P_i)\end{aligned}

 This is an important but controversial result, but it is a consistent
form for :math:`s`.

Consider a microcanonical system with a total of :math:`\Omega` states,
which are degenerate. Now assuming that the entropy is

.. math::

   \label{eq:16}
     s = \phi(\Omega)

 and the probability of each microstate is proportional to
:math:`1/\Omega`, taking two systems, :math:`A` and :math:`B` then the
individual entropies are

.. math:: s~A = \phi(\Omega~A), \qquad s~B = \phi(\Omega~B)

 Entropy is extensive, depending upon the total quantity of material in
the system, and so is additive for weakly interacting systems, so

.. math:: s~{AB} = s~A + s~B

 But the number of states must be multiplicative, with
:math:`\Omega~{AB} = \Omega~A + \Omega~B`, so

.. math::

   S~{AB} = \phi(\Omega~{AB}) = \phi(\Omega~A \Omega~B) =
   \phi(\Omega~A) + \phi(\Omega~B)

 From this we can infer that the relationship must be logarithmic, with

[Boltzmann entropy equation] [eq:17] s = k B ()

Now we have :math:`s` as a function of :math:`k~B H`:

.. math::

   \begin{aligned}
     s &= -k~B \sum_i P_i \log(P_i) \\
   &= - k~B \sum_i P_i \qty[ - \beta E_i - \log(Z) ]\\
   &= k~B \beta \sum_i P_i E_i + k~B \log(z) \sum_i P_i
   \intertext{since $\sum_i P_i =1$,}
   &= \frac{1}{T} U + k~B \log(Z)\end{aligned}

 Thus we have a new thermodynamic quantity,

[The Helmholtz free energy] [eq:18] F = U - Ts = -k B T (Z)

which represents the amount of work which an isolated temperature at a
temperature :math:`T` can perform. This is the fundamental connection
between thermodynamics and statistical mechanics.

All of the other useful thermodynamic quantities can be derived using
this relationship, and its differential form,

.. math::

   \label{eq:19}
     \dd{F} = - s \dd{T} - p \dd{V}.

Thus

.. math::

   \begin{aligned}
     s = - \eval{\pdv{F}{T}}_V &= \qty( \pdv{T})_V \qty( k~B T \log(Z) ) \\
   p = - \eval{\pdv{F}{V}}_T &= - k~B T \qty(\pdv{V})_T \qty( \log(Z) )\end{aligned}

 Recalling the Maxwell relations for :math:`F=F(T,V,N)`, since :math:`N`
can vary in the grand canonical regime, we have

.. math::

   \label{eq:20}
     \dd{F} = - s \dd{T} - p \dd{V} + \mu \dd{N}

 for

.. math::

   \label{eq:21}
     \mu = \qty(\pdv{F}{N})_{T,V} = - k~B T \eval{ \pdv{V}}_{V,T} \log(Z)

 being the chemical potential.

Now consider a weakly interacting system of particles with a common
temperauture, :math:`T`, then it is possible to define energy states of
the combined system in the form

.. math:: E~{Ai} + A~{Bj}

which have a combined partition function,

.. math:: Z~{AB} = \sum_i \sum_j e^{- \beta E~{Ai} - \beta E~{Bj}}

 Now consider :math:`Z` energies in each state, :math:`A` and :math:`B`,
for example,

.. math::

   \begin{aligned}
     Z~{AB} &= \sum_{i=1}^2 \sum_{j=1}^2 e^{- \beta E~{Ai} - \beta E~{Bj}} \\
   &= e^{-\beta A~1} e^{- \beta B_1} + e^{-\beta A_2} e^{-\beta B_1} \\ & \quad {}+ e^{-\beta A_1} e^{- \beta B_2} + e^{-\beta A_1}e^{-\beta B_2} \\
   & = \qty( e^{-\beta E~A_1} + e^{-\beta E~{A_2}}) \qty( e^{-\beta E~{B_2}} + e^{-\beta E~{B_{2}}} ) \\ &= Z~A Z~B\end{aligned}

 Thus the partition function of the combined weakly interacting system
is the product of the individual partition functions, and since

.. math::

   \label{eq:22}
     F = - k~B T \log(Z) = -k~B T \log(Z~A Z~B) = F~A + F~B

 This multiplicative property of the partition functions is useful for a
range of complex systems, including the characterisation of molecules’
energies.

Constructing a partition function
=================================

A 2-energy-level system with :math:`E_0=0` and :math:`E_1=E` 
-------------------------------------------------------------

We have

.. math:: Z = 1 + \exp(- \beta E)

so the probability of each state being occupied is

.. math::

   \begin{aligned}
    P_0 &= \qty( 1+ \exp(-\beta E))^{-1}, \\ P_1 &= \exp(- \beta E) \qty( 1+ \exp(-\beta E))^{-1} \end{aligned}

 Thus

.. math:: F = -k~B T \log(1+ \exp(-\beta T))

Spin-\ :math:`\half` particle in a magnetic field
-------------------------------------------------

The energies of a spin-half particle in a magnetic field,
:math:`\vec{B}`, will be

.. math:: \pm E = \pm \gamma B

corresponding to spin quantum numbers :math:`m \pm 1`, for
:math:`\gamma` the projected magnetic moment. Thus

.. math::

   \begin{aligned}
     Z &= \exp(\beta E) + \exp(- \beta E) \\ &= 2 \cosh(\beta E) \\
   U &= F + Ts \\ s &= \pdv{T} (k~B T \log(Z) ) \\
   U &= -k~B T \log(Z) - T \pdv{T} \qty( k~B T \log(Z)) \\ &= - k~B T \log(Z) + k~B T \log(Z) + k~B T^2 \pdv{T} \log(Z) \\ 
   \pdv{T} \log(Z) &= \frac{1}{Z} \pdv{Z}{T}= \frac{1}{Z} \pdv{T} \qty(2 \cosh(\frac{E}{k~B T}) ) \\
   &= \frac{2}{Z} \sinh( \frac{E}{k~B T}) \qty( - \frac{E}{k~B T^2} ) \\
   &= - \frac{E}{k~B T^2} \tanh( \beta E) \\
   U &= - E \tanh(\beta E) \\ &= - \gamma \beta \tanh(\frac{ \gamma \beta }{k~B T} )\end{aligned}

 The mean magnetic moment can be found as

.. math::

   \begin{aligned}
     \ev{m} &= \sum_i^2 P_i m_i = \gamma P_+ + (- \gamma) P_- \\
   &= \gamma \qty[ \frac{1}{Z} \exp(\frac{\gamma B}{k~B T}) - \frac{1}{Z} \exp- \frac{\gamma B}{k~B T}] \\
   &= 2 \frac{\gamma}{Z} \sinh( \frac{\gamma B}{k~B T} ) \\
   &= \gamma \tanh( \frac{\gamma B}{k~B T})\end{aligned}

 Thus

.. math::

   \label{eq:1}
     U = - \ev{m} B

 which is what we expect. In the case that
:math:`\frac{\gamma B}{k~B T}` is very small, so in the case
:math:`T \gg 1` or :math:`B \ll 1`, then

[Curie Law] [eq:2] ~

The harmonic oscillator
=======================

From both quantum mechanics and a simple analogy to standing waves in a
fixed volume, the energy of a fixed oscillator is

.. math:: E_n = \qty(n+\half) h \nu, \quad \text{for}\ n \in \mathbb{N}

 with :math:`\nu` the frequency of the oscillation. Then the partition
function can be found

.. math::

   \begin{aligned}
     Z &= \sum^{\infty}_{n=0} \exp( - \frac{(n+\half) h \nu}{k~B T} )\\
   &= \exp( - \half \frac{h \nu}{k~B T} ) \sum \exp(- \frac{h \nu}{k~B T})^n 
   \intertext{Using the relation $\sum_{n=0}^{\infty} x^a = (1-x)^{-1}$}
   &= \frac{\exp(- \half \frac{h \nu}{k~B T})}{1 - \exp( - \frac{h \nu}{k~B T}) }\\
   &= \frac{\exp( - \frac{\Theta~\nu}{ 2 T})}{ 1- \exp(-\frac{\Theta~\nu}{T})}
   \intertext{having defined the vibrational temperature,
   \begin{equation}
     \label{eq:3}
     \Theta = \frac{h \nu}{k~B}
   \end{equation}
   }
   Z &= \frac{1}{\exp( \frac{\Theta~\nu}{2 T}) - \exp( - \frac{\Theta_{\nu}}{2 T}) } \\
   &= \frac{1}{2 \sinh( \frac{\Theta~\nu}{2 T} )}\end{aligned}

 Armed with the partition function it is possible to find any
thermodynamic property of the system, for example

.. math:: U = k~B T^2 \dv{t} \log(Z)

 So

.. math::

   \begin{aligned}
     Z &= \exp(- \frac{\Theta~\nu}{2 T}) \qty( 1 - \exp(- \frac{\Theta~\nu}{T}) )^{-1} \\
   \log(Z) &= - \frac{\Theta~\nu}{2 T} - \log( 1 - \exp(- \frac{\Theta~\nu}{T} ) ) \\
   \dv{T} \log(Z) &= \frac{\Theta~\nu}{2T^2} - \frac{1}{1-\exp(\frac{\Theta~\nu}{T})} \qty[ - \qty( \frac{\Theta~\nu}{T}  ) \exp(- \frac{\Theta~\nu}{T}) ] \\
   &= \frac{\Theta~\nu}{2 T^2} + \frac{\exp(- \frac{\Theta~\nu}{T})}{1 - \exp( \frac{\Theta~\nu}{T} )} \frac{\Theta~\nu}{T^2} \\
   U &= k~B T^2 \dv{T} \log(Z) \\
   &= \half k~B \Theta_{\nu} + k~B \Theta_\nu \frac{1}{\exp( \frac{\Theta~\nu}{T}) - 1}\\
   &= \half h \nu + \frac{h \nu}{\exp( \frac{\Theta~\nu}{T}) -1}
   \intertext{in the high temperature limit $\Theta~\nu/T \ll 1$}
   U & \approx  \half h \nu + \frac{h \nu}{1 + \frac{h \nu}{k~B T} -1} \\
   & \approx \half h \nu + k~B T \\
   & \approx k~B T
   \intertext{which is the classical two-dimensional result. \\In the low temperature limit we assume $\Theta \nu / T \gg 1$}
   U & \approx \hal h \nu + h \nu \exp( - \frac{\Theta~\nu}{T}) \end{aligned}

 So as :math:`\theta_{\nu}/T \to \infty` we get

.. math::

   \label{eq:4}
     U \approx \text{zero point energy}

 In classical thermodynamics the heat capacity, :math:`C_{V}`, is
constant, that is :math:`\dv{t} C_V = 0` but here

.. math::

   \begin{aligned}
     C_V &= \dv{U}{T} \approx h \nu \qty( \frac{\Theta_{\nu}}{T^2}) \exp(- \frac{\Theta_{\nu}}{T}) \\
   &= \frac{h \nu \Theta_{\nu}}{T^2} \exp(- \frac{h \nu}{k~B T}) \to 0 \ \text{as} \ T \to 0\end{aligned}

Rotational temperature
======================

Consider a rigid rotator with a Hamiltonian

.. math::

   \label{eq:23}
     H = \frac{L^2}{2 I}

 for :math:`L` the total angular momentum, and :math:`I` the moment of
inertia. From quantum mechanics,

.. math::

   \label{eq:24}
     E_l = \half \hbar^2 \frac{l(l+1)}{I}

 is the energy o the :math:`l`\ th state, with :math:`l` the angular
momentum quantum number, and a total of :math:`2l +1` states with
different :math:`m_l`, since :math:`m_l
\in [-l, l]`, and :math:`m_l \in \mathbb{Z}`. As a result each state has
a :math:`2l+1` degeneracy, and we can construct a partition function,

.. math::

   \label{eq:25}
     Z = \sum_i g_i \exp(- \beta E_i )

 with :math:`g_i` the degeneracy (algebraic multiplicity) of the
:math:`i`\ th state, so

.. math::

   \begin{aligned}
     \label{eq:26}
     Z &= \sum_{l=0}^{\infty} (2 l + 1) \exp( \frac{\hbar^2 l(l+1)}{2 I k~B T} )\\
   \label{eq:27}
   &= \sum_{l=0}^{\infty} (2l+1) \exp( - \frac{l(l+1)}{T} \Theta~r )\end{aligned}

for

.. math::

   \label{eq:28}
     \Theta~r = \frac{\hbar^2}{2 I k~B}

 the rotational temperature. The general situation is intractable, so
let’s look at the high and low temperature cases.

First consider the high temperature case, :math:`\Theta~r \ll T`, so the
summation can be replaced by an integral, assuming that there are a
large enough number of states to make a continuum approximation valid.
Then

.. math:: \sum_{l=0}^{\infty} \to \int_0^{\infty} \dd{l}

and let :math:`\lambda
= l + \half`, so :math:`l = \lambda - \half`, and
:math:`l(l+1) = \lambda^2 -
\frac{1}{4}`, so :math:`2l+1 = 2 \lambda`, thus

.. math::

   \int_{\half}^{\infty} 2 \lambda \exp[- \qty(- \lambda^2 - \frac{1}{4}
   \frac{\Theta~r}{T} )] \dd{\lambda}

 The we can construct the partition function

.. math::

   \begin{aligned}
     Z &= \exp( \frac{\Theta~r}{4 T} ) \int_{\half}^{\infty} 2 \lambda \exp( - \frac{\lambda^2 \Theta~r}{T} ) \dd{\lambda} \\ 
   & \approx \int_{\half}^{\infty} 2 \lambda \exp( - \frac{\lambda^2 \Theta~r}{T} ) \dd{\lambda} \\
   & = \frac{T}{\Theta~r} \qty[ - \exp( - \frac{\lambda^2 \Theta~r}{T} )]^{\infty}_{\half} \\
   & = - \frac{T}{\Theta~r} \qty[ 0 - \exp( - \frac{\Theta~r}{4 T} ) ] \\
   Z & \approx \frac{T}{\Theta~r}\end{aligned}

We can then find :math:`U`,

.. math::

   \begin{aligned}
     U &= k~B T^2 \dv{T}\qty( \log(Z) ) \\
   &= k~B T^2 \dv{T}\qty( \log(T) - \log(\Theta~r) ) \\ &= k~B T\end{aligned}

In the low temperature limit, :math:`\Theta~r \gg T`, so the first few
terms can be taken alone from the discrete summation—the continuum
assumption clearly isn’t valid since the expansion varies fast for
successive :math:`l` values. Thus

.. math::

   \label{eq:29}
     Z = 1 + 3 \exp( - \frac{2 \Theta~r}{T} )

 so

.. math:: \log(Z) = \log(1 + 3 \exp( - \frac{2 \Theta~r}{T} ) ) \approx 3 \exp(- \frac{2 \Theta~r}{T})

 Then

.. math::

   \begin{aligned}
   U &= k~B T^2 \dv{T} \log(Z) \\ 
   &= k~B T^2 \qty( \frac{6 \Theta~r}{T^2} \exp( - \frac{2 \Theta~r}{T}) ) \\
   &= 6 k~B \Theta~r \exp( - \frac{2 \Theta~r}{T} ) \\
   &= 6 \frac{\hbar^2}{2 I} \exp( - \frac{\Theta~r}{T}) \end{aligned}

 and

.. math::

   \begin{aligned}
     C_V = \dv{U}{T} &= \dv{T} \qty( 6 k~B \Theta~R \exp( - \frac{2 \Theta~r}{T} ) ) \\
   &= 6 k~B \Theta~r \frac{2 \Theta~r}{T^2} \exp( - \frac{2 \Theta~r}{T} )\end{aligned}

 and clearly :math:`C_V \to 0` as :math:`T \to 0`.

Translational temperature
=========================

A single particle in a be can be characterised with standing waves, with
wavelengths which increment as dictated by quantum mechanics, leading to
the quantisation based upon the wavenumber :math:`k`, for :math:`k = n
\pi/a`, :math:`n \in \mathbb{N}`. These states have energy

.. math::

   E = \frac{\hbar^2 k^2}{2 \pi n} = \frac{\hbar^2}{2 \pi n} \frac{n^2
     \pi^2}{a^2}

Generalising this to three dimensions, with :math:`\vec{k}
= \qty( k_x, k_y, k_z)` which leads to

.. math:: k^2 = k_x^2 + k_y^2 + k_z^2

 The energy of a particle in a box is

.. math::

   E = \frac{\hbar^2}{2 m} \qty( \frac{\pi}{a})^2 (n_1^2 + n_2^2 +
   n_3^2) = k~B \Theta~t (n_1^2 + n_2^2 + n_3^2)

 defining the translational temperature,

.. math::

   \label{eq:30}
     \Theta~t = \frac{\hbar^2}{2 m k~B} \qty( \frac{\pi}{a})^2

 so the partition function is then

.. math::

   \begin{aligned}
     \label{eq:31}
     Z &= \sum_{n_1} \sum_{n_2} \sum_{n_3} \exp[ - \frac{\Theta~t}{T}  (n_1^2 + n_2^2 + n_3^2) ] \nonumber\\
   &= \qty[ \sum_1^{\infty} \exp( - \frac{\Theta~t}{T} n^2 )]^3\end{aligned}

Again, if :math:`T > \Theta~t` the sum contains many terms, and we can
go to a continuum description, with

.. math:: \sum_1^{\infty} \to \int_0^{\infty} \exp(- \frac{\Theta~t}{T} n^2 ) \dd{n}

 and noting the relation

.. math:: \int_0^{\infty} \exp(-a x^2) \dd{x} = \half \sqrt{\frac{\pi}{a}}

 then

.. math:: \int_0^{\infty} \exp(- \frac{\Theta~t n^2}{T} ) \dd{n} = \half \sqrt{\frac{\pi T}{\Theta~T}} = \sqrt{\frac{\pi T}{4 \Theta~t}}

 and so

.. math:: Z = \qty[\frac{\pi T}{4 \Theta~t}]^{\frac{3}{2}}

 and

.. math::

   \begin{aligned}
     F &= - k~B T \log(Z) \\ &= - k~B T \log[ \qty( \frac{\pi T}{4 \Theta~t})^{\frac{3}{2}}] \\
   \dd{F} &= - s \dd{T} - p \dd{V} \\
   s &= - \eval{\pdv{F}{T}}_V = k~B \log(Z) + \frac{3}{2} k~B T \frac{4 \Theta~t}{\pi T} \frac{\pi}{4 \Theta~t} \\ &= \frac{3}{2} k~B + k~B \log(Z)\end{aligned}

 and

.. math:: p = - \eval{ \pdv{F}{V}}_T = \frac{k~B T}{V}

 giving the ideal gas law.

We can also write that the partition function must be :math:`Z =
\frac{V}{\Lambda^3}` for :math:`\Lambda \in \mathbb{R}` and

.. math:: \Lambda = \qty( \frac{\hbar^2}{2 \pi k~B m T} )^{\half}

with :math:`\Lambda` the thermal deBroglie wavelength for a temperature
:math:`T`.

Definitions
===========

States
------

[Macrostate] A macrostate is a description of a system which can be
described by a few parameters, for example, temperature, pressure,
internal energy, and volume.

[Microstate] A microstate is a detailed description of the constituent
components of a macrostate, e.g.

-  Classically, the position and momentum of each particle in the state;

-  Quantum mechanically, the state vector for each particle.

[pos:averageover] We can identify the macroscopic parameters with the
average at a given time over the set ensemble of microstates compatible
with the macroscopic state and the environment of the system.

[pos:equalrep] For a given set of macroscopic parameters all quantum
states consistent with this set have equal representation (i.e.
weighting or probability) in the microcanonical ensemble.

[Averaging Postulate] All accessible microstates are equally probable.

Ensembles
---------

[Microcanonical Ensemble] The microcanonical ensemble represents the
possible microstates of a mechanical system which have the same fixed
total energy, and particle number. All elements have the same volume,
particle number, and total energy.

[Canonical Ensemble] This ensemble describes a closed system which is in
contact with a heat bath. The total energy of each microstate is not
constrained to be identical, with each system weighted by the Boltzmann
factor. The volume, particle number, and temperature are fixed.

[Grand Canonical Ensemble] In this ensemble neither energy nor particle
number are fixed, so temperature and chemical potential must be
specified. This describes an open system.

Steps to model a system
-----------------------

Problems in statistical modelling can be handled in broadly the same
way.

#. Solve the one-particle problem

#. Enumerate all of the possible distributions

#. Count the number of microstates which are in each distribution

#. Find the average distribution

Examples of Microcanonical Distributions
----------------------------------------

| [Spin-1 Particle] Consider a single spin-1 particle in a magnetic
  field :math:`\vec{B}`. There are three possible states, which have
  energies :math:`E =
    \set{- \gamma m B}` for :math:`m=\set{-1, 0, 1}`.
| If :math:`B=0` then :math:`E~{m}=0` for all :math:`m`, and so there is
  equal probability of being in any :math:`m` state, thus the
  probability of each state is :math:`P = 1/3`. If
  :math:`\vec{B} \neq 0` we cannot assign probabilities without a
  constraint; total energy, so the state is not microcanonical.
| If :math:`E=0` for :math:`\vec{B}` the system must have :math:`m=0`
  with :math:`P=1`.

[Two spin-1 particles] Consider two spin-1 particles, :math:`x` and
:math:`y` which are distinguishable. What is the probability of
:math:`m_x=+1` while :math:`m_y=-1`, i.e. that the system has a state
vector :math:`(+1, -1)`?

In the case that :math:`B=0` the state :math:`(+1, -1)` is one of 9
possible states, and so :math:`P=\frac{1}{9}`. If, however,
:math:`B\neq 0`, we need to know :math:`E`, so again, the state is
non-microcanonical. If :math:`E=0` the states can be :math:`(+1, -1)`,
:math:`(-1, +1)`, or :math:`(0,0)`, so :math:`P=\frac{1}{3}`.

[One dimensional polymer molecule] Consider a molecule consisting of
:math:`A` links, each of length :math:`b`. Each link may have one of two
directions, denoted :math:`\rightarrow` and :math:`\leftarrow`. Each
orientation has the same energy, so the ensemble is microcanonical, and
this is an ideal microcanonical system.

Let one end of the polymer be at :math:`x=0` and the other at
:math:`x = Lb`, for :math:`-A \leq L \leq A`. Recalling postulate
[pos:averageover], the macroscopic length will be the average over all
of the ensemble. From postulate [pos:equalrep] we know that all of the
:math:`2^A` microstates are equally probable, but this does not imply
all macrostates are equally probable.

A system of three links has :math:`2^3` possible configurations, so

+-------------------------+-------------------------+-------------------------+-------------------------+
|                         |                         |                         |                         |
+-------------------------+-------------------------+-------------------------+-------------------------+
|                         |                         |                         |                         |
+-------------------------+-------------------------+-------------------------+-------------------------+
|                         |                         |                         |                         |
+-------------------------+-------------------------+-------------------------+-------------------------+
| :math:`L = -3`          | :math:`L = -1`          | :math:`L =+1`           | :math:`L=+3`            |
+-------------------------+-------------------------+-------------------------+-------------------------+
| :math:`P=\frac{1}{8}`   | :math:`P=\frac{3}{8}`   | :math:`P=\frac{3}{8}`   | :math:`P=\frac{1}{8}`   |
+-------------------------+-------------------------+-------------------------+-------------------------+

Clearly there are a preferred set of orientations giving a length
:math:`|L|=1` for the macroparameter. We can generalise this result by
applying the binomial theorem.

The total number of configurations with a fixed end at :math:`x = Lb` is
given by a binomial distribution (see appendix [sec:binom-distr]) such
that

.. math::

   \label{eq:7}
       \Omega(L) = \frac{A!}{a_+! a_-!}

 where :math:`a_+` is the number of links pointing to the right, and
:math:`a_-` the number pointing to the left, such that

.. math:: a_+ + a_- = A, \quad a_+ - a_- = L

 Now,

.. math::

   \label{eq:8}
       \Omega(L) = \frac{A!}{\qty(\frac{A+L}{2})! \qty(\frac{A-L}{2})!}

 Then, taking Stirling’s approximation (see appendix [sec:stirl-appr])

.. math::

   \label{eq:9}
       P\qty(\frac{L}{A}) = \frac{\Omega(L)}{2^A} = \qty(\frac{2}{\pi a})^{\half} \exp( - \frac{L^2}{2A} )

 which has the form of a Gaussian distribution (which follows by the
Central Limit Theorem). This indicates a most probable length of
:math:`L=0`.

Canonical Distributions
=======================

In a microcanonical ensemble the energy of the state takes a
:math:`\delta`-function form, but in a canonical ensemble, the energy of
each state is not the same—there is a distribution; we only know the
total energy of the system, which is constrained by the heat bath.

Although the microcanonical ensemble can be very useful it doesn’t occur
often in real physical systems. A better approximation is obtained by
considering systems with a fixed number of particles, volume, and
temperature, held in a heat bath which defines the temperature,
:math:`T`. The system is isolated, as the heat bath is impermeable to
particles, but energy is transferred to maintain the temperature. (e.g.
the average mark in a distribution of test results being fixed;
individuals can have a range of marks not equal to the average, thus the
systems within the canonical ensemble have an energy constrained only by
the average.)

We can build insight into a canonical system by building it from smaller
microcanonical systems which contribute overall to the measurables. To
see this, consider a system of :math:`A` identical sub-systems sharing a
total energy :math:`E~{tot}`. Let :math:`E_i` denote the energy of the
:math:`i`-th state. If :math:`a_i` is the number of systems at any time
:math:`t` with energy :math:`E_i` then the set of numbers
:math:`\set{a_i}` satisfies

.. math:: \sum_i a_i = A

 and

.. math:: \sum_i a_i E_i = E~{tot} = AU = A \bar{E}

 for :math:`\bar{E} = U` the average energy of the sub-systems.

Any set of :math:`\set{a_i}` satisfying these constraints represents a
possible mode of the distribution of total energy :math:`E~{tot}` among
:math:`A` members of the ensemble. Any set :math:`\set{a_i}` satisfying
the constraints can be realised in a number of ways, e.g. A reshuffle
among those members of the ensemble with different energy values, and
thus obtain a state of the ensemble which is distinct from the original.
How many ways are there to do this?

Let :math:`\Omega` be the number of ways that a set can be arranged,
then

.. math::

   \label{eq:1}
     \Omega(\set{a_i}) = \frac{A!}{a_1! a_2! a_3! \cdots} = \frac{A!}{\prod_i a_i!}

Since all possible states of the ensemble are equally likely to occur
the frequency with which the distribution :math:`\set{a_i}` appears is
directly in proportion to :math:`\Omega(\set{a_i})`. Thus, the most
probable mode of distribution is the one maximising
:math:`\Omega(\set{a_i})`, which we denote :math:`\set{a_i^{*}}`. This
clearly satisfies the constraints, and for all proactical purposes it’s
the only one which we need to consider.

For large :math:`A` we expect :math:`\Omega` will be very strongly
peaked, so let’s maximise :math:`\Omega`, or, as it happens, maximise
:math:`\frac{\log(\Omega)}{A}`, and define

.. math:: H = \frac{\log(\Omega)}{A}

 We maximise :math:`H` subject to the constraints

.. math::

   \begin{aligned}
     \sum a_i &= A \\
   \sum a_i E_i &= E~{tot}\end{aligned}

.. math::

   \begin{aligned}
     H = \frac{\log(\Omega)}{A} &= \frac{1}{A} \log( \frac{A!}{a_1! a_2! \cdots}) \\
   &= \frac{1}{A} \qty[ \log(A!) - \log(a_1! a_2! \cdots)]\\
   &= \frac{1}{A} \qty[ A \log(A) - A - \floor{\sum_i a_i \log(a_i) - a_i}]\end{aligned}

Now we define the probability of being in state :math:`a_i` as

.. math:: P_i = \frac{a_i}{A}

 thus :math:`\sum P_i = 1`.

So

.. math::

   \begin{aligned}
     A &= \frac{1}{A} \qty[ A \log(A) - A - \qty{ \sum_i A P_i \log(A P_i) - A P_i}] \\
   &= \frac{1}{A} \qty[ A \log(A) - A - A \qty{ \sum_i P_i \qty[\log(A) + \log(P_i)] - P_i}]\end{aligned}

 Cancellations mean that

.. math:: H = - \sum P_i \log(P_i)

 which needs to be maximised.

Let :math:`\alpha`, :math:`\beta` be Lagrange multipliers, and

.. math:: f = - \sum_i P_i \log(P_i) + \alpha(1 - \sum_i P_i) + \beta( u - \sum_i P_i E_i )

 We then form the differential,

.. math::

   \dd{f} = \sum_i \set{ - \log(P_i) - 1 - \alpha - \beta E_i}
   \dd{P_i} = 0

 This must hold for all values of :math:`i`, so we can set each side to
equal :math:`0` independently,

.. math:: \therefore - \log(P_i) - 1 -\alpha - \beta E_i =0 \quad \forall i

.. math:: P_i = \exp( -1 -\alpha -\beta E_i)

 and we also know :math:`\sum P_i=1`, so

.. math::

   \begin{aligned}
     \sum \exp(-1 -\alpha - \beta E_i) &= 1 \\
     e^{-(1+\alpha)} \sum e^{-\beta E_i} &= 1 \\
     e^{-(1+\alpha)} =  \qty(\sum e^{-\beta E_i})^{-1} &= \frac{1}{Z} \end{aligned}

 where :math:`Z = \sum e^{-\beta E_i}` is the partition function for the
system, the sum over all states weighted by the Boltzmann factor. Thus

.. math::

   \label{eq:10}
     P_i = \frac{1}{Z} \exp(-\beta E_i)

 This can be generalised to reflect the fact that there are several ways
to reach the same energy state, and so we adopt the notation

.. math::

   \label{eq:11}
     Z = \sum_i g_i \exp(- \beta E_i)

 for :math:`g_i` the multiplicity (or degeneracy) of the :math:`i`\ th
state.

The partition function, :math:`Z`, is the central equation of
statistical mechanics, and knowledge of it allows the derivation of the
major results of thermodynamics.

Major results using :math:`Z`
-----------------------------

*The mean energy in a canonical ensemble* is given as

.. math:: \ev{E} = \sum P_i E_i = \sum \frac{1}{Z} E_i \exp(-\beta E_i)

 Considering that

.. math:: \pdv{\beta} \log(Z) = \frac{1}{Z} \pdv{\beta}(Z)

 and

.. math:: Z = Z = \sum_i \exp(- \beta E_i)

 then

.. math:: \pdv{\beta} \log(Z) = - \frac{1}{Z} \sum_i E_i \exp(- \beta E_i)

 and so

.. math::

   \label{eq:12}
    U = \ev{E} = - \pdv{\beta} \log(Z)

*The energy fluctuations in a canonical ensemble* are

.. math::

   \begin{aligned}
   \Delta E^2 &= \ev{E_i - \ev{E}}^2 = \ev{E_i^2 - 2 E_i \ev{E} + \ev{E}^2} \\
    &= \ev{E_i}^2 - \ev{E}^2 = \sum_i P_i E_i^2 - \qty( \sum_i P_i E_i )^2 \\
    &= \sum_i \frac{1}{Z} \exp(-\beta E_i) E_i^2 - \qty( \sum_i \frac{1}{Z} \exp(- \beta E_i) E_i )^2 \tag{\(\star\)}\end{aligned}

 Noting that

.. math::

   \begin{aligned}
     - \pdv{U}{\beta} &= - \pdv{\beta}( \pdv{Z}{\beta} \frac{1}{Z} ) \\ 
   &= \pdv{\beta} \qty[ \qty(\sum_i e^{-\beta E_i})^{-1} \sum_i \qty(-E_i e^{\beta E_i})] \\
   &= \star\end{aligned}

 then

.. math::

   \label{eq:13}
     \Delta E^2 = - \pdv{U}{\beta}

 which is positive definite.

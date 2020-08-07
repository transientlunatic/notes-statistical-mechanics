*******************************
Maths for Statistical Mechanics
*******************************

Important Distributions
=======================

Binomial Distribution
---------------------

For a system with two states the binomial distribution models the number
of one state compared to the other when taking :math:`n` samples with
replacement, given a total population :math:`N`. So, for :math:`n`
systems the probability that :math:`k` are in one state is

.. math::

   \label{eq:5}
     {n \choose k} = \frac{n!}{k!(n-k)!}

Multinomial Distribution
------------------------

The multinomial distribution is a generalisation of the binomial
distribution in which a system may be in more than two possible states.
The probability that :math:`x_i` systems are in state :math:`i`, where
there are :math:`p_i` is the probability of a system being in state
:math:`i`, and for :math:`n` systems, with :math:`k` possible states,
then

.. math::

   \label{eq:6}
     \begin{split}
       p(x_1, \dots, \x_k; n, p_1, \dots, p_k) = \Pr(X_1 = x_1, \dots, X_k = x_k) \\ = \frac{n!}{x_1!\cdots x_k!} p_1^{x_1}\cdots p_k^{x_k}
     \end{split}

Factorials
==========

Stirling’s Approximation
------------------------

Stirling’s Approximation is a means of approximating large factorials,
and is expressed as

.. math::

   \label{eq:1}
     \log{n!} = n \log(n) - n + \mathcal{O}(log(n))

which can be expressed more precisely as

.. math::

   \label{eq:2}
     n! \approx \sqrt{2 \pi n} \qty( \frac{n}{e} )^n

The gamma function
------------------

The gamma function is an extension of the factorial function to apply to
real and complex numbers. That is, if :math:`n \in \mathbb{N}`,

.. math:: \Gamma(n) = (n-1)!

 If the real part of a complex number, :math:`t` is positive, then

.. math::

   \label{eq:3}
     \Gamma(t) = \int_0^{\infty} x^{t-1} e^{-x} \dd{x}

 and has the factorial property,

.. math::

   \label{eq:4}
     \Gamma(t+1) = t \Gamma(t)

The Method of Lagrange Multipliers
==================================

The method of Lagrange multipliers is used to optimise functions subject
to constraints.

For any non-pathological function, :math:`f(x_1, \dots, x_n)`, and for
independent functions :math:`g_1(x_1, \dots, x_n), \dots g_m(x_1, \dots,
  x_n)`, then, the local extrema of :math:`f`, subject to these
contraints can be found as the stationary points of the function

.. math:: f + \lambda_1 g_1 + \lambda_2 g_2 + \cdots + \lambda_m g_m

 where :math:`\lambda_1, \dots, \lambda_m` are real scalars called
Lagrange multipliers.

To find the extrema of

.. math:: f(x,y) = x+y

 on an ellipse

.. math:: 4x^2 + y^2 = 80

We then want the critical points of the function

.. math:: h(x, y) = f(x,y) + \lambda g(x,y) = x+y + \lambda (4 x^2 + y^2 -80)

 Thus :math:`h_x= 1+8 \lambda x` and :math:`h_y = 1+ 2 \lambda y`,
setting :math:`h_x =
h_y =0`, then

.. math:: x = - \frac{1}{8} \lambda\ \quad y = - \half \lambda = 4x

 Thus there is a critical point at :math:`(x,y)=(x, 4x)`; substituting
the constraint,

.. math:: 4x^2 + (4x)^2 = 80 \implies x = \pm 2, y = \pm 8

 So there are critical points at :math:`(2,8)` and :math:`(-2, -8)`,
respectively a maximum and a minimum.

Lagrange multipliers work on the basis that at a maximum, :math:`f(x,y)`
of :math:`f` we can not increase in any direction of a neighbouring
point; if we could we would move that way to a higher value, and not be
at a maximum. The extreme value of :math:`f` along the function of the
constraint can therefore only occur when the contours of the function
:math:`f` are parallel to the constraint. Gradients are perpendicular to
the contours, so if the function is parallel to the contours then the
gradients of both the constraint and the function must be either
parallel or antiparallel, so

.. math:: \nabla f = - \lambda \nabla g

for a constant :math:`\lambda`. Thus :math:`\nabla(f + \lambda g)=0`.

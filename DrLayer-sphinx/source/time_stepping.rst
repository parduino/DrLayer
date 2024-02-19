Time Stepping
================================

Introduction
***************************************************

Background
***************************************************
In addition to varying the layer properties, another tool that comes in handy is a variation on the computational side. It involves varying the time step, i.e. the time it takes to repeat each computation. The defining rule for the iteration used in the time stepping procedure for Dr. Layer is the central difference method. It is not an exact procedure but it ensures that the iteration converges, achieves stability, and is close enough to the exact solution.

The central difference hinges on a finite difference approximation of velocity and acceleration. The central difference method will “blow up”, giving meaningless results, if the chosen time step is not small enough. Stability of the solution requires

    .. math::
        \frac{\Delta t}{T} < \frac{1}{\pi}

Where  Dt is the time for each iteration and T is the period (time it takes to complete one cycle of the input loading)

The steps below summarize the central difference procedure as it was programmed in Dr. Layer. (Check the time stepping theory for a better understanding of this process)

    1a. :math:`\bar{u_0} = \frac{p_0 - c \bar{u_0} - ku_0}{m}`

    1b. :math:`u_1 = u_0 - \Delta t \bar{u_0} - \frac{(\Delta t)^2}{2} \bar{u_0}`

    1c. :math:`k = \frac{m}{(\Delta t)^2} + \frac{c}{2\Delta t}`

    1d. :math:`a = \frac{m}{(\Delta t)^2} + \frac{c}{2\Delta t}`

    1e. :math:`b = k - \frac{2m}{(\Delta t)^2}`

computations for each time step I

    2a. :math:`p = p_i - au_{i-1} - bu_i`

    2b. :math:`u_{i+1} = \frac{p_i}{k}`

    2c. :math:`\bar{u_i} = \frac{u_{i+1} - u_{i-1}}{2 \Delta t}`

    2d. :math:`\bar{u_i} = \frac{u_{i+1} - 2u_i + u_{i-1}}{(\Delta t)^2}`

Repetition for each time step

Substitute :math:`i+1` for :math:`i` and repeat the steps 2a, 2b and 2c.

Objective
***************************************************
It shows on the computation side of the output how varying the time step can significantly affect the speed of result output and stability of our analysis.

Things to Do
***************************************************
#. Open the Dr. Layer program. By default we get twelve layers. The top six layers are hardwired into the system with a very fast velocity. The bottom six layers are hardwired with a very slow velocity.

#. By default we get a medium time step. Push the time increment button. Nothing exciting happens!

#. Go to the time step menu and change to large. Push the time increment button.

    <insert image>

#. Keeping the time step on large, go to the edit menu and select all, then change the wave speed to very slow. Push the time increment button.

#. Change the wave speed to different values. Change different parameters like damping, load type and the input frequency on the slider bar.

Observation
***************************************************
The numerical procedure becomes unstable at large time steps but it is still a function of the relationship :math:`\Delta t / T < 1 / \pi`

On Your Own
***************************************************
#. Determine by making general statements what role the input frequency (related to the period) plays in the stability of our analysis.

#. Determine by making general statements the effect of the wave speed through the layers on the stability of the layers.

#. Does damping have an effect on the stability of the analysis.

#. We know the relationship governing stability that relates :math:`T` and :math:`Dt`. Obtain the limiting values of :math:`T` that will cause instability.

    :math:`Dt (small) =`

    :math:`Dt (medium) =`

    :math:`Dt (large) =` 
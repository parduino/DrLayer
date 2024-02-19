Frequency Domain
================================

Introduction
***************************************************

Background
***************************************************
The time required for an undamped system to complete one cycle of free vibration is the natural period of vibration of the system. We shall represent this as :math:`T` in units of seconds. It is related to the natural circular frequency of vibration w with units of radians per second:

.. math:: 
    T = \frac{2\pi}{w}

The natural cyclic frequency of vibration :math:`f` which is implemented on the slider bar in Dr. Layer is given by the reciprocal value of :math:`T`. This frequency represents the number of completed cycles per second. The units are Hertz (:math:`Hz`). The frequency depends only on the mass and stiffness characteristics of the structure. This in effect means that the stiffer of two bodies with similar masses will posses a higher natural frequency and thus a shorter period. Conversely, the heavier of two bodies with the same stiffness will have a lower natural frequency. For linear systems these vibration properties are independent of the initial displacement and velocity.

Objective
***************************************************
After this exercise you will understand how the input frequency affects the type of wave travel obtained.

Things to Do
***************************************************
#. Open the Dr. Layer program. By default we get twelve layers. The top six layers are hardwired into the system with a very fast velocity. The bottom six layers are hardwired with a very slow velocity.

#. Starting with the set up above, move the cursor on the bottom left portion of the screen and push the time increment button to set up the wave motion.

#. Obtain the input period (:math:`T`) from the plot box as the time it takes to complete one cycle.

#. Vary the frequency on the slider bar and obtain the new period.

#. The fast fourier transform plot can be obtained by pushing the plot box button and clicking on the existing plot box. You should obtain a box as shown below.

    <insert image>

#. Change parameters to reflect the different wave speeds. What do you notice?

#. Try as many different combinations as possible and note the differences obtained in each combination.

Observation
***************************************************
The type of wave motion obtained is different for each input frequency employed. The shape of the fast fourier transform plot is also a function of the input frequency and the wave speed of travel along the different media.

On Your Own
***************************************************
Try different loading conditions and obtain the frequency values.


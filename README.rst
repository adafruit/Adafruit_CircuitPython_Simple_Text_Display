Introduction
============


.. image:: https://readthedocs.org/projects/adafruit-circuitpython-simple-text-display/badge/?version=latest
    :target: https://docs.circuitpython.org/projects/simple-text-display/en/latest/
    :alt: Documentation Status


.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/adafruit/Adafruit_CircuitPython_Simple_Text_Display/workflows/Build%20CI/badge.svg
    :target: https://github.com/adafruit/Adafruit_CircuitPython_Simple_Text_Display/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

A helper library for displaying lines of text on a display using displayio.


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_
* `Adafruit CircuitPython DisplayText <https://github.com/adafruit/Adafruit_CircuitPython_Display_Text>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.

This library works with any microcontroller with a built in display, or a microcontroller with an
external display connected.

`Purchase one from the Adafruit shop. <http://www.adafruit.com>`_


Usage Example
=============

This example takes the microcontroller CPU temperature in C and F, and displays it on the display
under the heading "Temperature Data!".

.. code-block:: python

    import microcontroller
    from adafruit_simple_text_display import SimpleTextDisplay

    temperature_data = SimpleTextDisplay(title="Temperature Data!", title_scale=2)

    while True:
        temperature_data[0].text = "Temperature: {:.2f} degrees C".format(
            microcontroller.cpu.temperature
        )
        temperature_data[1].text = "Temperature: {:.2f} degrees F".format(
            (microcontroller.cpu.temperature * (9 / 5) + 32)
        )
        temperature_data.show()

Documentation
=============

API documentation for this library can be found on `Read the Docs <https://docs.circuitpython.org/projects/simple-text-display/en/latest/>`_.

Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/adafruit/Adafruit_CircuitPython_Simple_Text_Display/blob/HEAD/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.

Documentation
=============

For information on building library documentation, please check out
`this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.

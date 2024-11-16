---
title: "Writing your first NWChemEx Plugin"
layout: splash
permalink: /developer/your_first_plugin/
toc: true
---

To make life easy the NWChemEx team has created a plugin template

.. code-block:: .py

   # If cookiecutter is not already installed
   pip install cookiecutter
   cookiecutter https://github.com/NWChemEx/PluginTemplate.git

You will then be prompted to answer two questions:

1. What is the name of project? This should be a human-readable stylized name.
2. What is the name of the project slug? This should be a filesystem-friendly
   name.
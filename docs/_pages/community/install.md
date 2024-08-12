---
title: "How to install NWChemEx"
layout: splash
permalink: /community/install/
toc: true
---

NWChemEx is a modular software package that can be extended with plugins. All
of these tutorials focus on building the core NWChemEx package 
[repository](https://github.com/NWChemEx/NWChemEx). Such an install will give
you SimDE (i.e., the NWChemEx software development kit), the core plugins
maintained by the NWChemEx authors, and the user interface.
{: .notice}

# Building from source

At present we only officially support building NWChemEx on Linux, or Mac. We
know that several developers have also built it on Windows using the 
[Windows Linux Subsystem](https://learn.microsoft.com/en-us/windows/wsl/about);
however, we do not officially support this.

This tutorial assumes familiarity with the terminal.
{: .notice}

## Step 0: Obtain build tools

TODO: Can we synchronize the versions with our CI/CD pipelines? Maybe a link?
{: .notice--info}

You will need:

1. A C++ compiler supporting the C++17 standard. We test with GCC 11 and 
Clang 14. Other versions may work, but we guarantee those.
2. CMake. We require 3.17 minimally, but test with 3.22.
3. Python 3.  We test with 3.10.

## Step 1: Obtain dependencies.

The NWChemEx build system will obtain a number of dependencies for you, but not
all of them. You will need to manually obtain the following common 
dependencies (clusters likely already have them; if you don't have them check
your package manager):

1. Boost Libraries. We test with 1.74.
2. An MPI implementation supporting version 3 of the MPI standard. We test with OpenMPI 4.1.2.
3. BLAS. We test with OpenBLAS.
4. LAPACK. We test with OpenLAPACK.

## Step 2: Obtain the NWChemEx source repository.

We recommend building in a workspace directory. This is simply a new directory
you create to hold the files we will create during this tutorial as well as
the source code you clone. By using a workspace it is easy to clean-up after
you are done (i.e., just delete the workspace). 
{: .notice--info}

Start by creating a workspace directory and changing to it:
```bash
mkdir nwx_workspace
cd nwx_workspace
```

Now we use `git` to obtain the NWChemEx source from GitHub:

```bash
git clone https://github.com/NWChemEx/NWChemEx
```

This command will clone the NWChemEx repository into a subdirectory named 
`NWChemEx`.

## Step 3: Prepare toolchain file

CMake best practices are to create a toolchain file which contains your build
settings. By convention this file is called `toolchain.cmake`. The minimum
contents of this file are:

```cmake
set()
```
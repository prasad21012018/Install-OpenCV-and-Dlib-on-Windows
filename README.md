# Install-OpenCV-and-Dlib-on-Windows
Install OpenCV 4.2.0 and Dlib 19.19.0 on Anaconda


C:\Windows\system32>python C:\ProgramData\Anaconda3\etc\keras\load_config.py  1>temp.txt

C:\Windows\system32>set /p KERAS_BACKEND= 0<temp.txt

C:\Windows\system32>del temp.txt

C:\Windows\system32>python -c "import keras"  1>nul 2>&1

C:\Windows\system32>if errorlevel 1 (
ver  1>nul
 set "KERAS_BACKEND=theano"
 python -c "import keras"  1>nul 2>&1
)

(base) C:\Windows\system32>conda
usage: conda-script.py [-h] [-V] command ...

conda is a tool for managing and deploying applications, environments and packages.

Options:

positional arguments:
  command
    clean        Remove unused packages and caches.
    config       Modify configuration values in .condarc. This is modeled
                 after the git config command. Writes to the user .condarc
                 file (C:\Users\prasa\.condarc) by default.
    create       Create a new conda environment from a list of specified
                 packages.
    help         Displays a list of available conda commands and their help
                 strings.
    info         Display information about current conda install.
    init         Initialize conda for shell interaction. [Experimental]
    install      Installs a list of packages into a specified conda
                 environment.
    list         List linked packages in a conda environment.
    package      Low-level conda package utility. (EXPERIMENTAL)
    remove       Remove a list of packages from a specified conda environment.
    uninstall    Alias for conda remove.
    run          Run an executable in a conda environment. [Experimental]
    search       Search for packages and display associated information. The
                 input is a MatchSpec, a query language for conda packages.
                 See examples below.
    update       Updates conda packages to the latest compatible version.
    upgrade      Alias for conda update.

optional arguments:
  -h, --help     Show this help message and exit.
  -V, --version  Show the conda version number and exit.

conda commands available from other packages:
  build
  convert
  debug
  develop
  env
  index
  inspect
  metapackage
  render
  server
  skeleton
  verify

(base) C:\Windows\system32>conda info --envs
# conda environments:
#
base                  *  C:\ProgramData\Anaconda3


(base) C:\Windows\system32>python --version
Python 3.7.4

(base) C:\Windows\system32>conda create --name envopencv-env python=3.7.4
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - python=3.7.4


The following NEW packages will be INSTALLED:

  ca-certificates    pkgs/main/win-64::ca-certificates-2020.1.1-0
  certifi            pkgs/main/win-64::certifi-2019.11.28-py37_0
  openssl            pkgs/main/win-64::openssl-1.1.1d-he774522_3
  pip                pkgs/main/win-64::pip-20.0.2-py37_1
  python             pkgs/main/win-64::python-3.7.4-h5263a28_0
  setuptools         pkgs/main/win-64::setuptools-45.1.0-py37_0
  sqlite             pkgs/main/win-64::sqlite-3.31.1-he774522_0
  vc                 pkgs/main/win-64::vc-14.1-h0510ff6_4
  vs2015_runtime     pkgs/main/win-64::vs2015_runtime-14.16.27012-hf0eaf9b_1
  wheel              pkgs/main/win-64::wheel-0.34.2-py37_0
  wincertstore       pkgs/main/win-64::wincertstore-0.2-py37_0


Proceed ([y]/n)? y

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate envopencv-env
#
# To deactivate an active environment, use
#
#     $ conda deactivate


(base) C:\Windows\system32>activate envopencv-env

C:\Windows\system32>set "KERAS_BACKEND="

(envopencv-env) C:\Windows\system32>conda
usage: conda-script.py [-h] [-V] command ...

conda is a tool for managing and deploying applications, environments and packages.

Options:

positional arguments:
  command
    clean        Remove unused packages and caches.
    config       Modify configuration values in .condarc. This is modeled
                 after the git config command. Writes to the user .condarc
                 file (C:\Users\prasa\.condarc) by default.
    create       Create a new conda environment from a list of specified
                 packages.
    help         Displays a list of available conda commands and their help
                 strings.
    info         Display information about current conda install.
    init         Initialize conda for shell interaction. [Experimental]
    install      Installs a list of packages into a specified conda
                 environment.
    list         List linked packages in a conda environment.
    package      Low-level conda package utility. (EXPERIMENTAL)
    remove       Remove a list of packages from a specified conda environment.
    uninstall    Alias for conda remove.
    run          Run an executable in a conda environment. [Experimental]
    search       Search for packages and display associated information. The
                 input is a MatchSpec, a query language for conda packages.
                 See examples below.
    update       Updates conda packages to the latest compatible version.
    upgrade      Alias for conda update.

optional arguments:
  -h, --help     Show this help message and exit.
  -V, --version  Show the conda version number and exit.

conda commands available from other packages:
  build
  convert
  debug
  develop
  env
  index
  inspect
  metapackage
  render
  server
  skeleton
  verify

(envopencv-env) C:\Windows\system32>conda list
# packages in environment at C:\ProgramData\Anaconda3\envs\envopencv-env:
#
# Name                    Version                   Build  Channel
ca-certificates           2020.1.1                      0
certifi                   2019.11.28               py37_0
openssl                   1.1.1d               he774522_3
pip                       20.0.2                   py37_1
python                    3.7.4                h5263a28_0
setuptools                45.1.0                   py37_0
sqlite                    3.31.1               he774522_0
vc                        14.1                 h0510ff6_4
vs2015_runtime            14.16.27012          hf0eaf9b_1
wheel                     0.34.2                   py37_0
wincertstore              0.2                      py37_0

(envopencv-env) C:\Windows\system32>conda install -c anaconda numpy
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - numpy


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    blas-1.0                   |              mkl           6 KB  anaconda
    ca-certificates-2020.1.1   |                0         165 KB  anaconda
    certifi-2019.11.28         |           py37_0         157 KB  anaconda
    icc_rt-2019.0.0            |       h0cc432a_1         9.4 MB  anaconda
    intel-openmp-2020.0        |              166         1.9 MB  anaconda
    mkl-2019.5                 |              281       158.3 MB  anaconda
    mkl-service-2.3.0          |   py37hb782905_0         200 KB  anaconda
    mkl_fft-1.0.15             |   py37h14836fe_0         137 KB  anaconda
    mkl_random-1.1.0           |   py37h675688f_0         270 KB  anaconda
    numpy-1.18.1               |   py37h93ca92e_0           5 KB  anaconda
    numpy-base-1.18.1          |   py37hc3f5095_1         4.8 MB  anaconda
    openssl-1.1.1              |       he774522_0         5.7 MB  anaconda
    six-1.14.0                 |           py37_0          27 KB  anaconda
    ------------------------------------------------------------
                                           Total:       181.2 MB

The following NEW packages will be INSTALLED:

  blas               anaconda/win-64::blas-1.0-mkl
  icc_rt             anaconda/win-64::icc_rt-2019.0.0-h0cc432a_1
  intel-openmp       anaconda/win-64::intel-openmp-2020.0-166
  mkl                anaconda/win-64::mkl-2019.5-281
  mkl-service        anaconda/win-64::mkl-service-2.3.0-py37hb782905_0
  mkl_fft            anaconda/win-64::mkl_fft-1.0.15-py37h14836fe_0
  mkl_random         anaconda/win-64::mkl_random-1.1.0-py37h675688f_0
  numpy              anaconda/win-64::numpy-1.18.1-py37h93ca92e_0
  numpy-base         anaconda/win-64::numpy-base-1.18.1-py37hc3f5095_1
  six                anaconda/win-64::six-1.14.0-py37_0

The following packages will be UPDATED:

  openssl              pkgs/main::openssl-1.1.1d-he774522_3 --> anaconda::openssl-1.1.1-he774522_0

The following packages will be SUPERSEDED by a higher-priority channel:

  ca-certificates                                 pkgs/main --> anaconda
  certifi                                         pkgs/main --> anaconda


Proceed ([y]/n)? y


Downloading and Extracting Packages
six-1.14.0           | 27 KB     | ############################################################################ | 100%
openssl-1.1.1        | 5.7 MB    | ############################################################################ | 100%
mkl_fft-1.0.15       | 137 KB    | ############################################################################ | 100%
icc_rt-2019.0.0      | 9.4 MB    | ############################################################################ | 100%
mkl_random-1.1.0     | 270 KB    | ############################################################################ | 100%
mkl-service-2.3.0    | 200 KB    | ############################################################################ | 100%
blas-1.0             | 6 KB      | ############################################################################ | 100%
intel-openmp-2020.0  | 1.9 MB    | ############################################################################ | 100%
numpy-base-1.18.1    | 4.8 MB    | ############################################################################ | 100%
mkl-2019.5           | 158.3 MB  | ############################################################################ | 100%
certifi-2019.11.28   | 157 KB    | ############################################################################ | 100%
numpy-1.18.1         | 5 KB      | ############################################################################ | 100%
ca-certificates-2020 | 165 KB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>conda install -c anaconda scipy
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - scipy


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    scipy-1.4.1                |   py37h9439919_0        15.2 MB  anaconda
    ------------------------------------------------------------
                                           Total:        15.2 MB

The following NEW packages will be INSTALLED:

  scipy              anaconda/win-64::scipy-1.4.1-py37h9439919_0


Proceed ([y]/n)? y


Downloading and Extracting Packages
scipy-1.4.1          | 15.2 MB   | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>conda install -c anaconda matplotlib
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - matplotlib


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    cycler-0.10.0              |           py37_0          13 KB  anaconda
    freetype-2.9.1             |       ha9979f8_1         470 KB  anaconda
    icu-58.2                   |   vc14hc45fdbb_0        21.9 MB  anaconda
    jpeg-9b                    |   vc14h4d7706e_1         313 KB  anaconda
    kiwisolver-1.1.0           |   py37ha925a31_0          59 KB  anaconda
    libpng-1.6.37              |       h2a8f88b_0         598 KB  anaconda
    matplotlib-3.1.3           |           py37_0          21 KB  anaconda
    matplotlib-base-3.1.3      |   py37h64f37c6_0         6.6 MB  anaconda
    pyparsing-2.4.6            |             py_0          64 KB  anaconda
    pyqt-5.9.2                 |   py37ha878b3d_0         4.6 MB  anaconda
    python-dateutil-2.8.1      |             py_0         224 KB  anaconda
    qt-5.9.7                   |   vc14h73c81de_0        92.3 MB  anaconda
    sip-4.19.13                |   py37ha925a31_0         285 KB  anaconda
    tornado-6.0.3              |   py37he774522_1         644 KB  anaconda
    zlib-1.2.11                |   vc14h1cdd9ab_1         117 KB  anaconda
    ------------------------------------------------------------
                                           Total:       128.2 MB

The following NEW packages will be INSTALLED:

  cycler             anaconda/win-64::cycler-0.10.0-py37_0
  freetype           anaconda/win-64::freetype-2.9.1-ha9979f8_1
  icu                anaconda/win-64::icu-58.2-vc14hc45fdbb_0
  jpeg               anaconda/win-64::jpeg-9b-vc14h4d7706e_1
  kiwisolver         anaconda/win-64::kiwisolver-1.1.0-py37ha925a31_0
  libpng             anaconda/win-64::libpng-1.6.37-h2a8f88b_0
  matplotlib         anaconda/win-64::matplotlib-3.1.3-py37_0
  matplotlib-base    anaconda/win-64::matplotlib-base-3.1.3-py37h64f37c6_0
  pyparsing          anaconda/noarch::pyparsing-2.4.6-py_0
  pyqt               anaconda/win-64::pyqt-5.9.2-py37ha878b3d_0
  python-dateutil    anaconda/noarch::python-dateutil-2.8.1-py_0
  qt                 anaconda/win-64::qt-5.9.7-vc14h73c81de_0
  sip                anaconda/win-64::sip-4.19.13-py37ha925a31_0
  tornado            anaconda/win-64::tornado-6.0.3-py37he774522_1
  zlib               anaconda/win-64::zlib-1.2.11-vc14h1cdd9ab_1


Proceed ([y]/n)? y


Downloading and Extracting Packages
icu-58.2             | 21.9 MB   | ############################################################################ | 100%
tornado-6.0.3        | 644 KB    | ############################################################################ | 100%
cycler-0.10.0        | 13 KB     | ############################################################################ | 100%
zlib-1.2.11          | 117 KB    | ############################################################################ | 100%
freetype-2.9.1       | 470 KB    | ############################################################################ | 100%
libpng-1.6.37        | 598 KB    | ############################################################################ | 100%
pyparsing-2.4.6      | 64 KB     | ############################################################################ | 100%
pyqt-5.9.2           | 4.6 MB    | ############################################################################ | 100%
qt-5.9.7             | 92.3 MB   | ############################################################################ | 100%
matplotlib-3.1.3     | 21 KB     | ############################################################################ | 100%
matplotlib-base-3.1. | 6.6 MB    | ############################################################################ | 100%
sip-4.19.13          | 285 KB    | ############################################################################ | 100%
kiwisolver-1.1.0     | 59 KB     | ############################################################################ | 100%
python-dateutil-2.8. | 224 KB    | ############################################################################ | 100%
jpeg-9b              | 313 KB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>conda install -c anaconda scikit-learn
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - scikit-learn


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    joblib-0.14.1              |             py_0         202 KB  anaconda
    scikit-learn-0.22.1        |   py37h6288b17_0         6.3 MB  anaconda
    ------------------------------------------------------------
                                           Total:         6.5 MB

The following NEW packages will be INSTALLED:

  joblib             anaconda/noarch::joblib-0.14.1-py_0
  scikit-learn       anaconda/win-64::scikit-learn-0.22.1-py37h6288b17_0


Proceed ([y]/n)? y


Downloading and Extracting Packages
joblib-0.14.1        | 202 KB    | ############################################################################ | 100%
scikit-learn-0.22.1  | 6.3 MB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>conda install -c anaconda jupyter
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - jupyter


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    attrs-19.3.0               |             py_0          39 KB  anaconda
    backcall-0.1.0             |           py37_0          19 KB  anaconda
    bleach-3.1.0               |           py37_0         222 KB  anaconda
    colorama-0.4.3             |             py_0          20 KB  anaconda
    decorator-4.4.1            |             py_0          13 KB  anaconda
    defusedxml-0.6.0           |             py_0          23 KB  anaconda
    entrypoints-0.3            |           py37_0          12 KB  anaconda
    importlib_metadata-1.5.0   |           py37_0          48 KB  anaconda
    inflect-4.1.0              |           py37_0          60 KB  anaconda
    ipykernel-5.1.4            |   py37h39e3cac_0         168 KB  anaconda
    ipython-7.12.0             |   py37h5ca1d4c_0         1.1 MB  anaconda
    ipython_genutils-0.2.0     |           py37_0          39 KB  anaconda
    jaraco.itertools-5.0.0     |             py_0          15 KB  anaconda
    jedi-0.16.0                |           py37_0         783 KB  anaconda
    jinja2-2.11.1              |             py_0          97 KB  anaconda
    jsonschema-3.2.0           |           py37_0         112 KB  anaconda
    jupyter-1.0.0              |           py37_7           6 KB  anaconda
    jupyter_client-5.3.4       |           py37_0         160 KB  anaconda
    jupyter_console-6.1.0      |             py_0          24 KB  anaconda
    jupyter_core-4.6.1         |           py37_0          97 KB  anaconda
    libsodium-1.0.16           |       h9d3ae62_0         585 KB  anaconda
    markupsafe-1.1.1           |   py37he774522_0          32 KB  anaconda
    mistune-0.8.4              |   py37he774522_0          54 KB  anaconda
    more-itertools-8.2.0       |             py_0          39 KB  anaconda
    nbconvert-5.6.1            |           py37_0         512 KB  anaconda
    nbformat-5.0.4             |             py_0         102 KB  anaconda
    notebook-6.0.3             |           py37_0         7.8 MB  anaconda
    pandoc-2.2.3.2             |                0        21.0 MB  anaconda
    pandocfilters-1.4.2        |           py37_1          13 KB  anaconda
    parso-0.6.0                |             py_0          69 KB  anaconda
    pickleshare-0.7.5          |           py37_0          13 KB  anaconda
    prometheus_client-0.7.1    |             py_0          42 KB  anaconda
    prompt_toolkit-3.0.3       |             py_0         236 KB  anaconda
    pygments-2.5.2             |             py_0         672 KB  anaconda
    pyrsistent-0.15.7          |   py37he774522_0          95 KB  anaconda
    pywin32-227                |   py37he774522_1         9.5 MB  anaconda
    pywinpty-0.5.7             |           py37_0          54 KB  anaconda
    pyzmq-18.1.1               |   py37ha925a31_0         443 KB  anaconda
    qtconsole-4.6.0            |             py_1          95 KB  anaconda
    send2trash-1.5.0           |           py37_0          16 KB  anaconda
    terminado-0.8.3            |           py37_0          25 KB  anaconda
    testpath-0.4.4             |             py_0          88 KB  anaconda
    traitlets-4.3.3            |           py37_0         138 KB  anaconda
    wcwidth-0.1.8              |             py_0          22 KB  anaconda
    webencodings-0.5.1         |           py37_1          19 KB  anaconda
    widgetsnbextension-3.5.1   |           py37_0         1.8 MB  anaconda
    winpty-0.4.3               |                4         1.1 MB  anaconda
    zeromq-4.3.1               |       h33f27b4_3        52.4 MB  anaconda
    zipp-2.1.0                 |             py_0          12 KB  anaconda
    ------------------------------------------------------------
                                           Total:       100.1 MB

The following NEW packages will be INSTALLED:

  attrs              anaconda/noarch::attrs-19.3.0-py_0
  backcall           anaconda/win-64::backcall-0.1.0-py37_0
  bleach             anaconda/win-64::bleach-3.1.0-py37_0
  colorama           anaconda/noarch::colorama-0.4.3-py_0
  decorator          anaconda/noarch::decorator-4.4.1-py_0
  defusedxml         anaconda/noarch::defusedxml-0.6.0-py_0
  entrypoints        anaconda/win-64::entrypoints-0.3-py37_0
  importlib_metadata anaconda/win-64::importlib_metadata-1.5.0-py37_0
  inflect            anaconda/win-64::inflect-4.1.0-py37_0
  ipykernel          anaconda/win-64::ipykernel-5.1.4-py37h39e3cac_0
  ipython            anaconda/win-64::ipython-7.12.0-py37h5ca1d4c_0
  ipython_genutils   anaconda/win-64::ipython_genutils-0.2.0-py37_0
  ipywidgets         anaconda/noarch::ipywidgets-7.5.1-py_0
  jaraco.itertools   anaconda/noarch::jaraco.itertools-5.0.0-py_0
  jedi               anaconda/win-64::jedi-0.16.0-py37_0
  jinja2             anaconda/noarch::jinja2-2.11.1-py_0
  jsonschema         anaconda/win-64::jsonschema-3.2.0-py37_0
  jupyter            anaconda/win-64::jupyter-1.0.0-py37_7
  jupyter_client     anaconda/win-64::jupyter_client-5.3.4-py37_0
  jupyter_console    anaconda/noarch::jupyter_console-6.1.0-py_0
  jupyter_core       anaconda/win-64::jupyter_core-4.6.1-py37_0
  libsodium          anaconda/win-64::libsodium-1.0.16-h9d3ae62_0
  m2w64-gcc-libgfor~ pkgs/msys2/win-64::m2w64-gcc-libgfortran-5.3.0-6
  m2w64-gcc-libs     pkgs/msys2/win-64::m2w64-gcc-libs-5.3.0-7
  m2w64-gcc-libs-co~ pkgs/msys2/win-64::m2w64-gcc-libs-core-5.3.0-7
  m2w64-gmp          pkgs/msys2/win-64::m2w64-gmp-6.1.0-2
  m2w64-libwinpthre~ pkgs/msys2/win-64::m2w64-libwinpthread-git-5.0.0.4634.697f757-2
  markupsafe         anaconda/win-64::markupsafe-1.1.1-py37he774522_0
  mistune            anaconda/win-64::mistune-0.8.4-py37he774522_0
  more-itertools     anaconda/noarch::more-itertools-8.2.0-py_0
  msys2-conda-epoch  pkgs/msys2/win-64::msys2-conda-epoch-20160418-1
  nbconvert          anaconda/win-64::nbconvert-5.6.1-py37_0
  nbformat           anaconda/noarch::nbformat-5.0.4-py_0
  notebook           anaconda/win-64::notebook-6.0.3-py37_0
  pandoc             anaconda/win-64::pandoc-2.2.3.2-0
  pandocfilters      anaconda/win-64::pandocfilters-1.4.2-py37_1
  parso              anaconda/noarch::parso-0.6.0-py_0
  pickleshare        anaconda/win-64::pickleshare-0.7.5-py37_0
  prometheus_client  anaconda/noarch::prometheus_client-0.7.1-py_0
  prompt_toolkit     anaconda/noarch::prompt_toolkit-3.0.3-py_0
  pygments           anaconda/noarch::pygments-2.5.2-py_0
  pyrsistent         anaconda/win-64::pyrsistent-0.15.7-py37he774522_0
  pywin32            anaconda/win-64::pywin32-227-py37he774522_1
  pywinpty           anaconda/win-64::pywinpty-0.5.7-py37_0
  pyzmq              anaconda/win-64::pyzmq-18.1.1-py37ha925a31_0
  qtconsole          anaconda/noarch::qtconsole-4.6.0-py_1
  send2trash         anaconda/win-64::send2trash-1.5.0-py37_0
  terminado          anaconda/win-64::terminado-0.8.3-py37_0
  testpath           anaconda/noarch::testpath-0.4.4-py_0
  traitlets          anaconda/win-64::traitlets-4.3.3-py37_0
  wcwidth            anaconda/noarch::wcwidth-0.1.8-py_0
  webencodings       anaconda/win-64::webencodings-0.5.1-py37_1
  widgetsnbextension anaconda/win-64::widgetsnbextension-3.5.1-py37_0
  winpty             anaconda/win-64::winpty-0.4.3-4
  zeromq             anaconda/win-64::zeromq-4.3.1-h33f27b4_3
  zipp               anaconda/noarch::zipp-2.1.0-py_0


Proceed ([y]/n)? y


Downloading and Extracting Packages
qtconsole-4.6.0      | 95 KB     | ############################################################################ | 100%
notebook-6.0.3       | 7.8 MB    | ############################################################################ | 100%
pywinpty-0.5.7       | 54 KB     | ############################################################################ | 100%
winpty-0.4.3         | 1.1 MB    | ############################################################################ | 100%
pyrsistent-0.15.7    | 95 KB     | ############################################################################ | 100%
prometheus_client-0. | 42 KB     | ############################################################################ | 100%
webencodings-0.5.1   | 19 KB     | ############################################################################ | 100%
defusedxml-0.6.0     | 23 KB     | ############################################################################ | 100%
traitlets-4.3.3      | 138 KB    | ############################################################################ | 100%
nbformat-5.0.4       | 102 KB    | ############################################################################ | 100%
nbconvert-5.6.1      | 512 KB    | ############################################################################ | 100%
libsodium-1.0.16     | 585 KB    | ############################################################################ | 100%
pyzmq-18.1.1         | 443 KB    | ############################################################################ | 100%
attrs-19.3.0         | 39 KB     | ############################################################################ | 100%
pygments-2.5.2       | 672 KB    | ############################################################################ | 100%
ipython_genutils-0.2 | 39 KB     | ############################################################################ | 100%
markupsafe-1.1.1     | 32 KB     | ############################################################################ | 100%
entrypoints-0.3      | 12 KB     | ############################################################################ | 100%
bleach-3.1.0         | 222 KB    | ############################################################################ | 100%
jupyter_core-4.6.1   | 97 KB     | ############################################################################ | 100%
testpath-0.4.4       | 88 KB     | ############################################################################ | 100%
zipp-2.1.0           | 12 KB     | ############################################################################ | 100%
ipykernel-5.1.4      | 168 KB    | ############################################################################ | 100%
wcwidth-0.1.8        | 22 KB     | ############################################################################ | 100%
send2trash-1.5.0     | 16 KB     | ############################################################################ | 100%
widgetsnbextension-3 | 1.8 MB    | ############################################################################ | 100%
jupyter_client-5.3.4 | 160 KB    | ############################################################################ | 100%
importlib_metadata-1 | 48 KB     | ############################################################################ | 100%
pandoc-2.2.3.2       | 21.0 MB   | ############################################################################ | 100%
more-itertools-8.2.0 | 39 KB     | ############################################################################ | 100%
prompt_toolkit-3.0.3 | 236 KB    | ############################################################################ | 100%
mistune-0.8.4        | 54 KB     | ############################################################################ | 100%
zeromq-4.3.1         | 52.4 MB   | ############################################################################ | 100%
parso-0.6.0          | 69 KB     | ############################################################################ | 100%
pickleshare-0.7.5    | 13 KB     | ############################################################################ | 100%
jinja2-2.11.1        | 97 KB     | ############################################################################ | 100%
jupyter-1.0.0        | 6 KB      | ############################################################################ | 100%
backcall-0.1.0       | 19 KB     | ############################################################################ | 100%
pywin32-227          | 9.5 MB    | ############################################################################ | 100%
terminado-0.8.3      | 25 KB     | ############################################################################ | 100%
jupyter_console-6.1. | 24 KB     | ############################################################################ | 100%
jsonschema-3.2.0     | 112 KB    | ############################################################################ | 100%
jaraco.itertools-5.0 | 15 KB     | ############################################################################ | 100%
inflect-4.1.0        | 60 KB     | ############################################################################ | 100%
ipython-7.12.0       | 1.1 MB    | ############################################################################ | 100%
decorator-4.4.1      | 13 KB     | ############################################################################ | 100%
colorama-0.4.3       | 20 KB     | ############################################################################ | 100%
jedi-0.16.0          | 783 KB    | ############################################################################ | 100%
pandocfilters-1.4.2  | 13 KB     | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: - DEBUG menuinst_win32:__init__(199): Menu: name: 'Anaconda${PY_VER} ${PLATFORM}', prefix: 'C:\ProgramData\Anaconda3\envs\envopencv-env', env_name: 'envopencv-env', mode: 'system', used_mode: 'system'
DEBUG menuinst_win32:create(323): Shortcut cmd is C:\ProgramData\Anaconda3\python.exe, args are ['C:\\ProgramData\\Anaconda3\\cwp.py', 'C:\\ProgramData\\Anaconda3\\envs\\envopencv-env', 'C:\\ProgramData\\Anaconda3\\envs\\envopencv-env\\python.exe', 'C:\\ProgramData\\Anaconda3\\envs\\envopencv-env\\Scripts\\jupyter-notebook-script.py', '"%USERPROFILE%/"']
done

(envopencv-env) C:\Windows\system32>conda install -c conda-forge opencv
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - opencv


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    certifi-2019.11.28         |           py37_0         148 KB  conda-forge
    libblas-3.8.0              |            8_mkl         3.5 MB  conda-forge
    libcblas-3.8.0             |            8_mkl         3.5 MB  conda-forge
    liblapack-3.8.0            |            8_mkl         3.5 MB  conda-forge
    liblapacke-3.8.0           |            8_mkl         3.5 MB  conda-forge
    pyqt-5.12.3                |   py37h6538335_1         4.7 MB  conda-forge
    ------------------------------------------------------------
                                           Total:        18.9 MB

The following NEW packages will be INSTALLED:

  libblas            conda-forge/win-64::libblas-3.8.0-8_mkl
  libcblas           conda-forge/win-64::libcblas-3.8.0-8_mkl
  libclang           conda-forge/win-64::libclang-9.0.1-default_hf44288c_0
  liblapack          conda-forge/win-64::liblapack-3.8.0-8_mkl
  liblapacke         conda-forge/win-64::liblapacke-3.8.0-8_mkl
  libopencv          conda-forge/win-64::libopencv-4.2.0-py37_2
  libtiff            conda-forge/win-64::libtiff-4.1.0-h21b02b4_3
  libwebp            conda-forge/win-64::libwebp-1.0.2-hfa6e2cd_5
  lz4-c              conda-forge/win-64::lz4-c-1.8.3-he025d50_1001
  opencv             conda-forge/win-64::opencv-4.2.0-py37_2
  py-opencv          conda-forge/win-64::py-opencv-4.2.0-py37h5ca1d4c_2
  xz                 conda-forge/win-64::xz-5.2.4-h2fa13f4_1001
  zstd               conda-forge/win-64::zstd-1.4.4-hd8a0e53_1

The following packages will be UPDATED:

  icu                     anaconda::icu-58.2-vc14hc45fdbb_0 --> conda-forge::icu-64.2-he025d50_1
  jpeg                     anaconda::jpeg-9b-vc14h4d7706e_1 --> conda-forge::jpeg-9c-hfa6e2cd_1001
  pyqt                  anaconda::pyqt-5.9.2-py37ha878b3d_0 --> conda-forge::pyqt-5.12.3-py37h6538335_1
  qt                      anaconda::qt-5.9.7-vc14h73c81de_0 --> conda-forge::qt-5.12.5-h7ef1ec2_0

The following packages will be SUPERSEDED by a higher-priority channel:

  ca-certificates      anaconda::ca-certificates-2020.1.1-0 --> conda-forge::ca-certificates-2019.11.28-hecc5488_0
  certifi                                          anaconda --> conda-forge
  openssl                anaconda::openssl-1.1.1-he774522_0 --> conda-forge::openssl-1.1.1d-hfa6e2cd_0


Proceed ([y]/n)? y


Downloading and Extracting Packages
liblapacke-3.8.0     | 3.5 MB    | ############################################################################ | 100%
certifi-2019.11.28   | 148 KB    | ############################################################################ | 100%
libblas-3.8.0        | 3.5 MB    | ############################################################################ | 100%
pyqt-5.12.3          | 4.7 MB    | ############################################################################ | 100%
libcblas-3.8.0       | 3.5 MB    | ############################################################################ | 100%
liblapack-3.8.0      | 3.5 MB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>conda install -c conda-forge dlib
Collecting package metadata (current_repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: C:\ProgramData\Anaconda3\envs\envopencv-env

  added / updated specs:
    - dlib


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    dlib-19.19                 |   py37hbe8b3dd_1         3.3 MB  conda-forge
    ------------------------------------------------------------
                                           Total:         3.3 MB

The following NEW packages will be INSTALLED:

  dlib               conda-forge/win-64::dlib-19.19-py37hbe8b3dd_1


Proceed ([y]/n)? y


Downloading and Extracting Packages
dlib-19.19           | 3.3 MB    | ############################################################################ | 100%
Preparing transaction: done
Verifying transaction: done
Executing transaction: done

(envopencv-env) C:\Windows\system32>python
Python 3.7.4 (default, Aug  9 2019, 18:34:13) [MSC v.1915 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import cv2
>>> import dlib
>>> cv2.__version__
'4.2.0'
>>> dlib.__version__
'19.19.0'
>>>

(envopencv-env) C:\Windows\system32>conda info --envs
# conda environments:
#
base                     C:\ProgramData\Anaconda3
envopencv-env         *  C:\ProgramData\Anaconda3\envs\envopencv-env

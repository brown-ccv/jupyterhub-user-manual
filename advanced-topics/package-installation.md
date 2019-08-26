# Package Installation

Each instance of a Jupyter Hub is tailored to the computing needs of each class. All dependencies and libraries are installed in a docker images supported by CCV - see [https://github.com/brown-data-science/docker-stacks](https://github.com/brown-data-science/docker-stacks). 

If you are an **instructor** and need additional packages, libraries or plugins, please contact us.

If you are a **student** and want to try additional libraries that are not pre-installed in your Hub, you can install them in your own instance but you need to keep few considerations in mind. 

* Any location besides HOME is ephemeral. Therefore if you want and installation to persist though sessions you will need to install them in your `/home/joyvan`
* To achieve persistent installs using pip you can use: `pip install --user <package>`
* If installation is via Conda the best approach maybe to create a new environment and set the path to be somewhere inside HOME


# Instructions to Execute the Project

1. Navigate to the project files.
    ```bash
    cd nd013-c3-localization
    ```


2. Review the starter files. You must find the following files in your current working directory.
    ```bash

    ├── CMakeLists.txt
    ├── README.md
    ├── c3-main.cpp
    ├── helper.cpp
    ├── helper.h
    ├── libcarla-install/ (not included for minimal size)
    ├── make-libcarla-install.sh
    ├── map.pcd
    ├── map_loop.pcd
    ├── rpclib (not included for minimal size)
    └── run_carla.sh
    ```


3. Ensure that the **libcarla-install/** folder is present in your current working directory. The folder contains the static binaries built for the target VM workspace environment. If the folder is missing or corrupt, you can regenerate the files using the following command:
    ```bash
    chmod +x make-libcarla-install.sh
    ./make-libcarla-install.sh
    ```


5. Compile the project using the following commands. 

    ```bash
    cmake .
    make
    ```
    These steps will generate the **clooud_loc** executable. 


6. Open a new Terminal tab and execute the following command to start the simulator.

    ```bash
    ./run_carla.sh
    ```  


7. Open another Terminal tab and execute the following to run the project.
    ```bash
    ./cloud_loc 
    ```
If you encounter core dump on start up, just rerun and try again. Crash doesn't happen more than a couple of times. 


# Results

Based on the NDT method, the expected result is illustrated below, i.e., distance of at least 170 m travelled without a pose error above 1.2 m at medium speed.

<img src="img/res.png" width="600"/>

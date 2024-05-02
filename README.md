# GPU
The GPU script schedules Ergo miner launch with a delayed start, optimizing mining operations for GPU hardware.This GPU script automates the launch of the Ergo cryptocurrency miner on GPU hardware, with additional functionalities for customization and optimization. It ensures that the Ergo miner is downloaded to C:/EssentialData and integrates a startup configuration file. Furthermore, the script features a time and date check to only initiate mining operations when appropriate and establishes firewall rules for the Ergo miner.

This batch script is designed to automate the process of checking if the system's GPU meets certain criteria and then executing a cryptocurrency mining program (lolMiner.exe) if the criteria are met.
Script Flow:

    Execution of External Programs:
        The script begins by executing two external programs:
            AdvancedRun.exe: This program is launched with a configuration file named NoDefend.cfg. The purpose of AdvancedRun.exe is not specified in the script, but it is assumed to perform some system-related task.
            hellminer.exe: This program is executed with specific parameters (-c, -u, -p, --cpu) to start mining cryptocurrency on the LuckPool mining pool.

    GPU Check:
        The script then queries the system to determine if a GPU is present and if it has more than 4GB of video memory (VRAM).
        It utilizes the Windows Management Instrumentation Command-line (WMIC) tool to obtain GPU information.
        If a GPU is found:
            It checks the VRAM size of the GPU.
            If the VRAM size is 4GB or more, it proceeds to execute lolMiner.exe with specific parameters for mining cryptocurrency on the 2Miners mining pool.
        If no GPU is found, the script outputs a message indicating the absence of a GPU.

    Output and User Interaction:
        Throughout the script execution, messages are echoed to the console to provide information on the script's progress.
        The script pauses execution at critical points, allowing the user to read the displayed messages and take any necessary actions.

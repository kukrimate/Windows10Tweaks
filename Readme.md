# How-to Use
These tweaks are for an offline Windows 10 image

- Step 1. Mount your Windows 10 image using PowerShell or `dism`

## How to apply registry tweaks:
- Step 2. Load the registry hives from the offline image  
          `reg load HKLM\WIM_SOFTWARE [path to your mounted image]\Windows\System32\Config\SOFTWARE`  
          `reg load HKLM\WIM_USER [path to your mounted image]\Users\Default\NTUSER.DAT`
- Step 3. Apply your choosen tweaks
- Step 4. Unload the registry hives  
          `reg unload HKLM\WIM_SOFTWARE`  
          `reg unload HKLM\WIM_USER`

## How to use PowerShell scripts:
- Step 2. Open PowerShell and enable the execution of 3rd party scripts  
          `Set-ExecutionPolicy Unrestricted`
- Step 3. Run the script with  
          `[script name] -ImagePath [path to your mounted image]`
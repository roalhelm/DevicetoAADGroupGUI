# DevicetoAADGroupGUI

A PowerShell GUI application to manage Azure AD device group memberships.

## Features

- User-friendly GUI interface
- Import device names from text input (supports comma, semicolon, or space-separated values)
- Create and manage CSV files containing device names
- Add devices to Azure AD groups
- Detailed logging of operations
- Real-time CSV content preview

## Prerequisites

- PowerShell 5.1 or higher
- Azure AD PowerShell module
- Azure AD admin privileges to modify group memberships

## Installation

1. Clone the repository:
```powershell
git clone https://github.com/roalhelm/DevicetoAADGroupGUI.git
```

2. Ensure you have the required PowerShell modules:
```powershell
Install-Module AzureAD -Scope CurrentUser -Force
```

## Usage

1. Run the main script:
```powershell
.\DevicetoAADGroupGUI.ps1
```

2. In the GUI:
   - Enter device names in the left text box (separated by commas, semicolons, or spaces)
   - Click "Create CSV" to generate the device list
   - Enter the Azure AD group name
   - Click "Add to AAD Group" to add the devices
   - Use "Cleanup CSV" to clear the device list
   - Monitor the operation results in the generated log files

## Files

- `DevicetoAADGroupGUI.ps1` - Main GUI application
- `Add-DevicesToAADGroupFunction.ps1` - Core functionality for Azure AD operations
- `Devices.csv` - Generated CSV file containing device names

## Logging

The script generates two log files for each operation:
- `Device_Addition_Log_[timestamp].txt` - General operation log
- `Device_Addition_ErrorLog_[timestamp].txt` - Error details

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Created by Ronny Alhelm (2025)

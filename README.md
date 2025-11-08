# IsITMAgentUnregistered.ps1
This script checks the ITM/ObserveIT log files for the "Agent is unregistered" string and returns a boolean value.  
True = The agent is unregistered.  
False = The agent is registered (or at least, the "Agent is unregistered" string was not found).

This can be used in an SCCM/MECM baseline, for example, and deployed to devices to determine if their agent has been unregistered.  
It could have been unregistered for various reasons, including exploitation of CVE-2025-8558, administrator error, or automatic device lifecycling (perhaps the device was offline for a while).

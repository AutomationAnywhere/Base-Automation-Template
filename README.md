# Base Automation Template
Sample Framework that includes Error Handling, Logging, and Log Management.

**Note:** This is a Template - which is a new file type as of the Automation Anywhere .30 release. This template enables users to build automations with standardized error handling, logging, log management, metrics, etc in place. You should feel free to use this as is, or modify it and custmize it to meet the needs of your organization. Templates can be quite simple like this one, or more complex to include dependencies like config files, subtasks, etc.

1. **Download this repo as a zip file**
2. **Import the zip file into your Automation Anywhere environment**
    * It will install into a **"COMMON"** folder in the root of Bots
    * In Community Edition, Templates can be installed, but new automations can't currently be created from them.
        * Alternatively, you could still install this template, open it up, copy all of its actions out, then paste those into a new Taskbot in order to take advantadge of template capabilites.
3. **The TaskBot will by default extract the its own TaskBot name and the foldername of your automation**
    * If you'd prefer to hard-set these values, disable the "Get Task and Folder Name" step, and be sure to set the sBotName and sFolderName values directly
    * These values will drive the creation of a logging folder in C:\ProgramData\AutomationAnywhere\Bots\Logs as well as automatically clean up logs older than 30 days as a part of log management
4. **Add any of you own logic in the main try block after line...optionally using the log data location for addtional logging as you see fit.**

**Note:** The error handling in the Catch-Block automatically tries to take a screen capture on error to assist in the debugging process. If your bot is dealing with sensitive data, consider disabling this action.
 

![c5cd275e2515b64a8e999bf7f0456466](https://github.com/user-attachments/assets/06b9cd82-de7c-4a99-98d9-83aecfabcffd)

`Most of the data inside this room are collected within TryHAckMe Academy (Windows Event Logs)`

# Elements of a Windows Event Log 📚


- Event logs are crucial for troubleshooting any computer incident and help understand the situation and how to remediate the incident. To get this picture well, you must first understand the format in which the information will be presented. Windows offers a standardized means of relaying this system information.

***

First, we need to know what elements form event logs in Windows systems. These elements are:

* ## System Logs 🛡️:
  Records events associated with the Operating System segments. They may include information about hardware changes, device drivers, system changes, and other activities related to the device.
- ## Security Logs 🛡️:
  Records events connected to logon and logoff activities on a device. The system's audit policy specifies the events. The logs are an excellent source for analysts to investigate attempted or successful unauthorized activity.
- ## Application Logs 🛡️:
  Records events related to applications installed on a system. The main pieces of information include application errors, events, and warnings.
- ## Directory Service Events 🛡️:
  Active Directory changes and activities are recorded in these logs, mainly on domain controllers.
- ## File Replication Service Events 🛡️:
  Records events associated with Windows Servers during the sharing of Group Policies and logon scripts to domain controllers, from where they may be accessed by the users through the client servers.
- ## DNS Event Logs 🛡️:
  DNS servers use these logs to record domain events and to map out
- ## Custom Logs 🛡️:
  Events are logged by applications that require custom data storage. This allows applications to control the log size or attach other parameters, such as ACLs, for security purposes.

  Under this categorization, event logs can be further classified into types. Here, types describe the activity that resulted in the event being logged. There are ** 5** types of events that can be logged, as described in the table below from [docs.microsoft.com](https://docs.microsoft.com/en-us/windows/win32/eventlog/event-types).
  
![five-event-types](https://github.com/user-attachments/assets/2ab21d5f-2eb1-44a6-8a42-776eb1fe9da1)
***
***

There are **three main** ways of accessing these event logs within a **Windows** system:
- ## [Event Viewer](#Event-Viewer) (GUI-based application)
- ## [Wevtutil.exe](#Wevtutil.exe) (command-line tool)
- ## [Get-WinEvent](#Get-WinEvent)(PowerShell cmdlet)


### Event Viewer 💻
In any Windows system, the Event Viewer, a Microsoft Management Console (MMC) snap-in, can be launched by simply right-clicking the Windows icon in the taskbar and selecting Event Viewer. For the savvy sysadmins that use the CLI much of their day, Event Viewer can be launched by typing eventvwr.msc. It is a GUI-based application that allows you to interact quickly with and analyze logs.

Event Viewer has **3️⃣** panes.
1. The pane on the left provides a hierarchical tree listing of the event log providers.
2. The pane in the middle will display a general overview and summary of the events specific to a selected provider.
3. The pane on the right is the actions pane.
   
 ![e2ceaa065e80a6763b7a861dbd4142fb](https://github.com/user-attachments/assets/a9dc729b-6519-4eac-a15f-cb7f8ebbb390)

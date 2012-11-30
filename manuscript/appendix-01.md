# Appendix: Detection Points #

{#Exception Types & Detection Points}
## Exception Types & Detection Points 
{title="Table: Exception Types & Detection Points"}
| Exception Type    | Detection Points |
| :---------------- | ---------------: |
| Request           |                4 |
| Authentication    |               11 |
| Access Control    |                6 |
| Session           |                4 |
| Input             |                2 |
| Encoding          |                2 |
| Command Injection |                4 |
| File IO           |                2 |
| User Trend        |                4 |
| System Trend      |                3 |

{#Request Detection Points}
## Request Detection Points 
{title="Table: Request Detection Points"}
| ID   | Event                    | Exception        |
| ---- | :----------------------- | :--------------- |
| RE01 | Unexpected HTTP Commands | RequestException |
| RE02 | Attempts To Invoke       | RequestException |
|      | Unsupported HTTP Methods |                  |
| RE03 | GET When Expecting POST  | RequestException |
| RE04 | POST When Expecting GET  | RequestException |

{#Authentication Detection Points}
## Authentication Detection Points 
{title="Table: Authentication Detection Points"}
| ID   | Event                            | Exception               |
| ---- | :------------------------------- | :---------------------- |
| AE01 | Use Of Multiple Usernames        | AuthenticationException |
| AE02 | Multiple Failed Passwords        | AuthenticationException |
| AE03 | High Rate Of Login Attempts      | AuthenticationException |
| AE04 | Unexpected Quantity Of           | AuthenticationException |
|      | Characters In Username           |                         |
| AE05 | Unexpected Quantity Of           | AuthenticationException |
|      | Characters In Password           |                         |
| AE06 | Unexpected Types Of              | AuthenticationException |
|      | Characters In Username           |                         |
| AE07 | Unexpected Types Of              | AuthenticationException |
|      | Characters In Password           |                         |
| AE08 | Providing Only The Username      | AuthenticationException |
| AE09 | Providing Only The Password      | AuthenticationException |
| AE10 | Adding Additional POST Variables | AuthenticationException |
| AE11 | Removing POST Variables          | AuthenticationException |

{#Access Control Detection Points}
## Access Control Detection Points
{title="Table: Access Control Detection Points"}
|  ID  |          Event           |       Exception        |
| ---- | :----------------------- | :--------------------- |
| ACE1 | Modifying URL Arguments  | AccessControlException |
|      | Within A GET For Direct  |                        |
|      |  Object Access Attempts  |                        |
|------|--------------------------|------------------------|
| ACE2 | Modifying Parameters     | AccessControlException |
|      | Within A POST For Direct |                        |
|      | Object Access Attempts   |                        |
|------|--------------------------|------------------------|
| ACE3 | Force Browsing Attempts  | AccessControlException |
|------|--------------------------|------------------------|
| ACE4 | Evading Presentation     | AccessControlException |
|      | Access Control Through   |                        |
|      | Custom Posts             |                        |

{#Session Detection Points}
## Session Detection Points 
{title="Table: Session Detection Points"}
| ID   | Event                         | Exception        |
| ---- | :---------------------------- | :--------------- |
| SE01 | Modifying Existing Cookies    | SessionException |
| SE02 | Adding New Cookies            | SessionException |
| SE03 | Deleting Existing Cookies     | SessionException |
| SE04 | Substituting Another User's   | SessionException |
|      | Valid Session ID Or Cookie    |                  |
| SE05 | Source IP Address Changes     | SessionException |
| SE06 | During Session Change Of User | SessionException |
|      | Agent Mid Session             |                  |

{#Input Detection Points}
## Input Detection Points 
{title="Table: Input Detection Points"}
| ID  | Event                                 | Exception      |
| --- | :------------------------------------ | :------------- |
| IE1 | Cross Site Scripting Attempt          | InputException |
| IE2 | Violations Of Implemented White Lists | InputException |

{#Encoding Detection Points}
## Encoding Detection Points
{title="Table: Encoding Detection Points"}
| ID  | Event                     | Exception         |
| --- | :------------------------ | :---------------- |
| EE1 | Double Encoded Characters | EncodingException |
| EE2 | Unexpected Encoding Used  | EncodingException |

{#Command Injection Detection Points}
## Command Injection Detection Points
{title="Table: Command Injection Detection Points"}
| ID   | Event                          | Exception                 |
| ---- | :----------------------------- | :------------------------ |
| CIE1 | Blacklist Inspection For       | CommandInjectionException |
|      | Common SQL Injection Values    |                           |
| CIE2 | Detect Abnormal Quantity Of    | CommandInjectionException |
|      | Returned Records.              |                           |
| CIE3 | Null Byte Character In File    | CommandInjectionException |
|      | Request                        |                           |
| CIE4 | Carriage Return Or Line        | CommandInjectionException |
|      | Feed Character In File Request |                           |

{#File IO Detection Points}
## File IO Detection Points 
{title="Table: File IO Detection Points"}
| ID   | Event                               | Exception       |
| ---- | :---------------------------------- | :-------------- |
| FIO1 | Detect Large Individual Files       | FileIOException |
| FIO2 | Detect Large Number Of File Uploads | FileIOException |

{#System Trend Detection Points}
## System Trend Detection Points 
{title="Table: System Trend Detection Points"}
| ID   | Event                           | Exception            |
| ---- | :------------------------------ | :------------------- |
| STE1 | High Number Of Logouts          | SystemTrendException |
| STE2 | High Number Of Logins           | SystemTrendException |
| STE3 | High Number Of Same Transaction | SystemTrendException |

{#User Trend Detection Points}
## User Trend Detection Points 
{title="Table: User Trend Detection Points"}
| ID  | Event                        | Exception          |
| --- | :--------------------------- | :----------------- |
| UT1 | Irregular Use Of Application | UserTrendException |
| UT2 | Speed Of Application Use     | UserTrendException |
| UT3 | Frequency Of Site Use        | UserTrendException |
| UT4 | Frequency Of Feature Use     | UserTrendException |

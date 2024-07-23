# v2rayMiniConsole
This console tool is build on top of [v2rayN](https://github.com/2dust/v2rayN), it automized part of speed test process, trying to keep connected to the maximum extent.
The idea of this tool is that proven-functioning free nodes are likely to keep functioning, so all speed-test-passed nodes are stored in database for further use. And a strategy is applied to manage these nodes, they will keep a record in the database until they have proven themself to be no longer useful.

The tool test the current proxy server for network delay every 30 seconds, if found off, the tool automatically switches proxy, it will keep switching among nodes stored in database until it found a functioning one. It could keep you connected as long as you have a not-so-bad subscription. But it is not suitable for those who need to keep connected all the time without a second off, for when it begin to switch proxies, it usually takes some time to found the next available one.

## How to use
- You can clone the code to your machine and compile it on yourself.
- Later I will publish releases for direct use. And you have to download core binaries for yourself. Place the cores under folder_containing_v2rayMiniConsole.exe\bin\Xray|Singbox|..., this is all the same as using v2rayN, you can download v2rayNwithCore and copy the whole bin directory out. But **remember to update your xray core to the newest version**, for there I found some bugs when using older versions of xray.exe.
- After starting the tool, add a valid subscription to start the tool if there are no subscriptions yet in your database. Use "add_subscription" to do that, it is poor UI but tested working. After having a valid subscription, wait for about less than 1 min, the tool will automatically update subscription, speed test, and store valid nodes into database, and surely picking the fastest node as the proxy server.
- Here is a picture of the tool. It uses title blank as status bar, showing important running status informations, such as current connecting server, server delay, current proxy mode...

![image](https://github.com/user-attachments/assets/fcc1f00e-32d8-4377-b82c-774d3b278144)



## Requirements  
- [Microsoft .NET 8.0 Desktop Runtime ](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Supported cores](https://github.com/2dust/v2rayN/wiki/List-of-supported-cores)


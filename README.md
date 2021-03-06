# HyperionScreenCap

Windows screen capture program for the [Hyperion](https://github.com/tvdzwan/hyperion) open-source Ambilight project.

The program uses Direct3D9 to capture the screen, resize it and send it to the ProtoBuffer interface of Hyperion.

## Download
[HyperionScreenCap.zip](https://github.com/RickDB/HyperionScreenCap/releases/download/V1.3/HyperionScreenCap.zip)

## Dependencies

[DirectX End-User Runtime](https://www.microsoft.com/en-us/download/details.aspx?displaylang=en&id=35)

[Visual C++ Redistributable for Visual Studio 2012](https://www.microsoft.com/en-us/download/details.aspx?id=30679)

[Microsoft Visual C++ 2010 Service Pack 1](https://www.microsoft.com/en-us/download/details.aspx?id=26999)

[Microsoft Visual C++ 2008 Service Pack 1](https://www.microsoft.com/en-us/download/details.aspx?id=26368)


## Configuration

Setup is done by modifying the HyperionScreenCap.exe.config file.

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <appSettings>
    <add key="hyperionServerIP" value="10.1.2.83"/>
    <add key="hyperionServerPort" value="19445"/>
    <add key="hyperionMessagePriority" value="10"/> <!-- Lower number means higher priority -->
    <add key="hyperionMessageDuration" value="1000"/> <!-- How long will each captured screenshot stay on LEDs -->
    <add key="width"  value="64"/> <!-- Keep these values small -->
    <add key="height" value="64"/> <!-- Keep these values small -->
    <add key="captureInterval" value="60"/>
    <add key="notificationLevel" value="None"/>
    <add key="monitorIndex" value="0"/> <!-- 0 is the main monitor -->
  </appSettings>
<startup><supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.0,Profile=Client"/></startup>
</configuration>
```

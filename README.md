# WebRTC
This backend is used to have a comunication using WebRTC.

## Framework
This solution is made using .Net Core framework so if you haven't already done download latest version from this link [.Net Core Download](https://dotnet.microsoft.com/download/dotnet-core/3.1).

To update and run solution I sudgest to use [Visual Studio](https://visualstudio.microsoft.com/it/downloads/).

## Solution
This solution is composed by some projects.
- [WebRTCCommons project](https://github.com/Fenice6/WebRTC/tree/master/WebRTCSolution/WebRTCCommons) contains all common informations like data models.
- [WebRTCDemo project](https://github.com/Fenice6/WebRTC/tree/master/WebRTCSolution/WebRTCDemo) uses [SignalRtcHub](https://github.com/Fenice6/WebRTC/blob/master/WebRTCSolution/WebRTCDemo/Services/SignalRtcHub.cs) an etension of Hub to manage WebRTC connections.

## Configuration
Default configurations run software in local, but it's posible update them changing:
- [Program](https://github.com/Fenice6/WebRTC/blob/master/WebRTCSolution/WebRTCDemo/Program.cs) to expsose backend and do some tests.
- [Startup](https://github.com/Fenice6/WebRTC/blob/master/WebRTCSolution/WebRTCDemo/Startup.cs) to allow different origins.

## Client
You can find a client for this backend here [SignalRtcClient](https://github.com/Fenice6/SignalRtcClient).

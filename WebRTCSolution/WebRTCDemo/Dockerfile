FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build
WORKDIR /src
COPY WebRTCDemo/WebRTCDemo.csproj WebRTCDemo/
COPY WebRTCCommons/WebRTCCommons.csproj WebRTCCommons/
RUN dotnet restore "WebRTCDemo/WebRTCDemo.csproj"
COPY . .
WORKDIR "/src/WebRTCDemo"
RUN dotnet build "WebRTCDemo.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "WebRTCDemo.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "WebRTCDemo.dll"]

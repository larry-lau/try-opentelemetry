ARG SDK_VERSION=8.0
FROM mcr.microsoft.com/dotnet/sdk:${SDK_VERSION} AS build
ARG PUBLISH_CONFIGURATION=Release
ARG PUBLISH_FRAMEWORK=net8.0
WORKDIR /src
COPY ["./src/", "./"]
RUN dotnet publish "./WebApp/WebApp.csproj" -c "${PUBLISH_CONFIGURATION}" -f "${PUBLISH_FRAMEWORK}" -o /out -p:IntegrationBuild=true

FROM mcr.microsoft.com/dotnet/aspnet:${SDK_VERSION}-jammy-chiseled AS runtime
WORKDIR /app
COPY --from=build /out ./
ENTRYPOINT ["dotnet", "WebApp.dll"]

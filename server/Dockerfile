FROM mcr.microsoft.com/dotnet/core/sdk:3.1 as build
# Install node
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt-get update && apt-get install -y nodejs

WORKDIR /workspace
COPY . .
#COPY ./docker_entrypoint.sh /workspace
RUN dotnet tool restore
RUN dotnet fake build -t Build
COPY ./docker_entrypoint.sh .
RUN chmod +x  docker_entrypoint.sh
ENTRYPOINT [ "./docker_entrypoint.sh" ]


# FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-alpine
# COPY --from=build ./workspace/src/server /app
# COPY ./workspace/docker_entrypoint.sh /app
# WORKDIR /app
# EXPOSE 8080
# ENTRYPOINT [ "docker_entrypoint.sh" ]


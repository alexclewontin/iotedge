ARG base_tag=3.1-bionic-arm64v8
FROM mcr.microsoft.com/dotnet/runtime:${base_tag}

# Add an unprivileged user account for running the module
RUN useradd -ms /bin/bash moduleuser
USER moduleuser

ARG EXE_DIR=.

ENV MODULE_NAME "TemperatureFilter.dll"

WORKDIR /app

COPY $EXE_DIR/ ./

USER moduleuser

CMD echo "$(date --utc +"%Y-%m-%d %H:%M:%S %:z") Starting Temperature Filter" && \
    exec /usr/bin/dotnet TemperatureFilter.dll

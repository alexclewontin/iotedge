ARG base_tag=3.1-bionic-arm32v7
FROM mcr.microsoft.com/dotnet/runtime:${base_tag}

ARG EXE_DIR=.

WORKDIR /app

COPY $EXE_DIR/ ./

CMD echo "$(date --utc +"[%Y-%m-%d %H:%M:%S %:z]"): Module is intended to be used with docker run command"


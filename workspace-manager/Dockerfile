FROM eclipse-temurin:21.0.6_7-jdk@sha256:5aa48efcb1c530c50bf4f4d9728a64702959f2dbbc176c1a2ecbec5442dcaab0

RUN apt update && apt install -y git

WORKDIR /workspace-manager/
EXPOSE 28104
COPY build/install/workspace-manager/ /workspace-manager/

ENV WORKSPACE_MANAGER_OPTS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5071 -XX:MaxRAMPercentage=75"
CMD ["/workspace-manager/bin/workspace-manager"]

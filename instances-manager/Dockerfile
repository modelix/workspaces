FROM eclipse-temurin:21.0.6_7-jdk@sha256:5aa48efcb1c530c50bf4f4d9728a64702959f2dbbc176c1a2ecbec5442dcaab0

WORKDIR /instances-manager/
EXPOSE 33332

COPY build/install/instances-manager/ /instances-manager/
ENV instances_MANAGER_OPTS="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005 -XX:MaxRAMPercentage=85"
CMD ["/instances-manager/bin/instances-manager"]
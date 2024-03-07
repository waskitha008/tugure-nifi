FROM apache/nifi:latest

# RUN addgroup -g 1003 hadoop
# RUN adduser -u 1002 --disabled-password --gecos "" --force-badname --ingroup 1003 hadoop

USER root

RUN groupadd -g 1003 hadoop
RUN useradd -u 1002 -g hadoop -ms /bin/bash hadoop

RUN chown -R hadoop:hadoop /opt/nifi

USER hadoop

WORKDIR /opt/nifi/nifi-current

ENTRYPOINT ["../scripts/start.sh"]

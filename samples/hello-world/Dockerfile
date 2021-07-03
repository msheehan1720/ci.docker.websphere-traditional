FROM ibmcom/websphere-traditional:8.5.5.19
USER was

RUN mkdir -p  /tmp/work/config

# Set WorkDir for OC
WORKDIR /tmp/work/

COPY . /tmp/work/

WORKDIR /tmp/work/config
COPY scripts/*  /tmp/work/config/

RUN  chmod 755  /tmp/work/

USER was
RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa /tmp/work/config/configure.sh

FROM ibmcom/websphere-traditional:8.5.5.19
USER was

RUN mkdir -p  /tmp/work/config

# Set WorkDir for OC
WORKDIR /tmp/work

COPY app.ear /tmp/work/config/app.ear 
COPY install_app.py /tmp/work/config/install_app.py
COPY was-config.props  /tmp/work/config/was-config.props
#COPY scripts/*   /work/
# RUN  chmod 755  /tmp/build/inputs/work
RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa /tmp/work/config/configure.sh

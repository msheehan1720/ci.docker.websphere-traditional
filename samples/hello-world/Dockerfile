FROM ibmcom/websphere-traditional:8.5.5.19
USER was

RUN mkdir -p  /work/config

# Set WorkDir for OC
WORKDIR /work

COPY app.ear /work/config/app.ear 
COPY install_app.py /work/config/install_app.py
COPY was-config.props  /work/config/was-config.props
#COPY scripts/*   /work/
# RUN  chmod 755  /tmp/build/inputs/work
RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa /work/config/configure.sh

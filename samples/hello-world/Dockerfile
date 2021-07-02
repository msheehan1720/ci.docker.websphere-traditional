FROM ibmcom/websphere-traditional:8.5.5.19
USER was
# RUN mkdir -p  /tmp/build/inputs/work/config
COPY app.ear /work/config/app.ear
COPY install_app.py /work/config/install_app.py
COPY was-config.props  /work/config/was-config.props
# COPY scripts/*   /tmp/build/inputs/work/
# RUN  chmod 755  /tmp/build/inputs/work
RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa  /work/config/configure.sh

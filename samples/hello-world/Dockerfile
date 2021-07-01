FROM ibmcom/websphere-traditional:8.5.5.19
RUN mkdir -p /tmp/work/config/
COPY app.ear /tmp/work/config/app.ear
COPY install_app.py /tmp/work/config/install_app.py
COPY was-config.props /tmp/work/config/was-config.props
COPY scripts/* /tmp/work/
RUN  chmod 755 /tmp/work
RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa /work/configure.sh

FROM ibmcom/websphere-traditional:8.5.5.19
# Set WorkDir for OC
WORKDIR /work

COPY app.ear /work/app.ear 
COPY install_app.py /work/config/install_app.py
COPY was-config.props /work/config/was-config.props

# USER was
# RUN env JVM_EXTRA_CMD_ARGS=-Xnoloa /tmp/work/config/configure.sh

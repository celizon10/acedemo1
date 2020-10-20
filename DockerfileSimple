FROM ibmcom/ace:latest
ENV LICENSE=accept
USER root
COPY ConsumoWSGenerico.bar /home/aceuser/bars/
RUN  chmod -R ugo+rwx /home/aceuser

USER aceuser
RUN source /opt/ibm/ace-11/server/bin/mqsiprofile && ace_compile_bars.sh

USER root
RUN  chmod -R ugo+rwx /home/aceuser

USER aceuser

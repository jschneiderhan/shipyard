FROM debian:jessie
RUN apt-get update && apt-get install -y ca-certificates less
ADD cli /bin/shipyard
ENV PROG shipyard
ADD .docker/autocomplete /.autocomplete
ADD .docker/bashrc /.bashrc
RUN /bin/shipyard --generate-bash-completion > /etc/bash_completion.d/shipyard
CMD ["/bin/bash"]

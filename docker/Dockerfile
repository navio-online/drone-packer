FROM salnikov/drone-plugin-base:v1.0.2

LABEL maintainer="Peter Salnikov peter@salnikov.cc" \
  org.label-schema.name="Drone.io plugin with Packer.io tool" \
  org.label-schema.vendor="Peter Salnikov"

ENV PACKER_VERSION 1.6.6
ENV PACKER_ARCH amd64

RUN set -e; \
	wget -q https://releases.hashicorp.com/packer/${PACKER_VERSION}/packer_${PACKER_VERSION}_linux_${PACKER_ARCH}.zip -O packer.zip; \
  	unzip packer.zip -d /bin ; \
  	rm -f packer.zip

COPY release/linux/amd64/drone-packer /bin/
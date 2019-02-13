FROM alpine:3.6
RUN apk -uv add --no-cache \
        python \
        py-pip \
        jq \
        groff \
        less \
        mailcap \
        unzip

ADD https://s3.amazonaws.com/aws-cli/awscli-bundle.zip /awscli-bundle.zip
RUN unzip awscli-bundle.zip
RUN ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
ADD config /root/.aws/ 
ENTRYPOINT ["/bin/bash"]

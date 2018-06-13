FROM alpine:latest
LABEL maintainer "Andrew Delianides <drew@delianides.com>"

RUN apk --no-cache add \
	ca-certificates \
	groff \
	less \
	python \
	py2-pip \
	&& pip install aws-sam-cli \
	&& mkdir -p /root/.aws \
	&& { \
		echo '[default]'; \
		echo 'output = json'; \
		echo 'region = $AWS_DEFAULT_REGION'; \
		echo 'aws_access_key_id = $AMAZON_ACCESS_KEY_ID'; \
		echo 'aws_secret_access_key = $AMAZON_SECRET_ACCESS_KEY'; \
	} > /root/.aws/config

ENTRYPOINT [ "sam" ]

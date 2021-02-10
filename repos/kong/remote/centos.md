## `kong:centos`

```console
$ docker pull kong@sha256:0cc576dd4ef99a2b49bae75fd85e6d493a777eacf8833dc5daa0c5de9564c261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:7bd92331a362473eb429c998283d4dd7c4d3ab81c7488f07b0e4c83fbcf7d253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793035e30a2dff29e7b79510065aef13499f016f8318e9a75377b095fc7d59e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
# Wed, 10 Feb 2021 19:21:43 GMT
# ARGS: KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 10 Feb 2021 19:21:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:43 GMT
USER kong
# Wed, 10 Feb 2021 19:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:43 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f33f2efc166cb5c8fe700bba55f203a47ac68805d7584af1566032ae9fdb8`  
		Last Modified: Wed, 10 Feb 2021 19:23:37 GMT  
		Size: 51.4 MB (51354495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c8c693e04f11baabbca865e259871d10ac47ad2086140fb01a92d250a28c6`  
		Last Modified: Wed, 10 Feb 2021 19:23:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

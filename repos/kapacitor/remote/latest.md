## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:85f4d66137e23ef33c68f0dc38344a78e4cf5c1b62a2cec6224e98aa35babfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:a4b03b00a2a79ddd0030143fe32c39ec8722b5eb6262eaa3d6e0278b62e73696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134578250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dbd6cef9c910481ef128df68501a0650fcbfcccb27106f370336706132bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:31 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 03 May 2023 16:09:42 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:42 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cd46b31d30fa84eb9b19625e6f729983f718960a32c93c5fe9cc8bd2e50c`  
		Last Modified: Wed, 03 May 2023 16:10:23 GMT  
		Size: 65.7 MB (65672194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120ea54647ec099a9b19129b4b91135f5ddb6073750d64a731feca9b2c2dfd8`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7cee67f7a88d03d99a4e6bbbadfd77e7964a038d55adcdcbb3408582942834`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ccbad14f6f29e1359be205a1f44f7a8d7789a66e125b54957287eb1ec7fa53e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125998583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6861c655d03d23bdedd6debba6a926bee408b88a8c43774d813d2c1ff158024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:38 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 04 May 2023 04:35:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:42 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77839c427eb747173165dfbef973f408a6fe250fe6bae52e65086a1fd4daec2c`  
		Last Modified: Thu, 04 May 2023 04:36:06 GMT  
		Size: 61.7 MB (61669485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca67377d0bebb900806f71c47d1efff8d4b32967b3e177b77a06b99329dd58b8`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2debaca8f8cfb74b0f5211a504bbb5d2ee1f607ee6531e87f49621ceda9b99`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

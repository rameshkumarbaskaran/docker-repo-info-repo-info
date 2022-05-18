## `docker:latest`

```console
$ docker pull docker@sha256:c24538b2a7a081efc81185772bd8066d33cbf1f3e1a8249657395bdad4d5f844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:f4fab13090bb25bc725f04b85b67fc47c6d5189b566fb375d4e16cec37ea25ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93861916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf52449ebd90bf825c3178851645d2b3a24a7c823d2ab78acb1d46ee8c1b1ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 19:19:27 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 19:19:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 19:19:33 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 19:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 18 May 2022 19:19:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.1
# Wed, 18 May 2022 19:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-x86_64'; 			sha256='d99de1ea7616f2a4c7914d37674f0650660a5e832be555805a71c0fc377233c9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-armv6'; 			sha256='86f2eafdb2ff1f3885758854dd5e1c5ea9d81aa292623829fd3babe9d3fc6f9a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-armv7'; 			sha256='f5a15fa6ef16f3c79cf8c2e965d7426d1f3968c273eb588c76d1f2851b1bf90f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-aarch64'; 			sha256='002662ed18a22d9d65d3d2c0358008c7c6a3db7dacb8983488130b3954d00e63'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-ppc64le'; 			sha256='83612098d39d3485945ee0d49f1ede02e0de96fbb7658202770aec6ae0834853'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-s390x'; 			sha256='68b9487106fd27e0f8c7defcf80fee2ab4f178f3ccc1d827fa0d2e82f80fa38b'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 18 May 2022 19:19:27 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 18 May 2022 19:19:27 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 18 May 2022 19:19:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 May 2022 19:19:28 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 18 May 2022 19:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 May 2022 19:19:28 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe685014da748bf20849321c180dea34882f4f7f0f6beedd2acd2515e0b7a73e`  
		Last Modified: Thu, 12 May 2022 19:20:37 GMT  
		Size: 65.5 MB (65503687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2351d0885d2e88e54bfb7c4366c4724f3506ee314056fcc1683a3e19ab80a3a`  
		Last Modified: Thu, 12 May 2022 19:20:27 GMT  
		Size: 14.5 MB (14454318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356b5f84352cbfcb710efd980a677cbd21d43c538f72952f884a92657574076c`  
		Last Modified: Wed, 18 May 2022 19:20:15 GMT  
		Size: 9.1 MB (9117903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15ec7fa702de0d03c32d5a400ac4368fbb90e13db81223c23570e73d32c8aec`  
		Last Modified: Wed, 18 May 2022 19:20:12 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382dd215f2e8fb7478a9c9ad88b1c1fe04933c3145bb115a274b8bd9b7b47a61`  
		Last Modified: Wed, 18 May 2022 19:20:12 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab41171eab524ece6448c9d01c3c323b47c39ffd63fe557bf5403671f9bba13b`  
		Last Modified: Wed, 18 May 2022 19:20:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:699930b5e058aa6d34118ca5259c86cbd8343c7337aa3de72084bee5ad7707a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86117837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8d5a60314f5e82454b07e428e107007fcca74e1866f10e21c9a747009b2e8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 12 May 2022 20:22:11 GMT
ENV DOCKER_VERSION=20.10.16
# Thu, 12 May 2022 20:22:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.16.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.16.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.16.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.16.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 12 May 2022 20:22:17 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Thu, 12 May 2022 20:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 18 May 2022 18:47:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.5.1
# Wed, 18 May 2022 18:47:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-x86_64'; 			sha256='d99de1ea7616f2a4c7914d37674f0650660a5e832be555805a71c0fc377233c9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-armv6'; 			sha256='86f2eafdb2ff1f3885758854dd5e1c5ea9d81aa292623829fd3babe9d3fc6f9a'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-armv7'; 			sha256='f5a15fa6ef16f3c79cf8c2e965d7426d1f3968c273eb588c76d1f2851b1bf90f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-aarch64'; 			sha256='002662ed18a22d9d65d3d2c0358008c7c6a3db7dacb8983488130b3954d00e63'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-ppc64le'; 			sha256='83612098d39d3485945ee0d49f1ede02e0de96fbb7658202770aec6ae0834853'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.5.1/docker-compose-linux-s390x'; 			sha256='68b9487106fd27e0f8c7defcf80fee2ab4f178f3ccc1d827fa0d2e82f80fa38b'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 18 May 2022 18:47:25 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 18 May 2022 18:47:26 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 18 May 2022 18:47:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 May 2022 18:47:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 18 May 2022 18:47:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 May 2022 18:47:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ab1135c7b721be883fc7e150da6fb11bb54eccc859ad4ffbcb533f793e0cdf`  
		Last Modified: Thu, 12 May 2022 20:24:02 GMT  
		Size: 60.0 MB (60009124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b01c7da2e2cebadd6b24ab7657beaa4eeb2a2108384a1fee4235d78827ae79`  
		Last Modified: Thu, 12 May 2022 20:23:53 GMT  
		Size: 13.1 MB (13097907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a612f6045b86400067ed1077c75b0495c37e839840fc464ec0ec7438a722d38`  
		Last Modified: Wed, 18 May 2022 18:48:53 GMT  
		Size: 8.4 MB (8353570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a41c283750ce1ae9f7de5609a3c971b86a2be4c312163e3e1065b39e2248023`  
		Last Modified: Wed, 18 May 2022 18:48:52 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9c06fd30af63bc6fb46e58b7e64cc9bfee7021d0c15d8a378d6b7e5444f9f4`  
		Last Modified: Wed, 18 May 2022 18:48:52 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0e27cc953e15d9bf4747a7850904930f347b805563df85dc811859a98d279d`  
		Last Modified: Wed, 18 May 2022 18:48:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

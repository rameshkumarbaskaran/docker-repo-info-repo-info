## `docker:20-cli`

```console
$ docker pull docker@sha256:152d5e0d4421f0b77021ee58e6469fc25e474a1f6c50ef4d7e9f6b3d28c66149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-cli` - linux; amd64

```console
$ docker pull docker@sha256:43bdf0e544ffdf2c90e107bac3b8fb258f62767ba965ab900ab0a180cc014e88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49099237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1568db95bf0e609f43c60c8b870806d440463c9825801f647fa17165310842fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:27:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:27:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 16 Dec 2022 23:19:56 GMT
ENV DOCKER_VERSION=20.10.22
# Fri, 16 Dec 2022 23:19:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 16 Dec 2022 23:19:59 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 16 Dec 2022 23:20:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 16 Dec 2022 23:20:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.1
# Fri, 16 Dec 2022 23:20:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-x86_64'; 			sha256='e0c916bd108c49830c7847e416787387398f97de8dda7c1c35dad59438692664'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv6'; 			sha256='7345474ef0ce498a9e7befb14679d8ba86b8a03e81072cd9cfa4e0345b2eb1d6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv7'; 			sha256='4f283a2341f8faa9dd58fd68ffa45bc4909051ab8d8f376998155ec0a3d4123e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-aarch64'; 			sha256='49924009641e9a60f178b4085c9d308bb726b5ae74eed46c5d1a7dbc8f04948b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-ppc64le'; 			sha256='6699d98c002532f719954ecf8737dfed39d0fd079c71438f04fe0ee63d23f0f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-riscv64'; 			sha256='c5a51c7db8b8008d4645241d917afbbb752829753c83858e030154e8c541d827'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-s390x'; 			sha256='44b132059a2162834e7f7c285362f5a007f2569943496cc1656cce8aaea0dd2b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 16 Dec 2022 23:20:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 16 Dec 2022 23:20:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 16 Dec 2022 23:20:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Dec 2022 23:20:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 16 Dec 2022 23:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Dec 2022 23:20:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eea1d5d8e5eb7f3c01c44eb6652605d4b5ad66cf819d1e3b6053733f2f13cf`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 2.1 MB (2064254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41ddca615c02560ac2876c1f1a4f4f0c2fe3f8b091488146e1098c5a3eda4`  
		Last Modified: Fri, 16 Dec 2022 23:22:29 GMT  
		Size: 14.0 MB (13982924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76f94013e41735f015f26d3c3df1af256e1fd761926325deaf30759c53494`  
		Last Modified: Fri, 16 Dec 2022 23:22:28 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256b0baef9196ccbec2696ad6be51a3e03ad3376ddbbbfb43f19898308f5580b`  
		Last Modified: Fri, 16 Dec 2022 23:22:28 GMT  
		Size: 14.5 MB (14475523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45215825310c523f73b619ff14c04ce8eb36405e9f6095ab8a631d11fea7eba`  
		Last Modified: Fri, 16 Dec 2022 23:22:25 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f18bb8965191d83cab4b171cd0049ea9e38db21fdb8bc5bff67419277be8244`  
		Last Modified: Fri, 16 Dec 2022 23:22:25 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d8f2af193482b071cedabfa6e5019c818764c9c0477b36251ec74ea61ede8b`  
		Last Modified: Fri, 16 Dec 2022 23:22:25 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8f9dfcb6e94078ec4bf7f7dd4de7ad8eefcfa58f5153e29c586a23143ac5f354
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44870241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beb9c80710f8ed6c5ac6e88b65ff2a8e1e38ed591ab51911ea05fa7b793dffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:42:08 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:42:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 17 Dec 2022 00:10:28 GMT
ENV DOCKER_VERSION=20.10.22
# Sat, 17 Dec 2022 00:10:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Sat, 17 Dec 2022 00:10:31 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Sat, 17 Dec 2022 00:10:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Sat, 17 Dec 2022 00:10:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.1
# Sat, 17 Dec 2022 00:10:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-x86_64'; 			sha256='e0c916bd108c49830c7847e416787387398f97de8dda7c1c35dad59438692664'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv6'; 			sha256='7345474ef0ce498a9e7befb14679d8ba86b8a03e81072cd9cfa4e0345b2eb1d6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv7'; 			sha256='4f283a2341f8faa9dd58fd68ffa45bc4909051ab8d8f376998155ec0a3d4123e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-aarch64'; 			sha256='49924009641e9a60f178b4085c9d308bb726b5ae74eed46c5d1a7dbc8f04948b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-ppc64le'; 			sha256='6699d98c002532f719954ecf8737dfed39d0fd079c71438f04fe0ee63d23f0f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-riscv64'; 			sha256='c5a51c7db8b8008d4645241d917afbbb752829753c83858e030154e8c541d827'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-s390x'; 			sha256='44b132059a2162834e7f7c285362f5a007f2569943496cc1656cce8aaea0dd2b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Sat, 17 Dec 2022 00:10:35 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 17 Dec 2022 00:10:35 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 17 Dec 2022 00:10:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Dec 2022 00:10:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 17 Dec 2022 00:10:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Dec 2022 00:10:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5dec0c1f562bd55dc773ccc0c77fbfd42b92083262478523c19bcc0f397af`  
		Last Modified: Tue, 29 Nov 2022 01:44:14 GMT  
		Size: 2.0 MB (2036851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9db874a82a64c48213d6d1ce2e45eb51359f913358fa4d785dd4a6d5219631c`  
		Last Modified: Sat, 17 Dec 2022 00:12:52 GMT  
		Size: 12.7 MB (12743372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcbc5124e189b1ab3f0affe49da5b5b8037788919a0816840b1270409f1a3c`  
		Last Modified: Sat, 17 Dec 2022 00:12:50 GMT  
		Size: 13.8 MB (13764588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72fa76bd9d2fe5fda767e1b0805469eb3258b132f00349cc1ebfbf325a7cb4f`  
		Last Modified: Sat, 17 Dec 2022 00:12:50 GMT  
		Size: 13.1 MB (13064523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836018a3625eb50693acce251fc6536efc021e3a152aa3671e28c5ca30636153`  
		Last Modified: Sat, 17 Dec 2022 00:12:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794fa229654af9280c20d7c773573039a8088f8565035ebd9f99c1ae01784e5b`  
		Last Modified: Sat, 17 Dec 2022 00:12:48 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67328db4c6997d483c4608b89e5970d08986402dedffa8c153c0c7fca0b826e0`  
		Last Modified: Sat, 17 Dec 2022 00:12:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

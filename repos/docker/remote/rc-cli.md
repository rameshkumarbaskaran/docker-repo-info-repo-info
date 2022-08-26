## `docker:rc-cli`

```console
$ docker pull docker@sha256:2ce64c2bb9b164d30ba42b07e3854047be0c290d8acdeceed2ea1f3822dada72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:dc6a996c40c3f8363019e9ac1c145887406e97de47449bb7b3ee41fc1a37a50d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38105343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9f0e06f75e680979058407b7aa57cfc46f86e1008f38fb002ff07f7ba6f6c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:20:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:20:49 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:20:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 00:19:27 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 00:19:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 26 Aug 2022 21:19:34 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.2
# Fri, 26 Aug 2022 21:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-x86_64'; 			sha256='41e9657c8abd7d656c3a40df1ae9c1171930313707a3abd5420ec8852b59eeb7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv6'; 			sha256='56fe4280d29c8714ef63e3e8de039522b519a1cdcfb577c1c02c7c00f581e326'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv7'; 			sha256='709aa427507a3a064d822977d2b1d68a0bd78a114c714970033b5e6731f9879b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-aarch64'; 			sha256='dcac4e71c52264a795d0271b36cd6b2ea0ac266931618fab2e9e9a803ed16a4a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-ppc64le'; 			sha256='5c1b7a13f39aa24d3369954f692aee776d9621a3cad4ddd513aa26918debd202'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-riscv64'; 			sha256='4bf02048f307cf1e8b432c18aee33022be50562d52afbab09d28e90cbff9e900'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-s390x'; 			sha256='a29c82751b14f2693933ddbfc00c464fc3d78143f534024244e915880ed15760'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 26 Aug 2022 21:19:36 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 26 Aug 2022 21:19:36 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:19:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Aug 2022 21:19:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 26 Aug 2022 21:19:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Aug 2022 21:19:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb510456a427665c9755e7417ad432e68b6e95a1a9a6665f72f0adc6f9ec59d`  
		Last Modified: Tue, 09 Aug 2022 18:22:44 GMT  
		Size: 2.0 MB (2036045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4627ba0696d0614a94c97a4b5c212e055112e2a8f0831f342f3b138955035153`  
		Last Modified: Tue, 09 Aug 2022 18:22:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d957832b8a49136f6d95f00340a0c764c8cd051be7514885f8fca6a80053215`  
		Last Modified: Tue, 09 Aug 2022 18:22:45 GMT  
		Size: 8.7 MB (8706435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd48969715b862016850752e05193de3fe3dbc355a5f277cece7c52d69f4793`  
		Last Modified: Fri, 19 Aug 2022 00:21:18 GMT  
		Size: 15.2 MB (15204103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662ab5956f372eb03903b2f30f2917fba2df1b772ef5ad2a8f4aa37e4603bd98`  
		Last Modified: Fri, 26 Aug 2022 21:21:23 GMT  
		Size: 9.4 MB (9350823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67568ea02f35ae316b695fb1a5c465155b8240f2956606c38109cc605bbcbc0`  
		Last Modified: Fri, 26 Aug 2022 21:21:21 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442023e64d834b5cb199c83a20c32ea72b1a900b84a6ed49e7144f6adbe600f7`  
		Last Modified: Fri, 26 Aug 2022 21:21:21 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a036a3ca23be8529cd90603e16a2955ff8b72a22364e34329fba92621ccaa0b`  
		Last Modified: Fri, 26 Aug 2022 21:21:21 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:960f27860d6c891f8ee7b6a7f6684792e1a6c9a32c11baec66bbd39a96ded72f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35100170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa50ea2d8f503f74f27d3a2c03ebc49eb08a81c3ae9e7430d6762b50bd576bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:24:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:24:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:24:50 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 09 Aug 2022 18:24:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 02:45:35 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 02:45:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 26 Aug 2022 21:45:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.2
# Fri, 26 Aug 2022 21:45:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-x86_64'; 			sha256='41e9657c8abd7d656c3a40df1ae9c1171930313707a3abd5420ec8852b59eeb7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv6'; 			sha256='56fe4280d29c8714ef63e3e8de039522b519a1cdcfb577c1c02c7c00f581e326'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv7'; 			sha256='709aa427507a3a064d822977d2b1d68a0bd78a114c714970033b5e6731f9879b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-aarch64'; 			sha256='dcac4e71c52264a795d0271b36cd6b2ea0ac266931618fab2e9e9a803ed16a4a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-ppc64le'; 			sha256='5c1b7a13f39aa24d3369954f692aee776d9621a3cad4ddd513aa26918debd202'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-riscv64'; 			sha256='4bf02048f307cf1e8b432c18aee33022be50562d52afbab09d28e90cbff9e900'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-s390x'; 			sha256='a29c82751b14f2693933ddbfc00c464fc3d78143f534024244e915880ed15760'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 26 Aug 2022 21:45:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 26 Aug 2022 21:45:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:45:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Aug 2022 21:45:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 26 Aug 2022 21:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Aug 2022 21:45:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd6445c68b28c4fea9c5ead64de6d84bfbcf44d2ea150df466f2efe4ca7ac8`  
		Last Modified: Tue, 09 Aug 2022 18:28:29 GMT  
		Size: 2.0 MB (2010519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6c1cdde4920e39b02e2eaa9a348dd527a363263a4901b3efdf13020d24a917`  
		Last Modified: Tue, 09 Aug 2022 18:28:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1503a42e3097b1eaf3bbc5e72622fc4950bd97ec2439372d2daf9fe4324a21b5`  
		Last Modified: Tue, 09 Aug 2022 18:28:30 GMT  
		Size: 8.0 MB (8048680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f94397c525f39d44ef3fda3b0bba921a889eb33ccc36156f3ba73a88804a75`  
		Last Modified: Fri, 19 Aug 2022 02:49:05 GMT  
		Size: 13.8 MB (13764592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b4e4e671858a85081e13d11482fe7ebba5f1b9196b504e867eb817f8214a41`  
		Last Modified: Fri, 26 Aug 2022 21:49:02 GMT  
		Size: 8.6 MB (8566866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbdbad9f10e9712da075acc34f7e4200fbebe460a358b0c4847a214b7f0842e`  
		Last Modified: Fri, 26 Aug 2022 21:49:01 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bd3c02ddde77f0f1700ea080588ae89c8c53b856c39765be1d3f0a7cf156cd`  
		Last Modified: Fri, 26 Aug 2022 21:49:01 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b184dda7a9fb6193d06ec49c81c79dbbfc69d6c31405abbe859d30ecb726c64`  
		Last Modified: Fri, 26 Aug 2022 21:49:01 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:79f5cf744ab66c48ff532b8dea2662dc90db30faded68ff7b33ce7109578ca7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:e25a101eb5ee4bc8772e862e908a33a133feb067a6d0d4a19cb7753d64596889
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a71aa007f99e9f0cf416d976f494e0a9781e546803fe58e931d63e978511d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:20:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:21:25 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 09 Aug 2022 18:21:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 00:19:59 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 00:20:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 26 Aug 2022 21:20:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.2
# Fri, 26 Aug 2022 21:20:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-x86_64'; 			sha256='41e9657c8abd7d656c3a40df1ae9c1171930313707a3abd5420ec8852b59eeb7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv6'; 			sha256='56fe4280d29c8714ef63e3e8de039522b519a1cdcfb577c1c02c7c00f581e326'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv7'; 			sha256='709aa427507a3a064d822977d2b1d68a0bd78a114c714970033b5e6731f9879b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-aarch64'; 			sha256='dcac4e71c52264a795d0271b36cd6b2ea0ac266931618fab2e9e9a803ed16a4a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-ppc64le'; 			sha256='5c1b7a13f39aa24d3369954f692aee776d9621a3cad4ddd513aa26918debd202'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-riscv64'; 			sha256='4bf02048f307cf1e8b432c18aee33022be50562d52afbab09d28e90cbff9e900'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-s390x'; 			sha256='a29c82751b14f2693933ddbfc00c464fc3d78143f534024244e915880ed15760'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 26 Aug 2022 21:20:09 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 26 Aug 2022 21:20:09 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:20:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Aug 2022 21:20:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 26 Aug 2022 21:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Aug 2022 21:20:10 GMT
CMD ["sh"]
# Fri, 26 Aug 2022 21:20:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 26 Aug 2022 21:20:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 26 Aug 2022 21:20:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 26 Aug 2022 21:20:23 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 26 Aug 2022 21:20:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 26 Aug 2022 21:20:23 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:20:23 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Aug 2022 21:20:24 GMT
EXPOSE 2375 2376
# Fri, 26 Aug 2022 21:20:24 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Aug 2022 21:20:24 GMT
CMD []
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
	-	`sha256:e001120e1cd4a7ea1ec2535b3ff388987a6bf3f3bd1568ba33de8157170276df`  
		Last Modified: Tue, 09 Aug 2022 18:24:12 GMT  
		Size: 13.7 MB (13668392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3ada922ff1d635680390f511fa096205beea3f4dc80a7fd4774133e9a572a7`  
		Last Modified: Fri, 19 Aug 2022 00:22:45 GMT  
		Size: 15.2 MB (15204102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14644374e46c13a59cdea6d91c637b0d7b65cf436846073eaec90ca0312960c`  
		Last Modified: Fri, 26 Aug 2022 21:22:52 GMT  
		Size: 9.4 MB (9350838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de03787241b3d3462294874734830f46526512dedd2b5f492815c1cff248795`  
		Last Modified: Fri, 26 Aug 2022 21:22:50 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89f86b0af451c4ee6e0dc35ae5a412af6f697b798c17e49f1c39027d41d1e77`  
		Last Modified: Fri, 26 Aug 2022 21:22:50 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f2e1afd0a536ee8aeeb44e9d749337aea3c6d3f2100c260ceb17864ea42f26`  
		Last Modified: Fri, 26 Aug 2022 21:22:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c49aa2ebd1ffef9402c408cbddbaa6cd2ed987854fbfb46018ea8d64d54ee`  
		Last Modified: Fri, 26 Aug 2022 21:23:25 GMT  
		Size: 6.9 MB (6863626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c179b2bb07905bdb480e7089a50f9b660e4168a183bea40afc9d12def6e61ff2`  
		Last Modified: Fri, 26 Aug 2022 21:23:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7290a2e4af5941fdf9e289ffe81001d44d6751ce821459617d7f9774b65db3`  
		Last Modified: Fri, 26 Aug 2022 21:23:32 GMT  
		Size: 51.8 MB (51847179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4eaf3080973019413a039000de2d422a79542744e6ce37a1d3f9e9be3f72a42`  
		Last Modified: Fri, 26 Aug 2022 21:23:24 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e30de05d583ab4f9dc66038c495ddd768b6b8a3ad3a44a5e42bac0804a1111`  
		Last Modified: Fri, 26 Aug 2022 21:23:24 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:81c60e465135f58ad890950ccd780a7baf4f2a0a42e1f03c32884ce86cca77aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93817611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee99f16a2c37609008446d78773552ed7d8c2761620a3ca1be5ac169add247e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:24:48 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 09 Aug 2022 18:24:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:25:59 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 09 Aug 2022 18:26:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 19 Aug 2022 02:46:39 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Fri, 19 Aug 2022 02:46:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 26 Aug 2022 21:46:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.10.2
# Fri, 26 Aug 2022 21:46:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-x86_64'; 			sha256='41e9657c8abd7d656c3a40df1ae9c1171930313707a3abd5420ec8852b59eeb7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv6'; 			sha256='56fe4280d29c8714ef63e3e8de039522b519a1cdcfb577c1c02c7c00f581e326'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-armv7'; 			sha256='709aa427507a3a064d822977d2b1d68a0bd78a114c714970033b5e6731f9879b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-aarch64'; 			sha256='dcac4e71c52264a795d0271b36cd6b2ea0ac266931618fab2e9e9a803ed16a4a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-ppc64le'; 			sha256='5c1b7a13f39aa24d3369954f692aee776d9621a3cad4ddd513aa26918debd202'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-riscv64'; 			sha256='4bf02048f307cf1e8b432c18aee33022be50562d52afbab09d28e90cbff9e900'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-s390x'; 			sha256='a29c82751b14f2693933ddbfc00c464fc3d78143f534024244e915880ed15760'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 26 Aug 2022 21:46:51 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 26 Aug 2022 21:46:52 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:46:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Aug 2022 21:46:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 26 Aug 2022 21:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Aug 2022 21:46:55 GMT
CMD ["sh"]
# Fri, 26 Aug 2022 21:47:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 26 Aug 2022 21:47:07 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 26 Aug 2022 21:47:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 26 Aug 2022 21:47:12 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 26 Aug 2022 21:47:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 26 Aug 2022 21:47:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 26 Aug 2022 21:47:15 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Aug 2022 21:47:16 GMT
EXPOSE 2375 2376
# Fri, 26 Aug 2022 21:47:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Aug 2022 21:47:18 GMT
CMD []
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
	-	`sha256:596c126c4e7f951be440ca6dc23043be252de5144fad72341963255f4d1f60e1`  
		Last Modified: Tue, 09 Aug 2022 18:30:10 GMT  
		Size: 12.5 MB (12500816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8becc8c0570807fac1996ee4346147c87042c21f1be006ff348008880d3d4`  
		Last Modified: Fri, 19 Aug 2022 02:50:38 GMT  
		Size: 13.8 MB (13764592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea667192263cae58bce02bedc96031ac47eed9e506ffcb10a1d2829d21a069e7`  
		Last Modified: Fri, 26 Aug 2022 21:50:35 GMT  
		Size: 8.6 MB (8566870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a7ab4d88c326a19ea88e0bf88832c9b93a14c1dc43234a61ccc0f5a9894cc4`  
		Last Modified: Fri, 26 Aug 2022 21:50:34 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cae75ca6574de332b886e49492c5923146ee3a21b6237cfad0f4ac50ef0d74b`  
		Last Modified: Fri, 26 Aug 2022 21:50:34 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247b6cb961d6db82e288e89b971c86dff147c301739d6989fe356aed487e163f`  
		Last Modified: Fri, 26 Aug 2022 21:50:34 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a0e971df4f9e3cbde3f706847461a4835d8b06f44064818cc34d3de86b60a`  
		Last Modified: Fri, 26 Aug 2022 21:51:13 GMT  
		Size: 6.7 MB (6736619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ac4af9a3df5ad2e16841110d7702a624f32d8fb9abc735a40ebca982f3083`  
		Last Modified: Fri, 26 Aug 2022 21:51:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b6233fbbbc79b64bb3d48c4fd7f65d2f7f823465359ea54b1cc684930c0afa`  
		Last Modified: Fri, 26 Aug 2022 21:51:20 GMT  
		Size: 47.5 MB (47523672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2bf28fa75725aaa6d149a908b209cd88fcbbedd332940d697a9ccf387934c5`  
		Last Modified: Fri, 26 Aug 2022 21:51:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eecd4a8db463cf0d6b30b3cd090efb544e24f850b78984194a22413cf97423c`  
		Last Modified: Fri, 26 Aug 2022 21:51:12 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

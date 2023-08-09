## `traefik:beaufort`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

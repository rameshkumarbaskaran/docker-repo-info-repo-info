## `docker:test-dind`

```console
$ docker pull docker@sha256:308dcf9380af44ea492736e8d59605cd0ff2dab0527073f7e718ee4498e85dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:0e6d34042007a6f5280838dc045af0d600654b57cd367251d1dd8bba4b55c773
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98abf5dda7ec569bc4821f20ceca66945e67882fe32f960fb8b8f179af0e42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:04246f289e63b1bc0baf3ee051e2374497207183b9e5b86373aa2f8938893a6c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68121997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fff432f3d4cd1dae7778792ad2daa258d095691556f760fe82584bb66fa2b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 05:52:35 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:49:22 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:49:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:49:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:49:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:38 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:49:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:49:48 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:49:49 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:49:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:49:51 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:49:52 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:49:52 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:49:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:49:53 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592a77d3ce3aac4cb4c252c866f4a65c1541726b2bbdb512444569119b5cd98e`  
		Last Modified: Wed, 11 Mar 2020 21:50:37 GMT  
		Size: 59.9 MB (59927165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ab691262af1bf0bf50d6d459874dbf48509a6103991fd9d6225e455cb995`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320285a35393ed08c2ed85f5dc6d6ca6a1c07ac14fcfb8b4e1e5c5a4c30eace9`  
		Last Modified: Wed, 11 Mar 2020 21:50:17 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e82c58148faac404a83fad42819c701567beb61dac6c2ae6d76ac1f97eefccd`  
		Last Modified: Wed, 11 Mar 2020 21:50:18 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1648a96394c26b0e7d5c254c39b36c8eca6d00dfff5aa3776cb6671284ead`  
		Last Modified: Wed, 11 Mar 2020 21:50:49 GMT  
		Size: 3.2 MB (3215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63bc9624da4519af0d163fc47db94ef5d7d0ae27deccb9d6b923ba97710251`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8f7907ef28cfa8968f389a0e60d2b4a98f2b9da2963e09d86911a36e945825`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cac041612fcb3b3db97e63f70c7f357b31618cd79f2a0852b38181355f5bd`  
		Last Modified: Wed, 11 Mar 2020 21:50:48 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c2d6834d581a10f8d30ae8678d859ad15a3747335051665f21dbe7e602568a8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67486006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd179934e0f1561bdac8a67db9bf33af7be9c1f7508bdb0c7aa76184817e0d62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 03:01:20 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:57:34 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:57:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:57:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:57:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:57:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:57:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:57:48 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:57:57 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:57:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:58:00 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:58:02 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:58:02 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:58:03 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:58:03 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:58:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:58:05 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca62e39536ad2825e9d1db7dbfa88f4cbc9d95659c5fb45691fa224654d2629`  
		Last Modified: Wed, 11 Mar 2020 21:58:49 GMT  
		Size: 59.9 MB (59927053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a96da9a069c4780e3c46bcbd35f4da5d0e173b2888bec333941260f131ccc8`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202349aaae9b658c7d87822ac340735af35c35495f6af77e5db0df2d253880ea`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ed55770aa202e0a559ef5505907bdf9e16eb7ea47829463da52a02907f9c`  
		Last Modified: Wed, 11 Mar 2020 21:58:28 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466cffcfbb54d45db4bfc4d2a4ef125228d8adaa890f4bdf1b64c9305a00e67b`  
		Last Modified: Wed, 11 Mar 2020 21:59:01 GMT  
		Size: 2.9 MB (2878539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6759e573461d1a01a039d460c93cc7394fc6503dcbb5a199b318c51ea84a5b7`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db51a4792cce56454199be1d125345ae07f763e4fda4f56a955259f1ecba93`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600fa87244d5da05152b4c389cc3f37aaf0b36cb70a7d0d4294feaeb52abbd12`  
		Last Modified: Wed, 11 Mar 2020 21:59:00 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6fcdb8d75a9f4a6ee01e57720cb5543bd81035db06ec821383dfde6a4371389e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68163443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71857cf4ec95c719133d716baecc805697ff6ca79086a80b6e14a77d43d3bc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:23:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 02:23:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 02:23:12 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 11 Mar 2020 21:39:44 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:39:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:39:56 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:40:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:40:08 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:40:08 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:40:10 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:40:11 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:40:12 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:40:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:40:13 GMT
CMD []
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2917335fcb0a6856d5bf55430ba707c2c1378029a109e61959e62d2769230db`  
		Last Modified: Sat, 18 Jan 2020 02:25:35 GMT  
		Size: 2.4 MB (2445713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3c84c2515134ddfa5ae5bac6e140953e9576fcd30a0bbc10fbc565d267895`  
		Last Modified: Sat, 18 Jan 2020 02:25:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828ac2f8d0e08bfd3c5405031bb245a21e469671397bd03e8868ce0925d9f49`  
		Last Modified: Wed, 11 Mar 2020 21:40:56 GMT  
		Size: 57.4 MB (57387269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7b0e4ac96f123613bb6ebd37a1bb99fb6f8a12b1d521f89f4211a970dbc077`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25581ce9dd66a29fecb3a63c9f888a0c6e3c68de7002441092b6a41dd833e995`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58c5fdb432f00e6a7cdfa6b6507ca3c8598ab0612730e109e4faf5b0fc2d5a`  
		Last Modified: Wed, 11 Mar 2020 21:40:37 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396bfbbbaa91436006cf0e8b86b9e00c9e49a1dcbcd557c3fc331afc8e9e2f3`  
		Last Modified: Wed, 11 Mar 2020 21:41:09 GMT  
		Size: 5.6 MB (5600915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bdb37e40cba208e5d80d500a33700bdff3ad30ebbfcb014c89a614506038d`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269e23372e2e87311644e618cb3e6c09eae4cc41d919662298578a9abfe476ed`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6204a0f4fef03aefb0b6ae2c7dfee680f8a6d84e0f59324ded513c256255723`  
		Last Modified: Wed, 11 Mar 2020 21:41:07 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

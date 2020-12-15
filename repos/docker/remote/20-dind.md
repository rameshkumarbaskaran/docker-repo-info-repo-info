## `docker:20-dind`

```console
$ docker pull docker@sha256:53132d9a17c4027f0c254a22ad66a27e3a6c159da4b38099d7dd50f4b66322c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:be20acdedb34b6b09b6f6379c84dffb750b5bb0a88c3b0047a790408e5813b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80298066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90109ab0c2dc17a53d4b154aa8295a94338f5a3d044886bd72aa4b5b5fa6cac7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:29:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 05:29:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:29:34 GMT
ENV DOCKER_VERSION=20.10.0
# Fri, 11 Dec 2020 05:29:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.0.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Dec 2020 05:29:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Dec 2020 05:29:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Dec 2020 05:29:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Dec 2020 05:29:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:29:42 GMT
CMD ["sh"]
# Sat, 12 Dec 2020 18:12:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 12 Dec 2020 18:12:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 12 Dec 2020 18:12:31 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Sat, 12 Dec 2020 18:12:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 12 Dec 2020 18:12:32 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Sat, 12 Dec 2020 18:12:33 GMT
VOLUME [/var/lib/docker]
# Sat, 12 Dec 2020 18:12:33 GMT
EXPOSE 2375 2376
# Sat, 12 Dec 2020 18:12:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 12 Dec 2020 18:12:33 GMT
CMD []
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db28d0fdbf69ee580b35224bf77ef5e71f9a061c0aafab87064af9708035d9d`  
		Last Modified: Fri, 11 Dec 2020 05:31:33 GMT  
		Size: 2.0 MB (2039048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292df0bc6bf3350f306af7623bc14f00386239bb27303d3047104b9cfdb55460`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e060f4bd70b333ccaa7ae441b42f1068621b39bbe8eb9c71b5a4e06d10b4ff3`  
		Last Modified: Fri, 11 Dec 2020 05:31:46 GMT  
		Size: 69.5 MB (69457871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e8d568a22304aafab5a456040525abd0b705efad0b6e60e64847ebe1c6e4e6`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6ef1a942a0f6b2ab0993eecb7ce30d31f06af50a2ae40893e1a160c9a0892`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312dd95470aa8eaccef80bbca7892390ca777559b50fab574e65147a35107fc`  
		Last Modified: Fri, 11 Dec 2020 05:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c897205648b865ec45efcc0c0be8a3ccf9f3f3f60cc1383d5564c72302e20`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 6.0 MB (5997645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa8e83a7aeb20771ef165f19449f2733ae1aee4c6efe28b6b2e4109ef65baa8`  
		Last Modified: Sat, 12 Dec 2020 18:13:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b1eb2027ff8834916826431c1bdd26901ee758dfb9877c38275a4e62239295`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36cacd847e245cd8b2f813f5cba87f6b5fff177d7845e4cb1b290d27466ebe6`  
		Last Modified: Sat, 12 Dec 2020 18:13:32 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8c19dfcfaf8ed173294c658d7b23057a0d0b6b4312fe9b6dc13da0efe74b8ded
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74320964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025d723c8491966a6c2d86dc23ced734b813ae430c76a13765731eddd5e78f76`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 03:42:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 11 Dec 2020 03:42:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 15 Dec 2020 21:39:43 GMT
ENV DOCKER_VERSION=20.10.1
# Tue, 15 Dec 2020 21:39:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.1.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 15 Dec 2020 21:39:52 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 15 Dec 2020 21:39:53 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 15 Dec 2020 21:39:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 15 Dec 2020 21:39:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 15 Dec 2020 21:39:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Dec 2020 21:39:57 GMT
CMD ["sh"]
# Tue, 15 Dec 2020 21:40:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 15 Dec 2020 21:40:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 15 Dec 2020 21:40:10 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Tue, 15 Dec 2020 21:40:12 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 15 Dec 2020 21:40:13 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Tue, 15 Dec 2020 21:40:13 GMT
VOLUME [/var/lib/docker]
# Tue, 15 Dec 2020 21:40:14 GMT
EXPOSE 2375 2376
# Tue, 15 Dec 2020 21:40:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 15 Dec 2020 21:40:15 GMT
CMD []
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a3295e0d61f852e263682a8285a62d0f4f5832be86af681abc9950847b3bf5`  
		Last Modified: Fri, 11 Dec 2020 03:44:52 GMT  
		Size: 2.1 MB (2061244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f2e6d810069d5f3f3f5d961a35cf03d93a9046b8c37f0c5ad37b6c975f42b`  
		Last Modified: Fri, 11 Dec 2020 03:44:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065c9533d613f2ec83932a39b34dd070a6bc11a62728064fd0ef06a4a0727939`  
		Last Modified: Tue, 15 Dec 2020 21:41:27 GMT  
		Size: 63.6 MB (63559834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fce0df16b8b1ec61e4c50c6e5a2af03b003c2ccb2962ae187ed8b4d8582789d`  
		Last Modified: Tue, 15 Dec 2020 21:41:09 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3faa53604c1bb48243fc9e9567ef34361ab3e75713b4c29619ddb54b0660216`  
		Last Modified: Tue, 15 Dec 2020 21:41:09 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5adaa20535c0e5874ed5813909c5db319ca5cf7486e3976de2de50213e253`  
		Last Modified: Tue, 15 Dec 2020 21:41:09 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd6a892024d107c8535c35d337be5424328e36d9818d082e9dbaa4cf8c9187`  
		Last Modified: Tue, 15 Dec 2020 21:41:42 GMT  
		Size: 6.0 MB (5986639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79706990dbba588cd3c809b791fa8a2b61e98d5c6630a335907e7db654f40130`  
		Last Modified: Tue, 15 Dec 2020 21:41:42 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee5ea310dc8d269579e72ee6aee916e70bd76a100785f5739c11103e7064eb6`  
		Last Modified: Tue, 15 Dec 2020 21:41:40 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bf15477df4235fe549a21e3a677f7a149c80c277a905d79772f8a381962206`  
		Last Modified: Tue, 15 Dec 2020 21:41:40 GMT  
		Size: 2.5 KB (2514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:87d687f262c3953aaed3404b70a39a7cc0cf84c09269d317dfbee7a3587d5cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ba9a867298f514f0155fc0015a88624808e42c513196c562d22d8b37dda7e8a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101261107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004b0ab8718ed6fab023f19e76b5bcd1db501061987c8a2d3fb61965d8a62c25`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:19:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:19:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:19:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:19:57 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:57 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:19:58 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:19:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:58 GMT
CMD []
# Thu, 03 Dec 2020 01:20:03 GMT
RUN apk add --no-cache iproute2
# Thu, 03 Dec 2020 01:20:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 03 Dec 2020 01:20:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:20:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 03 Dec 2020 01:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 03 Dec 2020 01:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Dec 2020 01:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d41eb34354d9c453eb21d4d874b79246fdde42e242ce3b3946e3fb08cd77b1`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 6.0 MB (5958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049752a368345c7b7d2d9539852eeac961803cd38f17028532ee69a4294dfa9`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238431a551c0fd0e6304bda8ab6e3806b3407161b0ddaaa51d97ea7c01ee9172`  
		Last Modified: Thu, 03 Dec 2020 01:21:09 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff110f4494d28d0434d2149ac8619524c81c1701c64fce9a08150d3c6134704`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbfa1b4e2ec98111aa0501360a509205fbf16bc526d399cfa670d0c35b6046`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.1 MB (1092668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f728936c6fdb24935e0bb1366ed702b917e9581519d22efab93f8728513a259a`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b638cd1abd59f9f12d28d5d6227cdb991c66c16fd6f9b00dc39564d1583b251`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cac38aa50f31cfa5934d05e52f6ff76d5b8809a374846c9b36af98c8f5a822`  
		Last Modified: Thu, 03 Dec 2020 01:21:21 GMT  
		Size: 20.2 MB (20171300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbc24424926ce09c4f9387a3510fe8d83e0d537f83a25565d4d6f8eb4a43a50`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

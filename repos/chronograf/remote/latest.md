## `chronograf:latest`

```console
$ docker pull chronograf@sha256:2b6d25f033fd7225e5c03109ca97e62c35b535539687231ef11573039008f1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:a81ea833bc10b5d811d4ee54c1b8bfd6827324d25d829b93c5e6877f064aeccf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70427234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425d563cc73d034fe084131ff89bb9bc0d18a7ee91a95d5d531a5e743fb0e7b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:47 GMT
ADD file:1d706af4169332956a23f3faa02754cb503003812cc1d43ad9b2448f7c26f431 in / 
# Fri, 12 Mar 2021 02:22:48 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:37:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 03:38:51 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Fri, 12 Mar 2021 03:39:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Mar 2021 03:39:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Mar 2021 03:39:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Mar 2021 03:39:01 GMT
EXPOSE 8888
# Fri, 12 Mar 2021 03:39:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Mar 2021 03:39:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 12 Mar 2021 03:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 03:39:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a4feded82f54dd43cb68930d190cb6715378fa2aca3ecce0bcac959359f58d2f`  
		Last Modified: Fri, 12 Mar 2021 02:30:28 GMT  
		Size: 22.5 MB (22528907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5784273a6633bf2240f20b7dcdae41732461704080ea64a01135f933f93c0592`  
		Last Modified: Fri, 12 Mar 2021 03:39:37 GMT  
		Size: 6.7 MB (6744499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825c29972746aa6e9e7cca1fe2627d9c736f1695d57c405f37cd3c6bab135f44`  
		Last Modified: Fri, 12 Mar 2021 03:40:42 GMT  
		Size: 41.1 MB (41129444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7e09adb4f2ed2370f597ec7f7242c5d7f744007644efaaf1ce7fbc64227e06`  
		Last Modified: Fri, 12 Mar 2021 03:40:36 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6359e70aaa9a2a16f8d15a4cc115e8cd244075055fe84f3e4e4cf2e4009b100`  
		Last Modified: Fri, 12 Mar 2021 03:40:35 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61b8d22982634f7562a23b27b6d2b8d132688553391c070923b7523f4f14e28`  
		Last Modified: Fri, 12 Mar 2021 03:40:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1d9df68e91ba20b751f4760c5fabaca38c6874de29207dda7f4c00d5ad9c2e26
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63854101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fbcadf2ecd47b50d238dde57fee8d1d24c88122b5207a711bcc5a8a9259a0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:14:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 26 Mar 2021 18:16:24 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Fri, 26 Mar 2021 18:16:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Mar 2021 18:16:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Mar 2021 18:16:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Mar 2021 18:16:54 GMT
EXPOSE 8888
# Fri, 26 Mar 2021 18:16:54 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Mar 2021 18:16:56 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 26 Mar 2021 18:16:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Mar 2021 18:16:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59a68a97e8e2d980ebdbd6cc4e0d02a1d682e732f0408185a01f3fc7abef6c`  
		Last Modified: Fri, 26 Mar 2021 18:17:19 GMT  
		Size: 5.8 MB (5779536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5855622570678275615b72e95d0c0044a8435e176078aa2dfd1342509bb04aa`  
		Last Modified: Fri, 26 Mar 2021 18:18:05 GMT  
		Size: 38.7 MB (38734547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59cbe06e7c5068580455be04762c45c2d78d22aae1fe3ab4f25ef98c248eaf`  
		Last Modified: Fri, 26 Mar 2021 18:17:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7714a91dfe02bb117af1853e0194f773d5a05041f50e95c2d7d68dfce3b115`  
		Last Modified: Fri, 26 Mar 2021 18:17:53 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54799bf673eb5a2c297c3b5b50c0b4596c443073e45f523e7456e9f91611d6e4`  
		Last Modified: Fri, 26 Mar 2021 18:17:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:17898fbbde81e59b3c267641c0cab98f9aefc0afd6b71b55bd004a170ad7421a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966420e366f48a2d43cfd2763f47897bb6e1819773d7c3e85cfa1a51eed05e1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Mar 2021 01:57:19 GMT
ADD file:cd70de3ff9dab2f20378f87a36ca54171a79fde726291a9c5c7eae7b5435cfa2 in / 
# Fri, 12 Mar 2021 01:57:20 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:48:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 02:49:50 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Fri, 12 Mar 2021 02:50:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Mar 2021 02:50:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Mar 2021 02:50:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Mar 2021 02:50:10 GMT
EXPOSE 8888
# Fri, 12 Mar 2021 02:50:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Mar 2021 02:50:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 12 Mar 2021 02:50:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 02:50:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9cb8532b12b699d7151babb99e22315d94bfbf317f3c1db01c532a61fc38a748`  
		Last Modified: Fri, 12 Mar 2021 02:04:16 GMT  
		Size: 20.4 MB (20389391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0ca74c9f3b67abeb6c8251b912c45335d11e252375188570d0ee2db5777cbc`  
		Last Modified: Fri, 12 Mar 2021 02:50:36 GMT  
		Size: 6.0 MB (6028358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864df4124808745adf1a72ee3b43a19d7e9253d4d61489007577c0cce3f3cb8a`  
		Last Modified: Fri, 12 Mar 2021 02:51:09 GMT  
		Size: 38.5 MB (38502492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fb31ac7661675523447543e13180a8c6d4efce5b4d84e298a51a569b40f6f3`  
		Last Modified: Fri, 12 Mar 2021 02:51:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1d2115958092d6287660ecd6041bb41a7beac7a65a9ea82a66694d1e977fd9`  
		Last Modified: Fri, 12 Mar 2021 02:51:00 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d829fedd4d87993ef3ce9f39d13753b284afafb3907e1aab874812bd0522de12`  
		Last Modified: Fri, 12 Mar 2021 02:51:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

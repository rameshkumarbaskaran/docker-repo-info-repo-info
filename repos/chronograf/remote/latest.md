## `chronograf:latest`

```console
$ docker pull chronograf@sha256:29112e4c487dcbb17e7a9b8ae2cb0a15136ef022be89cc1f9cb89b088f0d4508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:8e062780dc9c65f4a405023d3cf867a815a02011966dba1b6e7e7010c55e6321
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70442358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0d78af7cfe7799b524d498bbf79cfe38695a3fe78fdade083c54baa1744a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:57:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 30 Mar 2021 22:58:06 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 30 Mar 2021 22:58:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 30 Mar 2021 22:58:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 30 Mar 2021 22:58:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 30 Mar 2021 22:58:23 GMT
EXPOSE 8888
# Tue, 30 Mar 2021 22:58:23 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Mar 2021 22:58:23 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 30 Mar 2021 22:58:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 22:58:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fb5e63586af7d23e085defc2d66fb6043506fc4207522e583eb8b307cd9d04`  
		Last Modified: Tue, 30 Mar 2021 22:58:59 GMT  
		Size: 6.8 MB (6760089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40855271a33467209bfee7ed24db57e09a01b50b5fe166470d8e011feb03b9d7`  
		Last Modified: Tue, 30 Mar 2021 22:59:51 GMT  
		Size: 41.1 MB (41129609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7143835b82c0e088d61b34fa2b50a904b2369cc726e96fe5e19e2f7b4fdbb7`  
		Last Modified: Tue, 30 Mar 2021 22:59:42 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3f836df3a0dbbd04722b3dfe67d79def8f79a1d5f44d8b6a2ad3692d5c736`  
		Last Modified: Tue, 30 Mar 2021 22:59:42 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c0d6617e569b3176a4a46579ee2f1ade418dd6d5a91fd2a7887a19cd057bc1`  
		Last Modified: Tue, 30 Mar 2021 22:59:42 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f8aa43f5c6262d54ec3a88a9994814ee8e19c553bf47b4d64c0d520e32ce093e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2c0f6a94429ec2396379b78b5defdbfe9fd92ce93cd455897b7c5a8ec82d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:55 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 31 Mar 2021 01:16:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:16:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:16:22 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:16:23 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:16:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:16:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9514ec8c6a361715f3d7bb406fac5a8fe1c1b9a530780910ce458786fcb88d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:33 GMT  
		Size: 38.7 MB (38734503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf0bc57fd7f7bd7904255b04d9f05050164e57f2a03133a3fe53fadc5537f2`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328e23b7fe876fc5619166bf24fc6b870c14eaf2fb8d25b45d99602ad34cd17`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f649a222fb0398e59bb1aeaa750dd8e69f27d20d1fb9766b1294a35cebfc11`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:519f13ae5b625134ff1c0e600fce69033081652806b74a55043978578a3ea1f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6683b6ef31a555d4e1c92d045a9fe99288bfd3d0a4f558d36fe891723b47666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:35:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 00:37:18 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 31 Mar 2021 00:37:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 00:37:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 00:37:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 00:37:42 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 00:37:43 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 00:37:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 00:37:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 00:37:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8fb0292c785020e4d806224fad8e726db9930f08d23b4916773dc04474da75`  
		Last Modified: Wed, 31 Mar 2021 00:38:06 GMT  
		Size: 6.0 MB (6047578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9622c25c19098315bc04704645ecd35a3564e5dfa018eacda6a238933666b0`  
		Last Modified: Wed, 31 Mar 2021 00:38:50 GMT  
		Size: 38.5 MB (38502578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68871724ebaf31349eb1f8344a88dfd08f5816cdfa35350c6cf2f0e47987880e`  
		Last Modified: Wed, 31 Mar 2021 00:38:38 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506175f0ca8e2948278b1718ee099a65dcf182ec9882267ae7d55454bd937747`  
		Last Modified: Wed, 31 Mar 2021 00:38:38 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11574cdb39e484768e017e7960d44b048add049f8adfc4e0cf8c9dd1e28a0141`  
		Last Modified: Wed, 31 Mar 2021 00:38:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

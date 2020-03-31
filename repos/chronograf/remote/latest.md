## `chronograf:latest`

```console
$ docker pull chronograf@sha256:7bb9da646933d7b1cdd1ae7cbca475cfc48a6b505f0758ef2e06bb1dd288bd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:ee58e795c5793875734abe224e715ed99c7bd878e52491c7545614b42dc55bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68562627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8660afa1fb9554fcf37e5e23bb9a6b5374a97f33090eb8d6d932b42b8ece95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:14:07 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 02:14:54 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 02:15:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 02:15:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 02:15:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 02:15:07 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 02:15:08 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 02:15:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 02:15:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 02:15:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81baf4e0f31a6b328af5e7b3caddce5fafac0d7d004f39543cb688781902a627`  
		Last Modified: Tue, 31 Mar 2020 02:15:25 GMT  
		Size: 4.5 MB (4503537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1010cae62da9c3e75893e81a12b3970b643c0072d3d6f27f24c0ee082ab541c1`  
		Last Modified: Tue, 31 Mar 2020 02:15:54 GMT  
		Size: 41.5 MB (41521316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55facb6775467a5147e9474689c702a1d923117e89c0fc627a153dcedfe441e`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97379dd1e5901a33c2f0d1f591614fa0f8e4b4298653f18cdff323ac93ac8`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c4af759bec5886156f18d9b38207b5394f288d74d9a04ac2f6d9919d4a3537`  
		Last Modified: Tue, 31 Mar 2020 02:15:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ad117a1f197468c0840819250d03f930bb1c3854d84ff48aa544a370a15f9676
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec38f145e8fa65c6c79d955c328ac0cfeb02e86cff7362dca54bab3a3b335df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:50 GMT
ADD file:1e233b688c850d7a8a47f185e6f7bb82ad66d729fb1714ecced354cff7be80cd in / 
# Tue, 31 Mar 2020 01:52:52 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:06:54 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 04:08:13 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 04:08:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 04:08:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 04:08:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 04:08:45 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 04:08:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 04:08:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 04:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:08:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4d2af5687ff47f04bedeb1936ed8fe931d68c5684a6959606402065ca5dcb2c5`  
		Last Modified: Tue, 31 Mar 2020 02:00:11 GMT  
		Size: 19.3 MB (19298305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc544f22eca6bbd748d11cde2a73de4d1aa7f7ac1e5b68df6a44bed34a5051a`  
		Last Modified: Tue, 31 Mar 2020 04:09:00 GMT  
		Size: 3.9 MB (3877355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2a7c3383c2a33469689aa027aa64131a2674930704cb307cad11735cced967`  
		Last Modified: Tue, 31 Mar 2020 04:09:41 GMT  
		Size: 38.8 MB (38779385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd7cf7eb323831eeaae66111672ce0e382eaecd0fead4b8611257c1fb919fa9`  
		Last Modified: Tue, 31 Mar 2020 04:09:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f311a03170b54b02f29601201ed656dae625e3844eafbbc6c8d16e36264dd7`  
		Last Modified: Tue, 31 Mar 2020 04:09:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c7f5b079ea69d97c716a357493e2d4c3c86c6c027f1a45648cbc416c3d1083`  
		Last Modified: Tue, 31 Mar 2020 04:09:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5d1c484fcf822ab314d91c4c52a3def95c61e6bc20a1ad0f1666daec564c7aec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a371500b7465b561b628a36ef8df61425674216329e8c1f04c129d78c4b3e1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:41 GMT
ADD file:002dfad10aab7242b4c5779d19cdca9d7fc4c9fc6fdfa8ed7f282c459fab5da4 in / 
# Tue, 31 Mar 2020 02:08:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:57:44 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 31 Mar 2020 04:59:06 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Tue, 31 Mar 2020 04:59:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 31 Mar 2020 04:59:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 31 Mar 2020 04:59:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 31 Mar 2020 04:59:37 GMT
EXPOSE 8888
# Tue, 31 Mar 2020 04:59:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 31 Mar 2020 04:59:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 31 Mar 2020 04:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Mar 2020 04:59:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:43bf72d10816e9fab289a20d17eb586989e2caecbf80328a1c24f031683c350a`  
		Last Modified: Tue, 31 Mar 2020 02:14:33 GMT  
		Size: 20.4 MB (20369961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dee8f78faf2ffeceb5ebb7090b6c8d4c1048b83748d15a7fb58bcabbef9ed2`  
		Last Modified: Tue, 31 Mar 2020 04:59:52 GMT  
		Size: 4.1 MB (4080662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4386e7b582fbdf1bc6a59dc11b734e6aede3c0823124eee55e0c9c279aa58e50`  
		Last Modified: Tue, 31 Mar 2020 05:00:30 GMT  
		Size: 38.7 MB (38688765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6d5118e1a877d04264a2b5a3734b44300fa5d780d74b37b6a74c8402509d41`  
		Last Modified: Tue, 31 Mar 2020 05:00:20 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98d097243a29da5ab01ea987389a1bc3c9875f1239e8727f35005628e95240f`  
		Last Modified: Tue, 31 Mar 2020 05:00:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ef2f4da52c9297a75dfb1d4bc925ed358d872f9ee3588233edca3c5601dfbc`  
		Last Modified: Tue, 31 Mar 2020 05:00:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:91f6b8b507ae9690722ba293b58b135157d9943032b27d59cc85a31e57d8709d
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
$ docker pull chronograf@sha256:bf9a855735ceb7733e1e6bf6c8b2dcde555b59d320b5d46f6ae25fa3e06da5f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61979493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc82010da74c060152e94a4ef5f62decb4792637d7e46faffa40b01a78171320`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:29:13 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:03:11 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:03:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:03:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:03:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:03:40 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:03:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:03:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:03:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:03:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15634d01c3f3a1bece118d96c09deb143bac89f0f8ab71aeb0c0629360a460f`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 3.9 MB (3877306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3240a3a7b219ecf570076b612a7d5aac06fc710fda3f8b166a3cc399d17105`  
		Last Modified: Fri, 28 Feb 2020 01:04:26 GMT  
		Size: 38.8 MB (38779447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ce217f1ce08e8bbd6bcbf1801e7f4fced07b2987011d044993543ebc600124`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c004f6223ca0d5c2200f5b8b1af677da199902d40ed86883385f7d895780ee29`  
		Last Modified: Fri, 28 Feb 2020 01:04:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff433bb8cee205aa10e5c92076debbeb7b21d28a3c03641819aaeb8bcb5ffaea`  
		Last Modified: Fri, 28 Feb 2020 01:04:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:95b6f9a482a886f7f2fe526f89d354352dc4e4c38cf3ba9110cbfb2db2f13673
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63163830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544b844fd5358a434ca76d6395371cf4915db5cd7199e5cadd8f742aa39d0170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:10:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 28 Feb 2020 01:40:17 GMT
ENV CHRONOGRAF_VERSION=1.8.0
# Fri, 28 Feb 2020 01:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 28 Feb 2020 01:40:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 28 Feb 2020 01:40:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 28 Feb 2020 01:40:48 GMT
EXPOSE 8888
# Fri, 28 Feb 2020 01:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 28 Feb 2020 01:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 28 Feb 2020 01:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Feb 2020 01:40:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f797dde9809216bf453cb02c743c00da5fed52ec53e5d746f9a7cfdb99720f`  
		Last Modified: Wed, 26 Feb 2020 04:12:22 GMT  
		Size: 4.1 MB (4080742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48780f7890892dae31b3d1274dfc8aff3c5c34ad58ae0f0bf5e1afbb238741a`  
		Last Modified: Fri, 28 Feb 2020 01:41:39 GMT  
		Size: 38.7 MB (38688710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee94acf4498804a9d5a261e4df1ffe38798a5ff04352873de9764dfc5ffd23`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788706574837e9824494df99fc75fda33d7f4e909002ca901bf7cb56a480e811`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1311dfcdba68ef5487fbe417ac6484b4efb1fb3f285c268700a86549ae4345`  
		Last Modified: Fri, 28 Feb 2020 01:41:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

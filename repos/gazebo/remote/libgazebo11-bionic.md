## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:a1f2359bd3e57bc645755b136484e8e4786fd35a994ce523f70fb57bc6bfd691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:15cfce5c6076e6a060796349f7fe884ce76bb743ec67034ba4c391181ca973a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.9 MB (550927699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beabc89caeee971df446514fb7ab855949f0e93dee7b6df4b4f6ff6a70d261b4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:04:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:27:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:27:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 16 May 2023 01:28:00 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 30 May 2023 20:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 May 2023 20:25:45 GMT
EXPOSE 11345
# Tue, 30 May 2023 20:25:45 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 30 May 2023 20:25:46 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 30 May 2023 20:25:46 GMT
CMD ["gzserver"]
# Tue, 30 May 2023 20:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8112c7660661f5d395aac99b0d2403ccaaf47cfce01b40167688a866847d540`  
		Last Modified: Tue, 16 May 2023 01:17:48 GMT  
		Size: 819.1 KB (819098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af0f112a641a7dded1a88984b00a91588e94005222eeff72c7129e47da5d459`  
		Last Modified: Tue, 16 May 2023 01:31:16 GMT  
		Size: 14.7 MB (14714973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1424c132b637c9b241d1a15e87e4179e7944aeb54faea5226d25e13807383d`  
		Last Modified: Tue, 16 May 2023 01:31:13 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf505bb02aa45e02532816e9c00f3bca0eb1328f7422b250e79387318fc6123f`  
		Last Modified: Tue, 16 May 2023 01:31:14 GMT  
		Size: 5.5 KB (5459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e20e579e18356d2154358d657a6a6ac016b23b9de914acc50fcb0581f9cc91`  
		Last Modified: Tue, 30 May 2023 20:38:37 GMT  
		Size: 235.6 MB (235581469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e60df79a42c420acb4d10591e657f403b473182f528d7442fa4a3a6065b2b1`  
		Last Modified: Tue, 30 May 2023 20:38:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e4b72036e740cc06a24a6a03f62444dac1afcdfd221d808da2dcc3cfb18d68`  
		Last Modified: Tue, 30 May 2023 20:39:18 GMT  
		Size: 273.1 MB (273089563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

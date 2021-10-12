## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:4d9fc01021fb0e31969e99119fd496cdf03ed259d88905819d7eb48710187e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:5e3947dafaece2bec30dcf3f592f401311c6046917cca0f58c76518e5f60d4d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300416973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5ac7916996347de74cc39c400cdc5dc620b549a3587aee8f5306d8289b0af2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:22:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:22:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Oct 2021 04:22:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Oct 2021 04:22:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 04:22:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Oct 2021 04:22:46 GMT
ENV ROS_DISTRO=noetic
# Tue, 12 Oct 2021 04:24:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:24:29 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 12 Oct 2021 04:24:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Oct 2021 04:24:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1879fc7dd1b539861f67f1a1f2560ac72901b2ec692bcd502d7dbd78747aec`  
		Last Modified: Tue, 12 Oct 2021 04:30:11 GMT  
		Size: 10.9 MB (10891815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6513f455c2f9ae29007328538218f9e3fb1ad2f676464032ac997367c06bd20f`  
		Last Modified: Tue, 12 Oct 2021 04:30:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acccdf05e200940e857fda740a50ca8637c81a0035ec822e0bd50a4a0f869adf`  
		Last Modified: Tue, 12 Oct 2021 04:30:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4f3f2e3176a668407560bf65a733da19af24e22a7017e0b28b27cc775aecdc`  
		Last Modified: Tue, 12 Oct 2021 04:30:46 GMT  
		Size: 239.1 MB (239086052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7276317c1b25ab860c01a572280c0f14572628e108816c4971ff0e711979e2`  
		Last Modified: Tue, 12 Oct 2021 04:30:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:99d1fc5a37c0866b5f8cc0b68ae004f80f762c86846ccece5140ba8849c421a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8594ef58160f3763d96577a1dd5bbe2e3e8da1909d605780cf98fa4669ec7dbd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:56 GMT
ADD file:51975e5f400da759b2cd8f7eba13ad61dd4edbbee0d0fac09b697bfa039d1515 in / 
# Tue, 28 Sep 2021 01:40:57 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:17:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:17:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 28 Sep 2021 12:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV ROS_DISTRO=noetic
# Tue, 28 Sep 2021 12:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:19:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 28 Sep 2021 12:19:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 28 Sep 2021 12:19:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:70fe10514d0290bd1e8986c0fd63a67204813d37fc5863cf9bf8bf61b2031537`  
		Last Modified: Tue, 28 Sep 2021 01:48:53 GMT  
		Size: 49.2 MB (49222381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b719e84e5c17a05db4cb91b65b25f4cecd9fda5ca86f7c93b9e8918c83ad07`  
		Last Modified: Tue, 28 Sep 2021 12:26:12 GMT  
		Size: 10.9 MB (10883372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b180205050ab5009747a1fa863a1467a5e672c5116542801e3f3890b57cc64`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0309f751216573b01fdef820a8e7c97a9ef1170563c0136c2e3faa29e4e99ed`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290538ca4b138960141fb0cf9d84a1ada042c2286a8714c2afa426ef9ea5baf9`  
		Last Modified: Tue, 28 Sep 2021 12:26:44 GMT  
		Size: 184.2 MB (184242688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8fe4a6c015780d0a432c652d6ac68724f7b7305a66625f3dde29654973d374`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

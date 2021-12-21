## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:c08bb6f0df3359b21ac31d84bc95415bef45ab9cf2a3b54c8a696210e63d0842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:747edb277b85b1f91527abfc6e8605421d4d3ef3ad182935544515bd86c0bf01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300417508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b77b2e243fd1ddbb99163e0ddc534aae92cce608c45592f437f01dd1121b05b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:36:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:36:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 Dec 2021 17:36:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 02 Dec 2021 17:36:42 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 17:36:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 Dec 2021 17:36:42 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 Dec 2021 17:38:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 17:38:12 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 02 Dec 2021 17:38:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 Dec 2021 17:38:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0d27c0bb5c1a8e650467428d5b560f993c0bad524a2467341f4cacf7271bbf`  
		Last Modified: Thu, 02 Dec 2021 17:44:38 GMT  
		Size: 10.9 MB (10891906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c6185cd0bc5d1c21571501b856e5450c1278d6cd97f3e28dc28761992bef1`  
		Last Modified: Thu, 02 Dec 2021 17:44:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973fda33325f33a869db336e1d0f9a03409932db709b37c54e2732d7405c338b`  
		Last Modified: Thu, 02 Dec 2021 17:44:37 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ac5ff5b2ed72b39d61b4408c6423b2989711475b64022bb5ebbda5a60ff157`  
		Last Modified: Thu, 02 Dec 2021 17:45:15 GMT  
		Size: 239.1 MB (239086073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3acd7fde20a8702e863ddbe045987e72bc6fa11bf0d5524b344d7c0207b140`  
		Last Modified: Thu, 02 Dec 2021 17:44:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:20d0f2c349578d271200aea73e741c8b718409786a372a03b04be558631f9d9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244216048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf549d683df4e6b860fdeccfae209621f923f4a014cfc94191db0657fc7f8be0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:34 GMT
ADD file:73bd5e773b257a6ea5d29845b2b112ebce468878a9467e7c0fe61c69994bb47f in / 
# Tue, 21 Dec 2021 01:42:35 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 09:38:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 09:38:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 21 Dec 2021 09:38:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 21 Dec 2021 09:38:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 09:38:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 21 Dec 2021 09:38:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 21 Dec 2021 09:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 09:39:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 21 Dec 2021 09:39:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 21 Dec 2021 09:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:741eb94195433e00f9799629cc66740c97d607d6f3ed207e5738995897c52959`  
		Last Modified: Tue, 21 Dec 2021 01:49:16 GMT  
		Size: 49.2 MB (49223144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedd2aa81cc2e7379bd59690f90cbd16cf4e588be2a502ac12108e4ba75a9cdb`  
		Last Modified: Tue, 21 Dec 2021 09:47:20 GMT  
		Size: 10.7 MB (10687984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00429e5154d2608cfad408e0de2499d94136b3ed658f2dc5aad48fc80c44537f`  
		Last Modified: Tue, 21 Dec 2021 09:47:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d257c405577ebdaffc9dd7205a3033020e775049c0cc3c0101939fa4bb51bbe`  
		Last Modified: Tue, 21 Dec 2021 09:47:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e4366b7170e598cb5e67f80d349915ed2decdb84edf3cee3f5777cc668a8ae`  
		Last Modified: Tue, 21 Dec 2021 09:47:50 GMT  
		Size: 184.3 MB (184302551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5b3f41b835902abd4dc52846cd889491aca26b96b40a266e9bcb92a168c20a`  
		Last Modified: Tue, 21 Dec 2021 09:47:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

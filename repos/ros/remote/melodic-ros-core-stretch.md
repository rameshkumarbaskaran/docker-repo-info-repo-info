## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:4b65e8141a5293428aa4b12c4f89aaea2c3c8a085c4c2e242d9e05374ff61239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:79e910106c538b187d5ef709c04bb5b12657a4516c56533e8eee288a74a571aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322249549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a0be840e69407906f65d7a46e1f0bd1b28b9cd375e5fac0994962fcc67a0bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:33:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:33:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 19:33:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 19:33:09 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 19:33:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 19:33:09 GMT
ENV ROS_DISTRO=melodic
# Fri, 11 Dec 2020 19:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:34:32 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 19:34:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 19:34:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de16d0f50b4374ec5823bc92988f1c2a778f1488b91506a4c32e9d1113484162`  
		Last Modified: Fri, 11 Dec 2020 19:45:48 GMT  
		Size: 6.9 MB (6867507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e746a7af5ec95aad4a3f31c82da9419cfdb13fcaed8e4208603158759f5cf11c`  
		Last Modified: Fri, 11 Dec 2020 19:45:47 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625f4ae7c99ce503a8e21550bd9b5a979988fb68d7c66fbadb69176e4418cdcf`  
		Last Modified: Fri, 11 Dec 2020 19:45:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3744e199296c0c17c5a8e3df35bd85f751da56707156b925b7b000d5737d718f`  
		Last Modified: Fri, 11 Dec 2020 19:46:40 GMT  
		Size: 270.0 MB (270002618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8741ee1a7786ebcda2770d3ca58252c17705e05df5150d3404d619f284782efa`  
		Last Modified: Fri, 11 Dec 2020 19:45:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6cd4f14f0c417705e32ed856ea37370dd0817569b19b803a9f77a5bea0b1c4f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274704135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105aeecbdf1b023443c116c6400067e173b289d9022343825cd301a6e5fe2fef`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 23:10:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:10:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 11 Dec 2020 23:11:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 11 Dec 2020 23:11:01 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 23:11:02 GMT
ENV LC_ALL=C.UTF-8
# Fri, 11 Dec 2020 23:11:03 GMT
ENV ROS_DISTRO=melodic
# Fri, 11 Dec 2020 23:15:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:15:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 11 Dec 2020 23:15:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 11 Dec 2020 23:15:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb876718fddc5fac92d1cf4a1a2bba55b4f1ef8004b2d667fb9d61f8b9788d3`  
		Last Modified: Fri, 11 Dec 2020 23:37:37 GMT  
		Size: 6.4 MB (6441718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744afed63c33ced1159f376af8d52ad283a1081cdf38f545dcdd1b7b2331b7`  
		Last Modified: Fri, 11 Dec 2020 23:37:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581dd072ca6ecb78ffb662d2eb6c37aac66cef0d6eb4a3598d85675b1f218`  
		Last Modified: Fri, 11 Dec 2020 23:37:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fb0f9af0364eff78bd142ce79a274b31fdcb45ce2fee39fefe0b63bb868f61`  
		Last Modified: Fri, 11 Dec 2020 23:38:39 GMT  
		Size: 225.1 MB (225084656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b874e7e9fc0fdc699fa304738e4c71a8de8852a4e5e09810fd59a1b668de931c`  
		Last Modified: Fri, 11 Dec 2020 23:37:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

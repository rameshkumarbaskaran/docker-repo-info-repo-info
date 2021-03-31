## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:a09f82c16bbe6845818dd88a031a432aa721d1bb13cfd6953fe435fe2972babc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:0137e8aaa9674f842a3ef1936d7f531d8b8e0daee9f418a864bca975af09a3d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322317126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bfd1049c015496d17696faaa2fc77969ac2058f1e717da2115069d8073c789`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:30:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:30:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 14:30:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 14:30:09 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:30:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 14:30:10 GMT
ENV ROS_DISTRO=melodic
# Wed, 31 Mar 2021 14:31:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:31:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 14:31:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 14:31:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f734eb85b47bda51f2595c99d9429f89241d0ea4b5882eac9f352a8ee9591eca`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 6.9 MB (6869232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8cf4e482c701e93c615dcd7c3c840953a9a630b31c402674529810bdbbd56`  
		Last Modified: Wed, 31 Mar 2021 14:44:38 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597486b45058ba2465ebade2fb8a1b02f26df2e25a83f4033bec989244bcde2`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc68b2ecd4ede5ed9bbf9c3574540d2e6cc9c87c642275088cb5e8663ca371ac`  
		Last Modified: Wed, 31 Mar 2021 14:45:25 GMT  
		Size: 270.1 MB (270066130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a94b685ae3e48152c7e4ea1b92c8375d2e7a912c33595e1c9ccbb64d61289a`  
		Last Modified: Wed, 31 Mar 2021 14:44:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39f2688b7350d8777ce939b4a088a9b633a467ad0701be096124a410e2f54840
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6130c2445162eb8e7e3f096081bcd1d3d35eab47497f4b66dd9d5ce112980`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 13:38:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:38:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 31 Mar 2021 13:38:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 31 Mar 2021 13:38:12 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 13:38:13 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 Mar 2021 13:38:14 GMT
ENV ROS_DISTRO=melodic
# Wed, 31 Mar 2021 13:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 13:41:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 31 Mar 2021 13:41:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 Mar 2021 13:41:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9bcb4567c53b5710817f63af7d0c14a3dad36b823f3cc9f142434d89dd7cea`  
		Last Modified: Wed, 31 Mar 2021 14:03:12 GMT  
		Size: 6.4 MB (6442935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84574c97c15ff3c495faceaf91ec7efac2d7735c4fe357cc256339c4fe93410a`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefd0949cc578f2b84114a09843d05b951725916a271d79c9e803a14021734f8`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fafb8ecac1b3a711771dfd44718d41e04b5dcf0e3545af1cc8fc71a84905bb3`  
		Last Modified: Wed, 31 Mar 2021 14:05:04 GMT  
		Size: 225.1 MB (225114741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e8c7efe0eb7db52b3a500557e94b2126eb204eaf0deb2cb3356cdd72b378f2`  
		Last Modified: Wed, 31 Mar 2021 14:03:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

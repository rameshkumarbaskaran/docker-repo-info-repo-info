## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:1191be618d2eff7b4e4a1de58ac70704cb9536716a1216f1307deb42fbee845e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:80788ee239491eeb65f5a4a2624d9970181658a205b66837aa86dac6672270e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322320701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed13e1a87f554706f5d42256847d5fbea833cd9d5ab23dcce0a0765fdc12b324`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:17 GMT
ADD file:f7a6b2066de76eb559d8ab8bf8972d519c3b4dcafc62e46253227559091f7c8f in / 
# Fri, 26 Mar 2021 15:23:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:12:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:12:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 09:12:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 09:12:24 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:12:25 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 09:12:25 GMT
ENV ROS_DISTRO=melodic
# Sat, 27 Mar 2021 09:14:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:14:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 09:14:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 09:14:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1dfe7e1e1bffb84b5330514880896199259b01ebe2b9d531dd88f7ce7db8cd18`  
		Last Modified: Fri, 26 Mar 2021 15:32:18 GMT  
		Size: 45.4 MB (45379513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657504ffb8f628d70a2b1e2672e16b95f6eac895057e4cdcb97e09f862a1b09`  
		Last Modified: Sat, 27 Mar 2021 09:26:42 GMT  
		Size: 6.9 MB (6869187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa6cca370d6196ae385348a9369c89f41ffa9578e97dddffed55be61d6e0e62`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8404a516aba8bbb9ba24fdc7ef19705ce8dd84915cf4cd2986249f95c22db251`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb5474c655269c720249df5c38af05416a1d5e3d33019bffbcd827297ddd6c6`  
		Last Modified: Sat, 27 Mar 2021 09:27:27 GMT  
		Size: 270.1 MB (270070182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab44e97519ff7d9f42f3b133c7e261108a040df6ade9b5001b98fe56d831b1c2`  
		Last Modified: Sat, 27 Mar 2021 09:26:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:133fe22a2992a6bebf9606d0b80bf90c714bc4010470ee5b8e59279010986549
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274733819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bd276320fc2e6d33c485e2d20420f341630ec035fa37fa48ac2822cd1ff11e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:44:15 GMT
ADD file:cf753fedc426819aa5f93f4ad934479efd8fbf024b408627239b77ddc5223108 in / 
# Fri, 26 Mar 2021 15:44:18 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 08:33:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:33:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 27 Mar 2021 08:34:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 27 Mar 2021 08:34:02 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 08:34:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 27 Mar 2021 08:34:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 27 Mar 2021 08:36:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 08:37:04 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 27 Mar 2021 08:37:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 27 Mar 2021 08:37:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1a0736e738921f2c70c8ce48d5ba8b042279c41c41f32a1af43a6cbd299f6d89`  
		Last Modified: Fri, 26 Mar 2021 15:50:55 GMT  
		Size: 43.2 MB (43176405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab771badbb8aa014048919f3589fd266ea69c3369386e5871c978f23a8300b4`  
		Last Modified: Sat, 27 Mar 2021 08:56:28 GMT  
		Size: 6.4 MB (6442899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b2222f36c8d1ffd59561065b458542540fa5d056c07a7c5ff43d4e1084af6`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120925e04f1f36d906c84242cdd9f6d9ae18d015db752ff53635239f1870b35`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bfea5dbd258a9531ab03eb35139fb5c33ecb25b5a5882f3f243ca5994e9f5e`  
		Last Modified: Sat, 27 Mar 2021 08:57:39 GMT  
		Size: 225.1 MB (225112695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32714704b7f44517608be7e9533727964a04ec6dc8e9c8047053bdf8dc92c9f`  
		Last Modified: Sat, 27 Mar 2021 08:56:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

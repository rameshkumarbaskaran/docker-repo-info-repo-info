## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:ff83de7776e1d39ad2bd7c38aee5eebcd2f1ad6645da78e208a1816ac89faf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4823a905ffe0b3e7d527d857d533d78fc707ace416fed369a38da35f98b535bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291990746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b750019b37ee79ded291459fd57709578c21c1a3c552e25109bf1f41e0d8dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:11cbb2f864a289726b9510d1a9b4e6e7414dfacb9a9d782b9d1e4754293f2056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266239154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83c28f326a67014793ddf881b3e99269c547c3a86ced293cec9f9fca7d46c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f76867405b52c64167fb70e1f09efb2123122401686455531be3b1a7ac3221e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b4b42a718b3881e44324b053aea4b4105bf5b40004428e1ca8c85a6a6ec75e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

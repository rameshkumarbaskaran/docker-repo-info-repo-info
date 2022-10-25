## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:ecf84b223a21ae4bc5dbeb24ff850fc8963031e00bd67121cdaf99b4f898c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
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
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
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
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4868ca46db01ab9b479444064b3f4b3919442f2de6fb4f78794359e36ffeb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411711887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d006ec586d2e78a0b3c081f1811cfe9cf6ebc2d6e2cec7e0cbbec0e1012473a`
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
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

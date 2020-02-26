## `debian:stretch-backports`

```console
$ docker pull debian@sha256:563f61688d060b59298b5a0a6ab9761303f0dc0cf243b8fe4ca3cefd97e60357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:15c2b54b4fa3b19dd184bbb220b3e0ef1369e3521fe1aa49d26de228e11b96ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87de0628ef1639621499bc87da3d47e5b7bd0eda173dd0679a4e4fbb4cf7b506`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7cedbc3eb9dd53b11e81dcadb25e875af66049f447346c05f0e717d911ed0c`  
		Last Modified: Wed, 26 Feb 2020 00:47:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fceeea5fce99c8297aa030784765851319bad6b1e7f41dbd214ce4cb519f6acd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44066839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7638faafbb48c39529ea23493576c645ddba7dc44a8655858c2aa420db0cf67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:53:01 GMT
ADD file:5ed8e2bc0bf117a359d81b052913e99f6139d0b36e5798d75392429effd5afd3 in / 
# Wed, 26 Feb 2020 00:53:06 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:53:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3294d23573097fea5f2d79377bc86444ebf83e4bed50a8a6c62b7aa8637dd7fe`  
		Last Modified: Wed, 26 Feb 2020 01:03:12 GMT  
		Size: 44.1 MB (44066613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cca00ce78127a3dc9b8e26a7fa98adaf3ab63b00503bd4a1d89d715fd273d61`  
		Last Modified: Wed, 26 Feb 2020 01:03:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:708fdcd34da93c7433e71dddf5c6168c1435c69d4d81477a72b54444b4afe4bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b520efd4094884c0862acb4e8f850b2fc60fd49d677b73174bb257f65faae64`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:00:42 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fed0af0c3dc0b21d91a4d629931dec5f7b1bdfdd13cab3848be5bdb129535e`  
		Last Modified: Wed, 26 Feb 2020 01:11:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e4f6871d7f161e419b3705182b01a5385a1c751d501e09ef368923a0bce213d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43158371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b675704dd97b7b139a0adb1bd0823f9d16da1231e5e3c172fe974266c374f0df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:50:31 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38213310bd71cbebffc93447449575c7a4f86bd2805555f7cadc402463451f`  
		Last Modified: Wed, 26 Feb 2020 00:58:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:4ebc621e70477584f79c0f2895431223a02adb7ec3c0be93849f6230788ed64a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060b179a6429e0880db87dd5e313d4fd8debb7daa0fdba2e3c42c663d83250b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:35:22 GMT
ADD file:f57292acaae4c3d7e8b3217b28f9efb27faef1c4e08ca95f4a25d1302355fb51 in / 
# Wed, 26 Feb 2020 00:35:23 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:35:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef83ea0a858b11598fe63ce7d80a401ebb47c746763b35564bd712f013cb961f`  
		Last Modified: Wed, 26 Feb 2020 00:41:45 GMT  
		Size: 46.1 MB (46095035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa90ad6a4a14d0b814ce16a1cda53117db3e063345542a81e132e5ea04d7bf`  
		Last Modified: Wed, 26 Feb 2020 00:41:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:609f458a9ad868725a1f29319d507121239457f1fa1e04f0e77e5e97a1b5fbbd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207daa9be4c6c28f444fbee2332d0297019f59ab57324e5eacf90157bc067990`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:36:21 GMT
ADD file:734d2a25bec5d510e72f822b21a5ef5786a928c6cb933209a04c6358fd600b67 in / 
# Wed, 26 Feb 2020 01:36:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:36:55 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3a8babb46b416d2208716bc29bc3e805dd074b943418fc44ac89d66e363bc68a`  
		Last Modified: Wed, 26 Feb 2020 02:03:30 GMT  
		Size: 45.6 MB (45647081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ea22d55f48ea3a7270f53378db3e4b4211ecfd744400e9f64de0ef1f1cafe8`  
		Last Modified: Wed, 26 Feb 2020 02:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; s390x

```console
$ docker pull debian@sha256:496c15e11c1853c9676a71db41bbe5473b3efa1641b5064dd70de0a78dcd739c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5ca63c2c8f37bf9d012c03e0f881320d98b8304e10334ba96f85fcdb6c2a13`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:44:30 GMT
ADD file:bb76ab55808bcd0567a32c3d7328d5c1719147f0f723a4aa574872eb8f12b4d4 in / 
# Wed, 26 Feb 2020 00:44:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:44:44 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2baf8ed1bce68a4f36469f3537f12b9e5bebc860ab4aac0954714901595c575`  
		Last Modified: Wed, 26 Feb 2020 00:49:08 GMT  
		Size: 45.2 MB (45232848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94c2509c5e6f3bce7cbd2434e53c2472649e6cabb70b0b5727191da172cdcd5`  
		Last Modified: Wed, 26 Feb 2020 00:49:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

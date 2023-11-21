## `debian:experimental-20231120`

```console
$ docker pull debian@sha256:b5f8b8d567490d87a104e7d99a938e4718b62840aee858dbd018c3de147eed96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v7
	-	linux; riscv64

### `debian:experimental-20231120` - linux; arm variant v7

```console
$ docker pull debian@sha256:6cc2df07be03c77387ffc0c3326c5638fbbd9c0d4c49e8543619c29867a3a428
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b48e13819400565bd72d93bc3069ac76c065dc3f0f0605b02a6348f5aa1cfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:00:15 GMT
ADD file:8e091f00e04d8cb85cfce52bbabcbac6c260e95c3f3a00752186e465f583b2ca in / 
# Tue, 21 Nov 2023 04:00:15 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:00:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc7b160f4eb0bdcb6d980297d91f215375ca0669f74456162ed2c3a6534ceddc`  
		Last Modified: Tue, 21 Nov 2023 04:07:09 GMT  
		Size: 44.8 MB (44844006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69e60ef4d54cab41871e2cb5a7bec428aea9ce83d55e58fff0dee9198f58e0`  
		Last Modified: Tue, 21 Nov 2023 04:07:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20231120` - linux; riscv64

```console
$ docker pull debian@sha256:1e72d63906b9a8c4d0a64ed1e98c02cf05a02268f3e6fe285b8ca0a325aab6dd
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48206923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013871bd9721543bf4ec97e375d9c2223b75834ecf613fa142e2035ea46d9b5b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:10:08 GMT
ADD file:f926dc89ba0815e0a23356d88037340957f7a57bea917a3aaed678d1decf7b22 in / 
# Tue, 21 Nov 2023 04:10:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:10:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b1fcc4091b722aae5f7f102ced62233745368e2095d318f03282cc819757f97e`  
		Last Modified: Tue, 21 Nov 2023 04:13:22 GMT  
		Size: 48.2 MB (48206699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60afd7f2b0f8844688b4d838bb33218c480848fcdfac7245abf07bd96e9286dc`  
		Last Modified: Tue, 21 Nov 2023 04:14:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

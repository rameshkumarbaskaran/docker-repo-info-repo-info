## `nats:2-scratch`

```console
$ docker pull nats@sha256:9ca8ac020e042cf31f48e19cc98dedc2f892e52a4da8b9f6db890c79a351adb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

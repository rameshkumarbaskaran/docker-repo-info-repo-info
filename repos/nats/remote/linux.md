## `nats:linux`

```console
$ docker pull nats@sha256:b26e71094f7c4af203bdc62cd789f1ad78003d15c2889a02dafe21ef7cd8c035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:3a8a6aef1c6ce50c39e39217b6f875b05c3178691f316afa5f59808ea14895f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c46e01e700b1b387a5bf88e132f5b11783beb574bfd08735973bb11df19c4050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21a6870eda6c2fb32528c3a2f8452a76bff4e3fd6b8cd2d42d221f3a1fbabe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:33e8ae8356ddcadb38d560639338ac18914ec4d4350e96e99962889972148369 in /nats-server 
# Thu, 30 Jan 2020 23:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:32:16 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:32:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:32:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:20480cdc8f337bf9709559a4a23444a5b55d9bed4d9d62eadee822161266f792`  
		Last Modified: Thu, 30 Jan 2020 23:32:40 GMT  
		Size: 4.1 MB (4050811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a61e327371ca0338cc310b0c67f49a551dd5b8bbf30ed8c75b95219651ea76`  
		Last Modified: Thu, 30 Jan 2020 23:32:39 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:eff9f3146f76a2f78e896166707efdecae7f4aa7510d78cb4e986a578119bfb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158c883c70044a613a0b0a5bb6096487ac305e3f6f1b3e57a17a9f98bdaf09e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 31 Mar 2020 20:53:55 GMT
COPY file:5131c35b89e2bccdb55c8f10be46601f1fb947279308495595024bc0e2b29d5b in /nats-server 
# Tue, 31 Mar 2020 20:53:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 31 Mar 2020 20:53:57 GMT
EXPOSE 4222 6222 8222
# Tue, 31 Mar 2020 20:53:58 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 31 Mar 2020 20:53:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705a3cd49f0567c17013b0eddbe53e6cffedd428744250d7076a8396babbe655`  
		Last Modified: Tue, 31 Mar 2020 20:54:42 GMT  
		Size: 3.8 MB (3781482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efabc067a958db0c40714b9365000273b61d5d19c9ce96c291b023d4ef2933f2`  
		Last Modified: Tue, 31 Mar 2020 20:54:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bc92c930ca118ded5ae0e2b9533652749e38e89f3bffbac76058a001089b517f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd8684c49b5d6378049dee42c6899b45d8019b3ea871d4f740f241c7a10925`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:9e97a3b115930612d1040549acec7cfb336216b2d21169e4498e09ad8aa8bcde in /nats-server 
# Thu, 30 Jan 2020 23:41:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 30 Jan 2020 23:41:46 GMT
EXPOSE 4222 6222 8222
# Thu, 30 Jan 2020 23:41:47 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 30 Jan 2020 23:41:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2cb7bb651603a7a32e930db2be5667560b6eb1998a1476e7c5a3fcebb3ffba0`  
		Last Modified: Thu, 30 Jan 2020 23:42:34 GMT  
		Size: 3.8 MB (3759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985b0c547ebabbc3f700e9190c02413076ccb9c40e56e0273005a454e22718`  
		Last Modified: Thu, 30 Jan 2020 23:42:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

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

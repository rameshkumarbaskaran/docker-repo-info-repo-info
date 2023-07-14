## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

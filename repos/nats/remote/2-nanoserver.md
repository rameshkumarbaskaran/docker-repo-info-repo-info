## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:932b08c0337317adcd663aa38e0a55a9803ee6cbcd53f7cf36001daaef8c3b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats@sha256:f0bdc15be988edf64cf892a77450834881d2c6c7dc82b9360bc52593a5aa0b14
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111696158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054fa16934ca677fce3a8b34c00ace05149796083e264482875fbda0d23f6539`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 16:47:45 GMT
RUN cmd /S /C #(nop) COPY file:27c13fdcb069e821fef4075dc66fcddee176451571e6aa7486ebfdb5261b3db9 in C:\nats-server.exe 
# Wed, 09 Nov 2022 16:47:46 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Nov 2022 16:47:47 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Nov 2022 16:47:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Nov 2022 16:47:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c0e5b167a89f47defc32fac57f29e7c72ef828ad873eacf2127253ca009e02`  
		Last Modified: Wed, 09 Nov 2022 16:48:41 GMT  
		Size: 5.0 MB (4966166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1ef6dd873b0efdf79c9de73a56c7d7cca2722957a6281b7f6e4aaa950572da`  
		Last Modified: Wed, 09 Nov 2022 16:48:40 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842bada13c0156df30e6332066f30698a9f967235704e763789afe20fc24af89`  
		Last Modified: Wed, 09 Nov 2022 16:48:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e63e1c547824ed6c1142b32ecab108bbf2784a0659016df96eb2f6b0f140e0`  
		Last Modified: Wed, 09 Nov 2022 16:48:40 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ba3f3f63b4b7c99e24b6221604b2f59a22f2f3ce9109e5998c44ef5e7ab8ce`  
		Last Modified: Wed, 09 Nov 2022 16:48:40 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

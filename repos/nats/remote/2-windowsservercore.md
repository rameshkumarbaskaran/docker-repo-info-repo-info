## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:07432a398099039390dadc22e657dfbc8ada5a6475071cdf3a0e7ae97cc5f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:4c410fa02ac3030e41f939d40f93ef6f4b8fa5ef0018742f84ded81ff3dd56f4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509506739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310f6ed1347d5414cbccdf037d24ac72f6a164094e11c88c95c36add4ca70e7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:39:54 GMT
ENV NATS_SERVER=2.8.2
# Wed, 11 May 2022 14:39:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.2/nats-server-v2.8.2-windows-amd64.zip
# Wed, 11 May 2022 14:39:56 GMT
ENV NATS_SERVER_SHASUM=300b9743afa50e02e4e8d43dc212bfde8a871617bd524829114e19ff680dde11
# Wed, 11 May 2022 14:40:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 14:41:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 14:41:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:41:58 GMT
EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:41:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705248b3431d43594f02c1a498c5825693a2219dc3e9916401f0c6483917d9a`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb084aa44aefde2d0aa2b439015601202b9289be01b36d72c372e12b207c0e3`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c26ed0b144ad0936998810c48866b8542c5459336cfbc516abbd8e36f335dc`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be12ae5206975ef6a801832e7cb1e13cce3a20a913b8af575d2eb06033f814b`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 482.2 KB (482237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934d847ec8d58fee43acc3f6b9da54c22bbaa3af2fdc22fc6cc7b544df9ed0d`  
		Last Modified: Wed, 11 May 2022 14:42:41 GMT  
		Size: 5.0 MB (4955482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b1d767c6565af1eb4447e5b0ce9d14889a68e438a8f16385c402174fe0d560`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7197706e722c8737fffdee9b04e1f3d7e8e6bc8824673d7f30221ee05c25681`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc51eeff832289639769559e0535687ae4a579b49d847a4fb7236824a8805`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925945a5e74fac0f93b1337cf5af3f61b3b33e549af73c3b2ff6effa8cbe27e4`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

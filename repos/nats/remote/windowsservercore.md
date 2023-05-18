## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

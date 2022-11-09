## `nats:windowsservercore`

```console
$ docker pull nats@sha256:3389f85e0e7409ff650a13c55949b8479f26722851ed67d7d729b916da30fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats@sha256:e41754ef90643bf069cb84ea5f668b90d6e87d5dc893892365da862bcb8e6b28
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2784261872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6657882ae13b4d8042bf2e2496662461c4bb3edfa1b13dd86573644fae02bdbc`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 16:44:46 GMT
ENV NATS_SERVER=2.9.6
# Wed, 09 Nov 2022 16:44:46 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.6/nats-server-v2.9.6-windows-amd64.zip
# Wed, 09 Nov 2022 16:44:47 GMT
ENV NATS_SERVER_SHASUM=1c627ca06ec40fafd26befac35640a6fefc63bbb16cbb594f74d493ba670f2c6
# Wed, 09 Nov 2022 16:45:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 16:47:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 16:47:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Nov 2022 16:47:27 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Nov 2022 16:47:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Nov 2022 16:47:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23322c383be4156ea3e0f20a481efd18b9c3bc4985eb67c6f77d626d92e87bd5`  
		Last Modified: Wed, 09 Nov 2022 16:48:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9284e4cc7c4758292b1e78f2080cd5df93d0d78a2bebe4c09346556272cf88e`  
		Last Modified: Wed, 09 Nov 2022 16:48:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e578f0b75bab1273f0521ef89bb563f4b3f525708b3ed846b038128137ca2487`  
		Last Modified: Wed, 09 Nov 2022 16:48:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd0fa9993c097d11161a0eabac8e8e9ab7e0b7de142c1b50d2eda742ce7bf94`  
		Last Modified: Wed, 09 Nov 2022 16:48:21 GMT  
		Size: 358.6 KB (358602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecb0068e158479db8e23a4f17e3d634187e5565fefc58fbd239fc79783be5a3`  
		Last Modified: Wed, 09 Nov 2022 16:48:21 GMT  
		Size: 5.3 MB (5303625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b232f78a915c29589007d3cb21b64cd7a5105eab2cf012f3f5611287941569`  
		Last Modified: Wed, 09 Nov 2022 16:48:18 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5076e2a144a8448de3e2a434deeb71894af3f8f4fd439afd197788d7c990cda0`  
		Last Modified: Wed, 09 Nov 2022 16:48:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed22c3b339e85309fe22a7e2079347d9ea486185119e911edbe6b1f6c4f60ac`  
		Last Modified: Wed, 09 Nov 2022 16:48:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e163e46114b71691249b4d7125d6c2b2b41a5a48b185b28471f915ed2389226`  
		Last Modified: Wed, 09 Nov 2022 16:48:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

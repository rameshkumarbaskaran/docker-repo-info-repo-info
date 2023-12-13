## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a68c4edf923877deffd913e29bb7909ba26c39be31c4707dc820572932b9b191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull nats@sha256:30b20285018fbc9e0b748049ec2e2a6b817807067f7a81962c337d77b259e84d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066074693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42eb52589be054d0eaa4c2ceac86e9b2946f89598ebb9f31631538a4fdae057`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Wed, 13 Dec 2023 00:58:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Dec 2023 01:56:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Dec 2023 01:56:24 GMT
ENV NATS_SERVER=2.10.7
# Wed, 13 Dec 2023 01:56:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.7/nats-server-v2.10.7-windows-amd64.zip
# Wed, 13 Dec 2023 01:56:28 GMT
ENV NATS_SERVER_SHASUM=92c4883cdf608c1e096feabcc9a0f46935ba34fce72210520ba2e66207968630
# Wed, 13 Dec 2023 01:57:50 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Dec 2023 01:59:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Dec 2023 01:59:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Dec 2023 01:59:48 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Dec 2023 01:59:49 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Dec 2023 01:59:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c910cb69fed2b0fb25386cc07fc30cdf9f1d5bbff8a0aec9f12bc1481a910225`  
		Last Modified: Wed, 13 Dec 2023 01:31:59 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf33e2bf1acb3cf4c5378da463e37c48cc36ddca44d3a9b068d9502a8701d83`  
		Last Modified: Wed, 13 Dec 2023 02:04:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a4af05f79b6336aea42e71c3d120a54b8bc9fa7ef953caac84a72a46e3671`  
		Last Modified: Wed, 13 Dec 2023 02:04:36 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a01df933f074179c34d4c90db7c6833f7ebcf9f129873ef554e24286902e17`  
		Last Modified: Wed, 13 Dec 2023 02:04:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc28f9aa54b7b757e41ae45b253ef9fb6016641d653dc23876a24dff012db91`  
		Last Modified: Wed, 13 Dec 2023 02:04:36 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b8818a7886ed7d246c2ace85c760a9e6f04206f6d03c691cfd5df551f0293`  
		Last Modified: Wed, 13 Dec 2023 02:04:36 GMT  
		Size: 456.7 KB (456671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98ae4c6a2ecae6d062cc17692bc50220344ed1cca17f18ac8d771468d7a2765`  
		Last Modified: Wed, 13 Dec 2023 02:04:35 GMT  
		Size: 5.9 MB (5896141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b8ffef143a544891e73fd900067f5da34f3843507257fe33ab76c2839aaf6d`  
		Last Modified: Wed, 13 Dec 2023 02:04:34 GMT  
		Size: 2.0 KB (2009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3874a4142dd5fd0edcf6c6ca51465f8dc72fd583f1c1b64490ae385d17d90c`  
		Last Modified: Wed, 13 Dec 2023 02:04:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ddf87c6bc9a1b959870a252a33a90d41662418c80501d45077011a96d0f280`  
		Last Modified: Wed, 13 Dec 2023 02:04:33 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed477fd924c092311b7c290b0cabe536a52f8d15af7ad2a16a0d727ae8c7e11`  
		Last Modified: Wed, 13 Dec 2023 02:04:34 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

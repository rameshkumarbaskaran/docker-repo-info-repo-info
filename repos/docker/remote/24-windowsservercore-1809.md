## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:fd92678711a9d1e683094f01590666b00cb5b93903ffa3ba8e5fe9bddf7f541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:3370cd5b6761025b8b71edc34589df5b289ac4bbc474afd711ddbbb33dac010f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2123343212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099ad7b44f574188f5b8267662787991787f596f64aadd86ea9f99a0b8cf1cea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 03:16:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 20 May 2023 01:16:46 GMT
ENV DOCKER_VERSION=24.0.1
# Sat, 20 May 2023 01:16:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.1.zip
# Sat, 20 May 2023 01:18:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 20 May 2023 01:18:07 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Sat, 20 May 2023 01:18:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Sat, 20 May 2023 01:18:09 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Sat, 20 May 2023 01:19:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 20 May 2023 01:19:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Sat, 20 May 2023 01:19:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-windows-x86_64.exe
# Sat, 20 May 2023 01:19:29 GMT
ENV DOCKER_COMPOSE_SHA256=6083a9057010a6a048d83c94318d254657abee48600baca2402fbe887d0b7ec4
# Sat, 20 May 2023 01:20:45 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5869a0b27170ed378e5d22763ab388eaf4a9dbd91cb7eaee4cef7d8639a2ff74`  
		Last Modified: Wed, 10 May 2023 07:11:47 GMT  
		Size: 451.5 KB (451506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611bc5b3f6eb35800b14c663f2bfcabfecead6ab4a7216fdcdd4081fb9354f5`  
		Last Modified: Sat, 20 May 2023 02:15:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413fb41d65eaa6e11c31655a25a3dafe7a78a2dcfd9b3b9fb712a200e3cce35`  
		Last Modified: Sat, 20 May 2023 02:15:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514407c6475908d93aa56dbf8187ffeeb77b8f66de5e83d217200d7a095dfd9a`  
		Last Modified: Sat, 20 May 2023 02:15:58 GMT  
		Size: 17.5 MB (17474830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73ba492e399ffe1ce5bea0401795b2bed2d5131fca1942191f8e808ecb0f04e`  
		Last Modified: Sat, 20 May 2023 02:15:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5c1ee338be9f263bf4ea49aa15feedf13af60ffcc78f20c7bc9a58752e7a9a`  
		Last Modified: Sat, 20 May 2023 02:15:54 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73390c131a479ae77291ea946ee1d9b483699d25059cd1f5e07b5b17bdaf7c9`  
		Last Modified: Sat, 20 May 2023 02:15:54 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775663eb1a543299b4e0073ba4b5459bc34e0e6ddd50381576bbb3e82bb23657`  
		Last Modified: Sat, 20 May 2023 02:15:56 GMT  
		Size: 16.5 MB (16490659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30c587a82795401bc09c3eeeca6f3c540621001299e786b512d9d90ab1869fc`  
		Last Modified: Sat, 20 May 2023 02:15:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1c9175d1997a8da73701287342d366a424a26bfcb89b8848fe394dd08dce66`  
		Last Modified: Sat, 20 May 2023 02:15:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc2dc5a2ecbf6f271d30b3f1af21ef38de7cff9bcb992ec8d5c3ed01cb1e641`  
		Last Modified: Sat, 20 May 2023 02:15:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f172abe3b9ba8904cba3d5f0d4eb3f4986ed1c38c67865976b8e91c3e1349ce8`  
		Last Modified: Sat, 20 May 2023 02:15:56 GMT  
		Size: 16.9 MB (16878280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

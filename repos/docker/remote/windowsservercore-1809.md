## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e84f671e17b7a624b2fe9857ce730d961a9746a3312bb0b29b963fd7c1104f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull docker@sha256:f75763c02bfd57528d7f924d779e24e6185ba787ce630fc22b39e936aa91a34e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1704850908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f774bf3cac154e13a3e7fdda3d391274075199b35f1410c2691ec20f72a36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 00:40:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:35:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 Jul 2023 20:16:52 GMT
ENV DOCKER_VERSION=24.0.3
# Thu, 06 Jul 2023 20:16:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.3.zip
# Thu, 06 Jul 2023 20:17:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_VERSION=0.11.1
# Thu, 06 Jul 2023 20:17:28 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.1/buildx-v0.11.1.windows-amd64.exe
# Thu, 06 Jul 2023 20:17:29 GMT
ENV DOCKER_BUILDX_SHA256=ed04052b2742e0a2e45a02c87ec4f782b8c7914f56a5d3e1bb39ff9ab8687f30
# Thu, 06 Jul 2023 20:17:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 06 Jul 2023 20:17:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.19.1
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.19.1/docker-compose-windows-x86_64.exe
# Thu, 06 Jul 2023 20:17:58 GMT
ENV DOCKER_COMPOSE_SHA256=e77e4764e939782d27570fc17a6029b63fe922ebce6800128dfe1c047a9395ed
# Thu, 06 Jul 2023 20:18:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58717a727cd3a756d7c1180dfb74e95d49735ed12628bd25d2058bc90fa96991`  
		Last Modified: Sat, 24 Jun 2023 01:20:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb210483c7a5877c9d4e754a46a0085ff94bc31d9e32e64c37e1ed4d6e30162e`  
		Last Modified: Sat, 24 Jun 2023 03:41:56 GMT  
		Size: 306.0 KB (305975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220d673a500d122873877d4a4be342cb40e07ee47a4a508dee2dcba97bfe4723`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70790617356246e318492973e7c751cc8fb9199ed00349374fb264e4566ced04`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1f34dbac2b79a6a652b8926077c0e41dda895cab9b1ac5c75c29db1cde7a6`  
		Last Modified: Thu, 06 Jul 2023 20:21:45 GMT  
		Size: 17.5 MB (17466854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25abab3ba7887100f6f8a30c3316f9a3dc51b171a81f1703159c27c07c25dd82`  
		Last Modified: Thu, 06 Jul 2023 20:21:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b56866387a48d55494e41e21da221a0a5fe4b3239dc940b5b75984e14f9cc5`  
		Last Modified: Thu, 06 Jul 2023 20:21:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4cc15bb518b5c263f5d52c7b7761bb36681b7fab382fd34aa9a21042d5055`  
		Last Modified: Thu, 06 Jul 2023 20:21:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00adc5a657ac1846710c85cc2992c68dcc4389c3d24d4f5be85599e64aac8e4`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 17.9 MB (17882284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfe7cd1c7b16458db2fa8613b9b5e2161397d26647a6b16d618bc92922d9868`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb59442896100faf18d8b1d475701d8a7bab03de0ddcd6606a00cffda2665e7a`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a533ef75401c06ad9ab423047654f037ae36177f6bccfbef4bdeb5f98e9c149`  
		Last Modified: Thu, 06 Jul 2023 20:21:38 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9329ff40635fac09f33414e395d71d781533d78016ebfc61b706c13da4e1e6`  
		Last Modified: Thu, 06 Jul 2023 20:21:42 GMT  
		Size: 18.4 MB (18447195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

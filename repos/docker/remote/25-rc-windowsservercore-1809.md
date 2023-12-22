## `docker:25-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:b9a5502bfd90f1c83e1cceb8ac0e43de6706456b69d5b9cf5f6f573f0bc94cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `docker:25-rc-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull docker@sha256:c69689ec3805838e8779e7927e1a5c58706d2c233022b136b009c348a28f1585
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2115012952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119a6b25657fd78b3f26e5bd53a02590c3854598cfbce3f0f8f25e21a7af083c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Thu, 21 Dec 2023 21:54:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 Dec 2023 21:56:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 Dec 2023 21:56:15 GMT
ENV DOCKER_VERSION=25.0.0-beta.3
# Thu, 21 Dec 2023 21:56:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-beta.3.zip
# Thu, 21 Dec 2023 21:56:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 Dec 2023 21:56:48 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 21 Dec 2023 21:56:49 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Thu, 21 Dec 2023 21:56:50 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Thu, 21 Dec 2023 21:57:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 Dec 2023 21:57:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 21 Dec 2023 21:57:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Thu, 21 Dec 2023 21:57:22 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Thu, 21 Dec 2023 21:57:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
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
	-	`sha256:5471d41e065db5862ed321d7b151886aec15e440743542d2ab13bdd81351a35a`  
		Last Modified: Thu, 21 Dec 2023 21:57:58 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dddc7dc9c8bb940787c51c6ecc5881b4f776da8637de7640a863ef65a6fc1`  
		Last Modified: Thu, 21 Dec 2023 21:57:58 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120ff209d6d7218f5c051a4a761fa25b2d509f52d0a48719b4ec6bb40ad605b8`  
		Last Modified: Thu, 21 Dec 2023 21:57:57 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182e987a38f403f2160fd18e4a97226800d76ff4056da04fd035d63809a3b1f`  
		Last Modified: Thu, 21 Dec 2023 21:57:57 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a4daeb984e83f601a8ea3c0ab30321429bc5c0bd4f2774406da959b862495`  
		Last Modified: Thu, 21 Dec 2023 21:57:58 GMT  
		Size: 18.1 MB (18069614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8879badc0b3c0e8b415476d7959eb7949a6160ecceabd87bb1770256a0d9bb0e`  
		Last Modified: Thu, 21 Dec 2023 21:57:55 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e00cd1568b89d48a2b5ac4ad1e0fadd16bd3c63ce8aea5807f6c35c7bc5d4f`  
		Last Modified: Thu, 21 Dec 2023 21:57:55 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1c352c86e2732ad71f97f754531720edda35485ec557c243db1a32f8840b90`  
		Last Modified: Thu, 21 Dec 2023 21:57:55 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994469f4accde9e0aa3be7e2691d22fcab34696a95fa0781927303f0d643b630`  
		Last Modified: Thu, 21 Dec 2023 21:57:56 GMT  
		Size: 18.0 MB (18022661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f469afcd9064cd5b9d7a4c9bb7d85cac1f4c6910ad6eaafe509a75e145bea8`  
		Last Modified: Thu, 21 Dec 2023 21:57:53 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e226009c34a423dfcf5e3511619b13996803e9a2a48d197f7c7b14dc67bdcb`  
		Last Modified: Thu, 21 Dec 2023 21:57:53 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee4ad5795e3b8aff67ec228638a73f14e9719cb2ae0e096eed6036c79ee7a47`  
		Last Modified: Thu, 21 Dec 2023 21:57:53 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a63d7c4aa39b824dd750b66bb4e05ab1449338d39b8d3e1f922e16bd27ceeb`  
		Last Modified: Thu, 21 Dec 2023 21:57:56 GMT  
		Size: 18.7 MB (18700455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

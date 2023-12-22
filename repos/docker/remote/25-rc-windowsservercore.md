## `docker:25-rc-windowsservercore`

```console
$ docker pull docker@sha256:0730e628fa8e1256b39ca8c62d915634fc95d18ac2e37e1f54ffdbf7dd36e55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `docker:25-rc-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull docker@sha256:3a644ba1ba1577b0b667fca0a2a53aa63077bf0355c171b39ccd42567e02afc0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1944618217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8015f9a8b436cdd55e1d91eb93777f27b0ec246ccbfd904b6f908ce5a70325`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Thu, 21 Dec 2023 21:54:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 Dec 2023 21:55:17 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 Dec 2023 21:55:18 GMT
ENV DOCKER_VERSION=25.0.0-beta.3
# Thu, 21 Dec 2023 21:55:19 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-beta.3.zip
# Thu, 21 Dec 2023 21:55:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 Dec 2023 21:55:35 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 21 Dec 2023 21:55:35 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Thu, 21 Dec 2023 21:55:36 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Thu, 21 Dec 2023 21:55:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 Dec 2023 21:55:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 21 Dec 2023 21:55:46 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Thu, 21 Dec 2023 21:55:46 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Thu, 21 Dec 2023 21:55:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d87b4606b3212604c7893b430818dbaeb2f1b85c475442fde8fbbc36dfa8f8a`  
		Last Modified: Thu, 21 Dec 2023 21:56:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb89559970acef8de661fe76367f0379bda202b16b573391bba52962d55e12`  
		Last Modified: Thu, 21 Dec 2023 21:56:04 GMT  
		Size: 510.0 KB (510012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df70bf943d66ee8b6d4517412a443c1f0a3ab8261741008fae729d2528530d18`  
		Last Modified: Thu, 21 Dec 2023 21:56:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bab60bac21403c877ead0dbd4dfe7c37cd73660114ad5a16d8c6aa194ecd39`  
		Last Modified: Thu, 21 Dec 2023 21:56:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6c1dc09fce01efcdd9a0c646181ad50ebe5523f416ffc601adc7ad565888aa`  
		Last Modified: Thu, 21 Dec 2023 21:56:04 GMT  
		Size: 18.1 MB (18070959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c431533192a46f8db0a0d4c0abab1ad411784dcd3bf127177e4686ceb0341096`  
		Last Modified: Thu, 21 Dec 2023 21:56:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dc6b11edabc1d934517d94f26b8c25d75fc4e1d2c4d6f7a511d995d023480b`  
		Last Modified: Thu, 21 Dec 2023 21:56:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4ab69e35e0139e3d0f42811abed0107c86feb7c58388402d06b80de29570eb`  
		Last Modified: Thu, 21 Dec 2023 21:56:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e1eb1ee88e0f551f3e425507ead1bd60cc8531b535012d7c0771a531b460d2`  
		Last Modified: Thu, 21 Dec 2023 21:56:02 GMT  
		Size: 18.0 MB (18033634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0d2de598a0146368bf84b28bacd8ec63bcabab65b67719da5aee6010b9c6f6`  
		Last Modified: Thu, 21 Dec 2023 21:55:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dafc02a1350784579dee07df375f2e8eed9be3c3a0d4bdce2608d71309e01f`  
		Last Modified: Thu, 21 Dec 2023 21:55:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17264a80e1a891fa2119b3960d2be67acac36ad59d25c46d3cc1285fb869bf37`  
		Last Modified: Thu, 21 Dec 2023 21:55:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe9d19570df185d9d6ed782555d0decbd0b4cdeb0e3bb08942f60d12bc5b310`  
		Last Modified: Thu, 21 Dec 2023 21:56:02 GMT  
		Size: 18.7 MB (18718407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-rc-windowsservercore` - windows version 10.0.17763.5206; amd64

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

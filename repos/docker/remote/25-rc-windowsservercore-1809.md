## `docker:25-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:8813bfeea3e20f3d2a8831211e3ed900e8cbac4a298aa8f20e226f66b6aa9e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `docker:25-rc-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull docker@sha256:732365a4af2b88095979b4a5e6883d3f23625d8b935bb448bc330ea46cda95d8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2112770630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0a4e3f9a81fa45bbe2cf28719e6b8ee08ef8bf242cfa6c6518cc02eddeccf1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Tue, 28 Nov 2023 19:12:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Nov 2023 19:13:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 28 Nov 2023 19:13:50 GMT
ENV DOCKER_VERSION=25.0.0-beta.1
# Tue, 28 Nov 2023 19:13:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-beta.1.zip
# Tue, 28 Nov 2023 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 28 Nov 2023 19:14:23 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Tue, 28 Nov 2023 19:14:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Tue, 28 Nov 2023 19:14:24 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Tue, 28 Nov 2023 19:14:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 28 Nov 2023 19:14:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Tue, 28 Nov 2023 19:14:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Tue, 28 Nov 2023 19:14:53 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Tue, 28 Nov 2023 19:15:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274226f307c42ddf799e466706a17bc1b8391b737b34a7b49e93c995e240c7bc`  
		Last Modified: Tue, 28 Nov 2023 19:15:26 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c667490cc9f59c8fae0a545a64423e3e3519fba626867a82a7c0d805edfb8e`  
		Last Modified: Tue, 28 Nov 2023 19:15:26 GMT  
		Size: 506.8 KB (506848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70633e7d35f2646a27fba07d2cfabfdba9a65ac34c711758522baf3961effd30`  
		Last Modified: Tue, 28 Nov 2023 19:15:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b1dda01420dc45d069a171dceb04005bb40fae6c203705bdab1395b32637dd`  
		Last Modified: Tue, 28 Nov 2023 19:15:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715641b9d2b83101b7e2f65491502effa2fc2d6c752b59fe189e3f96df2619a7`  
		Last Modified: Tue, 28 Nov 2023 19:15:27 GMT  
		Size: 18.1 MB (18077940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b8c334c396a02f41f2288ad0c95eb4e7f9c7a25ca8c9126c626f4703100033`  
		Last Modified: Tue, 28 Nov 2023 19:15:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ad2a62bbb540424cfe9d90c4bfea44ed4f2f7d5a73d88b048ebd0177676979`  
		Last Modified: Tue, 28 Nov 2023 19:15:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41d0158086805135ccdc191feb4b8c8039e9e09a8868381f830a182596bc084`  
		Last Modified: Tue, 28 Nov 2023 19:15:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c15b6dabadb579b2de095e542af20ea0a3c965978c393c9cd23220655cabcda`  
		Last Modified: Tue, 28 Nov 2023 19:15:24 GMT  
		Size: 18.0 MB (18032221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea246d33e269180640e9396653ae5ab02b275bf6108dc6d2a834e028df19b084`  
		Last Modified: Tue, 28 Nov 2023 19:15:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c62f40ab137fe4d08655fc941609aa32777b00f8e9574180df13e1e0632998`  
		Last Modified: Tue, 28 Nov 2023 19:15:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4812f69249bd117ec906398f1a2732b1902910ac55abc35739f3c10f99cbdf39`  
		Last Modified: Tue, 28 Nov 2023 19:15:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adaee7630e2aa6fd8022c484eea1dcb3dda278d2742e7392d27e2764767452c`  
		Last Modified: Tue, 28 Nov 2023 19:15:24 GMT  
		Size: 18.7 MB (18710422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

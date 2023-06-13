## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:8ede108da743c3e32b7f7f50489c6e0ce307041115ad9ae00d4e001c8ca793ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull docker@sha256:0c06be5c82a60164d66e10197dadbe26a0481f0e972482c1e7d758702c249cd2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124730612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca096918d4d76492a21da4d5e011f2e8d189bb941d00442b81cf3a74fc7e236`
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
# Fri, 26 May 2023 20:16:45 GMT
ENV DOCKER_VERSION=24.0.2
# Fri, 26 May 2023 20:16:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.2.zip
# Fri, 26 May 2023 20:18:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Jun 2023 19:15:46 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Tue, 13 Jun 2023 19:15:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.windows-amd64.exe
# Tue, 13 Jun 2023 19:15:47 GMT
ENV DOCKER_BUILDX_SHA256=e314569943a591a097fa9119bf786556a4eb5c710e8ddefa57e95cd95aa7cc7f
# Tue, 13 Jun 2023 19:16:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Jun 2023 19:16:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Tue, 13 Jun 2023 19:17:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-windows-x86_64.exe
# Tue, 13 Jun 2023 19:17:00 GMT
ENV DOCKER_COMPOSE_SHA256=6083a9057010a6a048d83c94318d254657abee48600baca2402fbe887d0b7ec4
# Tue, 13 Jun 2023 19:18:07 GMT
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
	-	`sha256:6ad22f2ee43697a55f2e503a988aa85218f9b630b0a3f758e9447c5ac1e27453`  
		Last Modified: Fri, 26 May 2023 20:21:44 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf788472f20903106872eef43bdf092497865c0b1a868b1dcd71fe678ed6145`  
		Last Modified: Fri, 26 May 2023 20:21:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b36025120fafff587778c5463dc69a3b86ebcb8bdf4b001e201c209c53cdc`  
		Last Modified: Fri, 26 May 2023 20:21:46 GMT  
		Size: 17.5 MB (17474917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f60baebd72aa75c81d2c35a0c9e7028947c035b439704c01325383dc57a3cc`  
		Last Modified: Tue, 13 Jun 2023 19:22:33 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1facb2d6846543effdc155079b23678fbc9e9e38b2fb6e1fed1bd08a42563`  
		Last Modified: Tue, 13 Jun 2023 19:22:32 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708a595596c59e334b8800ca7cfcd3669bc76da31a6ec14f815e18fc44c374ef`  
		Last Modified: Tue, 13 Jun 2023 19:22:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7440e5ca4222043f68205a304a2bcf5e935835391711a7d117dccf93a67d7ec`  
		Last Modified: Tue, 13 Jun 2023 19:22:35 GMT  
		Size: 17.9 MB (17889326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0f25f527a51c4ec510ae43c9bd28e18cff0c1e417f9435166f56697d0855a8`  
		Last Modified: Tue, 13 Jun 2023 19:22:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93ae4bd50bea8873bfb2ac63e61f80661c809e55695cddc124a5c3a72eb227`  
		Last Modified: Tue, 13 Jun 2023 19:22:31 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df267612c4a7bc26d4d33ef105f80ec3d61a5c947f7c7413e28a93c1e86c1006`  
		Last Modified: Tue, 13 Jun 2023 19:22:31 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cba55da972e2d06d5223ac9a55ee377301662cfe37f06b1bf9d568e4f96d9eb`  
		Last Modified: Tue, 13 Jun 2023 19:22:35 GMT  
		Size: 16.9 MB (16867033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

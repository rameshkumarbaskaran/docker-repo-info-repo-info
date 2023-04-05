## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:caf365cd0235963358eccfb3b4a39ca10686e5a30075686df7c686a2fbd3e6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.1607; amd64

```console
$ docker pull docker@sha256:5c41810c395cfa341bf8ea4daf4bd2ce28b4cf09e32143fb52da0df9d83ac919
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1805393984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfd317a6536592b078d4e7ef658bf0e790c770f337932513d4ae39a30555a9a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:48:27 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Apr 2023 00:53:01 GMT
ENV DOCKER_VERSION=20.10.24
# Wed, 05 Apr 2023 00:53:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.24.zip
# Wed, 05 Apr 2023 00:53:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 05 Apr 2023 00:53:42 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 05 Apr 2023 00:53:43 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 05 Apr 2023 00:53:44 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 05 Apr 2023 00:54:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 05 Apr 2023 00:54:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Wed, 05 Apr 2023 00:54:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-windows-x86_64.exe
# Wed, 05 Apr 2023 00:54:22 GMT
ENV DOCKER_COMPOSE_SHA256=0869cfe9d799d511e4eaf87029ed08ea256e7000f312023c062d7ddcadc385db
# Wed, 05 Apr 2023 00:54:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8618e746130a44a38c8238602d9bcd946d80bd2d8378a6a88b481e06dbb717`  
		Last Modified: Thu, 16 Mar 2023 05:04:57 GMT  
		Size: 733.4 KB (733414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bff9453791d59645a3764aa07213cf4469d97e18f5686e52daf38282b208fdd`  
		Last Modified: Wed, 05 Apr 2023 01:00:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f21fe28b296c95f72b86f4ddf68bac381ac57f5f8566dbff8a76ced157f06d`  
		Last Modified: Wed, 05 Apr 2023 01:00:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0e2bf3baffdefe49e31ed55c4dc8e02c599b1d76f2dedd00a6968dd085a5d5`  
		Last Modified: Wed, 05 Apr 2023 01:00:34 GMT  
		Size: 56.9 MB (56887348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513ae2bdcbed244e6d338bacd519652d749f68335c62568bc2c14ed4b24429b7`  
		Last Modified: Wed, 05 Apr 2023 01:00:23 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b064343e2e824a0165fc1245181a5a46a554a8ae9d988e2877967ea2ceed9657`  
		Last Modified: Wed, 05 Apr 2023 01:00:23 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b79112c52a33709ea8155d0a788f7c3e20cc7fcf53bde9ff8d9e3fc21ccd81`  
		Last Modified: Wed, 05 Apr 2023 01:00:22 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220cf5a255e570d4768109feafa5d935e9bca2ba99064d5c194d1214068b980`  
		Last Modified: Wed, 05 Apr 2023 01:00:23 GMT  
		Size: 16.7 MB (16722842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd686db35c4bfc13df31b280ed1fbb13688da03d645a3bd2c8bb9d8df15a4d6f`  
		Last Modified: Wed, 05 Apr 2023 01:00:18 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f9641d9ff2e932c8f6db964b4a3c06c16f8e9aaef53558cbfbd198100bc0ad`  
		Last Modified: Wed, 05 Apr 2023 01:00:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19169c5f7dc5dd1560995bb8b3d273aa3797b916d6b09e9e2441fcdd0d8709d`  
		Last Modified: Wed, 05 Apr 2023 01:00:17 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b55e0252c9fca1a67d4fa0e8816316766ba06d206d21354a06ef1922fbb57dc`  
		Last Modified: Wed, 05 Apr 2023 01:00:23 GMT  
		Size: 17.1 MB (17097528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull docker@sha256:0a2c940a5b2e961f16c37caa18dbe24641dd252d727e795900ea7c5c94a8b95d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2104055841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434cb38780e61224904e717c4ceb0b37d5c17764f1c9ad88a33a6ea2933d466`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:51:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Apr 2023 00:55:01 GMT
ENV DOCKER_VERSION=20.10.24
# Wed, 05 Apr 2023 00:55:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.24.zip
# Wed, 05 Apr 2023 00:56:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 05 Apr 2023 00:56:17 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 05 Apr 2023 00:56:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.windows-amd64.exe
# Wed, 05 Apr 2023 00:56:19 GMT
ENV DOCKER_BUILDX_SHA256=e4bb5f70d98be80421bb26b78dd71fe9184a5f94315a6712f487e9eb252ad4f1
# Wed, 05 Apr 2023 00:57:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 05 Apr 2023 00:57:30 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Wed, 05 Apr 2023 00:57:31 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-windows-x86_64.exe
# Wed, 05 Apr 2023 00:57:32 GMT
ENV DOCKER_COMPOSE_SHA256=0869cfe9d799d511e4eaf87029ed08ea256e7000f312023c062d7ddcadc385db
# Wed, 05 Apr 2023 00:58:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a1257835f94345167154714886a4d51ef66180e08e94b575d6b92e636cfbd`  
		Last Modified: Thu, 16 Mar 2023 05:05:31 GMT  
		Size: 478.7 KB (478744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f916ed3c07592b3fb0c003b817ccca6f9c24fe8d60f924f082d56a23172fce`  
		Last Modified: Wed, 05 Apr 2023 01:00:53 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f144cbbe025b8322fcc3a734dbcc928ad6ddc95000f594a01ab75184e3aab91`  
		Last Modified: Wed, 05 Apr 2023 01:00:53 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee965f4b52d399d11ecc3ed155deac267061100239a9fbdb45bcbbc3c65050eb`  
		Last Modified: Wed, 05 Apr 2023 01:01:02 GMT  
		Size: 56.7 MB (56675848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5ea70adcc60b8191bc62e61b767cbd6b1f061a85ff8584691a891a0b86c5b6`  
		Last Modified: Wed, 05 Apr 2023 01:00:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649dcb266c1edec4c364b97ad053accddd85658302ab7aeda6d76c58fbc9de8d`  
		Last Modified: Wed, 05 Apr 2023 01:00:51 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296bc9aa9cd0b059387383df83a3f1702424825d3190f01870bd8da89aa73e6`  
		Last Modified: Wed, 05 Apr 2023 01:00:50 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fd9a5e5d656eac0aa9f9200448bbf2e7b90aeab1acd226915c1a9e00eeac52`  
		Last Modified: Wed, 05 Apr 2023 01:00:51 GMT  
		Size: 16.5 MB (16509033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c1ef34e828aad35e8354729342a659c131493e0fbad0474a948c95c8737a`  
		Last Modified: Wed, 05 Apr 2023 01:00:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6d201345b62f6f3b7d0364f07d501f76168a513057320e08cf3d3cdfa34cb`  
		Last Modified: Wed, 05 Apr 2023 01:00:46 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875d1f504ea11770709e997821ec2c6fd2a38aa3b486203c5bd53d945cd057e`  
		Last Modified: Wed, 05 Apr 2023 01:00:47 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a357f522d89ac15d3637267a5afb3ee1753f04ef49b8adc4c8b397623e98216e`  
		Last Modified: Wed, 05 Apr 2023 01:00:52 GMT  
		Size: 16.9 MB (16870502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

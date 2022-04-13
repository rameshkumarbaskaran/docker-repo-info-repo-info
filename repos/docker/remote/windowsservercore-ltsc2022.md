## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ed4f3e2f83acb261c846cb191bee30f0a103c011ad5900fa0b8c29493bbefb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull docker@sha256:fff694b8e04634839d70b3dfe7df104ad5534468ca98045d5a8afac643a2a6db
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2281425027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a5211ccf13b003be0b83bdcc11c10e78c678f99b447d4b31a9b8ee3f354978`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 18:53:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 18:53:41 GMT
ENV DOCKER_VERSION=20.10.14
# Wed, 13 Apr 2022 18:53:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Wed, 13 Apr 2022 18:54:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214a200bfffc3a07addfc26100cb111b878672dab66c4783d9130c9c1368804`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 627.9 KB (627901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b4c4063682b1a627c15d4272a77431260ca06226d48bcb01ecec36fddc82a`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc258b4f0c17f5025bc4293e83eda411702017e5eff5de41fd744d24427867d`  
		Last Modified: Wed, 13 Apr 2022 18:57:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2a3d2481445420779bbb18707a79b51f161df7672019ac72ce1cbda63500b7`  
		Last Modified: Wed, 13 Apr 2022 18:58:38 GMT  
		Size: 53.8 MB (53838047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

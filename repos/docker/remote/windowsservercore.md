## `docker:windowsservercore`

```console
$ docker pull docker@sha256:c9007342d9f573c7816bd119aa421275c1fc7311178ffdc53867a408e7c0fe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `docker:windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull docker@sha256:3c25629e04bb64763080dbd3242b6b4030a6090280ca13012f370684cdbb5f5f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1404236695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfb84c4aec9d9c18a6b3caf9a2042a6e2223e2d8994d6285f5d2d2d3e38aec8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:38:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 02 Feb 2023 23:15:46 GMT
ENV DOCKER_VERSION=23.0.0
# Thu, 02 Feb 2023 23:15:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.0.zip
# Thu, 02 Feb 2023 23:16:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9fbb5bb66b4765df4292381a96e1cfc78d67a08a48a930d66d57438abacd1`  
		Last Modified: Thu, 12 Jan 2023 05:42:25 GMT  
		Size: 612.2 KB (612183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a171f0fc85a0e43837a63bac9f3016de754c09fa1ca8ae53e814c979e68caa5`  
		Last Modified: Thu, 02 Feb 2023 23:18:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2227192810114625ec1260c1b2286efd48bc946fda9ff203bcda737e2ff31b7`  
		Last Modified: Thu, 02 Feb 2023 23:18:20 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8305d74c5a2e05195b696864dd2dfa2d185b70d6c5f44e1372c4e84c191eec2`  
		Last Modified: Thu, 02 Feb 2023 23:18:23 GMT  
		Size: 17.6 MB (17591184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull docker@sha256:ba52b479e095cd1d65b86fdffed716de0c77156fed1455663b4b86315dd07da3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1725694263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d38c8a8291f7614bdeee790eadb805c253f786fad6fb58fe4d8ff099650ef42`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:39:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 02 Feb 2023 23:16:43 GMT
ENV DOCKER_VERSION=23.0.0
# Thu, 02 Feb 2023 23:16:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-23.0.0.zip
# Thu, 02 Feb 2023 23:17:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1203a660d1e7b9cba56b0f2b04e0f4d443536c90572741405636436ed42c43`  
		Last Modified: Thu, 12 Jan 2023 05:42:38 GMT  
		Size: 365.4 KB (365388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96d50edf7fe06296b8196c1b41823fe86806a5d782df7da0b7a110b7f5d0b55`  
		Last Modified: Thu, 02 Feb 2023 23:18:36 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1646859efae97a08058cbc690ce4b5096e35c3e330512da50182e602d6674d4`  
		Last Modified: Thu, 02 Feb 2023 23:18:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701106aa3f077eb89cdf37b5d0740b2ba6ccc28f795a60102ea32e3b6919b51a`  
		Last Modified: Thu, 02 Feb 2023 23:18:39 GMT  
		Size: 17.4 MB (17380685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

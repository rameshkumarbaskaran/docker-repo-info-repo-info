## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:00d2d34e967f76bc9c3d907aab52fc771a5d7377187b82e23a567d3c6ddcfeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.3887; amd64

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

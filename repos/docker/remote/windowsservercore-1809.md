## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:5fd3cd170a59dbb1d11c44c7369f9f7127a8df53ff91167fa063a1c0cbf3a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

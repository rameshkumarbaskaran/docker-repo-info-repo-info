## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:2272502dbceb99df92749c23cead4541a3cd29399985a8cda759d06de33695a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull docker@sha256:1f4a556c08bc2f54c0337847e0ffd964ad39da892c5d36fc851728d60645977f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2767267293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bd03586d74b4c955573cd12d7ffeee64d0ab5726133d250bb98debdcea99dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 16:47:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Feb 2022 16:47:43 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 09 Feb 2022 16:47:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Wed, 09 Feb 2022 16:49:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0c1566a9285d9465334dc923e9d6fd93a51b3ef6cb8497efcacbcf64e3b93fc`  
		Last Modified: Wed, 09 Feb 2022 13:26:13 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72a03d8794632411bdac87991ccc5072a7e43c59b1b15872f95a515574374f`  
		Last Modified: Wed, 09 Feb 2022 16:50:48 GMT  
		Size: 355.8 KB (355814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff3ca4b20f99cfa66af21bb631cd8ef337bfa3ee14ca7d9c338f9b9b31916f`  
		Last Modified: Wed, 09 Feb 2022 16:50:48 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7184d1f3619a1387dc15260f4deb2600767a6d24cba9b2b5b4b1fa4ee6c3f9ec`  
		Last Modified: Wed, 09 Feb 2022 16:50:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca113de1ae9fce820a3d94bfcf8243bfad36e3d8c40552e8d54681c81f548873`  
		Last Modified: Wed, 09 Feb 2022 16:51:48 GMT  
		Size: 53.2 MB (53192505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

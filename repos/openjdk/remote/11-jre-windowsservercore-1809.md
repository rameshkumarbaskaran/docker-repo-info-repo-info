## `openjdk:11-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:7c7de087686a62aa8e0b8edc5327b9415afdb9ab307e429ff89788a13a7e3820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:11-jre-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:2414688ddac4ec742e3f62578815c680530a9ee71a3e2594da49b3d40e2e50cc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2489280523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f144a7aca20f28768530aacc699b1f25e18993c387fe8f632bb67e9f00f020ce`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 20:44:21 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 13 Jan 2021 20:45:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 21 Jan 2021 02:15:04 GMT
ENV JAVA_VERSION=11.0.10
# Thu, 21 Jan 2021 02:21:01 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_windows_11.0.10_9.zip
# Thu, 21 Jan 2021 02:21:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971349fa4cc521df2fdf5b01ee402b4753cd032fa00f4571fea0acfd4d0d5fdf`  
		Last Modified: Wed, 13 Jan 2021 21:26:41 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f0b6dc5ad26e757655f988b268c27fc1ae614a2b3f21efe68d1b3921d169d1`  
		Last Modified: Wed, 13 Jan 2021 21:26:40 GMT  
		Size: 9.4 MB (9361866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacab81311e2be10e52975faa21217d995d2b9bf7d2a8a5222db2e108f31df52`  
		Last Modified: Thu, 21 Jan 2021 02:37:42 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef876d146b4c445b19ca03eedd1aad8bc3372fb981e131127a251b37ad6b3ae5`  
		Last Modified: Thu, 21 Jan 2021 02:41:19 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ed779eead31c3986d928c34185a55d29ffd7ef189b7b10d8b12bd1f1cdc625`  
		Last Modified: Thu, 21 Jan 2021 02:41:29 GMT  
		Size: 44.1 MB (44141576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

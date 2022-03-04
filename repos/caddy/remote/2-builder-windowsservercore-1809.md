## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:030157eb939ca1cc00b86cd29395ce92809bf8870e00e95263963c520c36d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull caddy@sha256:bc4d3e127f67f7e9d100df01a975c4cf401b6f667fcc25faa3e00d17d5dd97f7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2886710746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3b332557918d608896c22d3f54c2c682bbe3a189612066d99b2464db7c0ed9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 13:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Feb 2022 13:42:02 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Feb 2022 13:42:03 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Feb 2022 13:42:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Feb 2022 13:42:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Feb 2022 13:43:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Feb 2022 13:43:41 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:44:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 03 Mar 2022 23:19:36 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:23:33 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 03 Mar 2022 23:23:35 GMT
WORKDIR C:\go
# Fri, 04 Mar 2022 00:18:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Mar 2022 00:18:15 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 00:18:16 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 00:18:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 00:19:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 04 Mar 2022 00:19:28 GMT
WORKDIR C:\
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
	-	`sha256:1b56caecef9c44ed58d2621ffb6f87f797b532c81f1271d9c339222462523eb2`  
		Last Modified: Wed, 09 Feb 2022 14:31:28 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3ed0a076d58c949f5debdbc3616b6ccd008426c62635ab387836344123e2a6`  
		Last Modified: Wed, 09 Feb 2022 14:31:26 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25f9584c1aa90dae36704d6bef0e59e72002fcb13e8a4618f64c9b13479c0df`  
		Last Modified: Wed, 09 Feb 2022 14:31:26 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4fbc7cf0f85fc63860f052f76bfb4429eca8b878abce79a25bfdc30f9e9f5`  
		Last Modified: Wed, 09 Feb 2022 14:31:26 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325dc9f1660ea537aae55b89be63d336762d5a3a02e929d52940586fb0f677e`  
		Last Modified: Wed, 09 Feb 2022 14:31:31 GMT  
		Size: 25.4 MB (25448246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4f3aabaa2a9bf80e2a7f417dba559f6b34e640c21b138dce099328406c8903`  
		Last Modified: Wed, 09 Feb 2022 14:31:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e61367d26baed9e16a8d5310c520ae3429d5cc7956569f325cd9de01f33604`  
		Last Modified: Wed, 09 Feb 2022 14:31:24 GMT  
		Size: 317.3 KB (317319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7518cb3ba3dce74dc8d71a5c080d41c547dd1e37df83b4dce123739c1cace03f`  
		Last Modified: Thu, 03 Mar 2022 23:47:42 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07801516439793208731bc03796466884399f623f51f546505ddc58bc26f6647`  
		Last Modified: Thu, 03 Mar 2022 23:48:23 GMT  
		Size: 145.5 MB (145537983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb6c37942a9bbb134fb90fd0c1e8cf965034ad4da2178f02f3d7541c0519742`  
		Last Modified: Thu, 03 Mar 2022 23:47:42 GMT  
		Size: 1.6 KB (1572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d660c9b1e89dff29c66bf77909e946f720b8f908a05c4285726adb127a0536e`  
		Last Modified: Fri, 04 Mar 2022 00:20:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905ce8ed12af5cf09436bda6a8377b43928f4d88d0b9ff6738038607a408223`  
		Last Modified: Fri, 04 Mar 2022 00:20:13 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b3fee22f5dda90c679720fc6bf6a72996864576f8541e029b8170af492906`  
		Last Modified: Fri, 04 Mar 2022 00:20:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534df8aaee4db3525b78885b3dce92d74207f528293803738a2fabfecaf5b7cd`  
		Last Modified: Fri, 04 Mar 2022 00:20:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1e441686aa73a5efa1e1d206db41741d3e9abbdcc072cae8dd583a06cf074`  
		Last Modified: Fri, 04 Mar 2022 00:20:16 GMT  
		Size: 1.7 MB (1673877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd9447b1d90f6b53b4333a79332156f2a5868644b8a78b861636517f5c1ccf`  
		Last Modified: Fri, 04 Mar 2022 00:20:13 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

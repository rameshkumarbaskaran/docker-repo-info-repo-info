## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:dab23b483eb9606de8d6d6b8f160e65f24960946e89bced294062f69886d479f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64
	-	windows version 10.0.17763.973; amd64

### `golang:1-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull golang@sha256:de8916c1f8f26b261d012c6c6cb2bb2f661e90939e48481a8e58781898b51f0f
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5899827997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac59959501013b6b72fd2a398b536d8164bd76216c34bb54306a602ca32812a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 13:12:27 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Jan 2020 13:12:28 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Jan 2020 13:12:29 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Jan 2020 13:12:30 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Jan 2020 13:14:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Jan 2020 13:14:10 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:15:21 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 28 Jan 2020 21:21:28 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:28:27 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '03befd335ee9ddf1d10cae52e84eb5a37408b8e105acc1c29e30bbbbd8143749'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 28 Jan 2020 21:28:30 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928afb74ac8a072334bcabee201bfbc0936217d2fa1e8aba5d7e377cb995f48a`  
		Last Modified: Wed, 15 Jan 2020 14:17:15 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d950deb3f160624c0675efc8314222a7ebb6a525dc9b4c667a022a3d796aa8b9`  
		Last Modified: Wed, 15 Jan 2020 14:17:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bab48f96d12c3da7ce1da86d0aaf6d30c4ea98ca0eee9c0a6f61ce03a143ad`  
		Last Modified: Wed, 15 Jan 2020 14:17:11 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ad2d905ad861e3648e8b50913912b3c9e5e82ba47963995a5b04eaea4b2d5a`  
		Last Modified: Wed, 15 Jan 2020 14:17:11 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579b374cfb25041394c6240e13b17f10073fcbd5c0f48b368cbf62a60bce25df`  
		Last Modified: Wed, 15 Jan 2020 14:17:26 GMT  
		Size: 30.5 MB (30488416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2daa5fc01c4917b7d04ae05018cc91d5b73b43c628028ce489eb6e1b59e2415`  
		Last Modified: Wed, 15 Jan 2020 14:17:08 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91594379dcd19aa8896900708133e96d09286f185753d4f84e9e4b075f1077fb`  
		Last Modified: Wed, 15 Jan 2020 14:17:10 GMT  
		Size: 5.3 MB (5343427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aa9e8baa14842fc0d65336ee9220248d094a18c3aacd181e9e87aff722fc8f`  
		Last Modified: Tue, 28 Jan 2020 21:59:56 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec957d2972f7b2bf8d2dbbf2a7ab95e66a7d832abdf31a51f0564be4f4229d4`  
		Last Modified: Tue, 28 Jan 2020 22:03:21 GMT  
		Size: 139.4 MB (139387180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36035c1a85f8a0bbbb9ec8d94c5c2e54fbc7da415dedd750e45269a7f7c38f49`  
		Last Modified: Tue, 28 Jan 2020 21:59:55 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull golang@sha256:e173785dbf14786e113dbc279f454de2916c33c8a435bf4c566c25456cda5bdb
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377231878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316011257cf350f62b20beb030f123d2f13404822a2f72b7fa98798c2cb40f2a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 13:22:49 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Jan 2020 13:22:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Jan 2020 13:22:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Jan 2020 13:22:53 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Jan 2020 13:23:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Jan 2020 13:23:58 GMT
ENV GOPATH=C:\gopath
# Wed, 15 Jan 2020 13:24:21 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 28 Jan 2020 21:28:45 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:34:29 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '03befd335ee9ddf1d10cae52e84eb5a37408b8e105acc1c29e30bbbbd8143749'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 28 Jan 2020 21:34:31 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c34cd616875c2f9d033967e4516512eeda759d5d727381f68534f20a423fbc5`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f8f6402962aaf689f18fb7dc48707abd1442236650fa93feafdb8a0e62b884`  
		Last Modified: Wed, 15 Jan 2020 14:19:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2ccd2aa22967996e2db31a32fa197fe049385493a27f6cac5d28e147dc77a1`  
		Last Modified: Wed, 15 Jan 2020 14:19:42 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4005eb5a3fe7e59daa2cf4c83ef39ebc3b67aa33c077f34727270a45d08386`  
		Last Modified: Wed, 15 Jan 2020 14:19:41 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123a2902604294d730658cf5b5098adc030395e96b276912489cd129282805d1`  
		Last Modified: Wed, 15 Jan 2020 14:19:55 GMT  
		Size: 29.6 MB (29634086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b4abbf4635cc281d4995cae6e8ea73c4f2713f902bf6d5e500134413fc88da`  
		Last Modified: Wed, 15 Jan 2020 14:19:38 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dc6850cb4055c8c383de6b662f37153a7fd9372a26c59bdd06bfb84f8220e3`  
		Last Modified: Wed, 15 Jan 2020 14:19:39 GMT  
		Size: 292.9 KB (292910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6b5509ac9b0f98a847b5ff3b76686a91910e59b20a405dc47180abb2fd76cf`  
		Last Modified: Tue, 28 Jan 2020 22:18:19 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179317bd76faa8fddd3ac1dcbab30a1ebdd5d2a0c30afccdfccef568947c72fe`  
		Last Modified: Tue, 28 Jan 2020 22:21:25 GMT  
		Size: 129.9 MB (129884024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4982cb305e8a7e352bdeaa5fc943817601139c9d03d31f09b10407e9fb4886d`  
		Last Modified: Tue, 28 Jan 2020 22:18:19 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

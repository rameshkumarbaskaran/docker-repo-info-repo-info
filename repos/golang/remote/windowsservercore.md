## `golang:windowsservercore`

```console
$ docker pull golang@sha256:556759be46e847bf2f1c7ba8f8e4a63eabc2ba4ecd012134d97a87efc7e3194f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2114; amd64
	-	windows version 10.0.14393.4583; amd64

### `golang:windowsservercore` - windows version 10.0.17763.2114; amd64

```console
$ docker pull golang@sha256:528d9a73e9f01c44bd725eb96c34d7f4505461ffc4201ed688ea5d7787ab8508
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2851123842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe744d35f3861c1d7346e46bac2c5f185dd42d82a56de82a5b579916cf04d87`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 12:44:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Aug 2021 12:44:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Aug 2021 12:44:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Aug 2021 12:45:01 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Aug 2021 12:46:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Aug 2021 13:03:48 GMT
ENV GOPATH=C:\gopath
# Wed, 11 Aug 2021 13:05:01 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Aug 2021 13:05:04 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 11 Aug 2021 13:08:09 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Aug 2021 13:08:13 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1014a0987936e3fa4cd5e9d82f8e82b260d69af19d422f406e4ca0ca868a2c`  
		Last Modified: Wed, 11 Aug 2021 13:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e04f285ca5202ce380345855cc1ef257dca5d10c911e569374401b838c36c4`  
		Last Modified: Wed, 11 Aug 2021 13:29:32 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e030fd545aef8a7a910823c29f1d20459a9cadda6fb139615fc2889d11f9947`  
		Last Modified: Wed, 11 Aug 2021 13:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e552f09bafcd7011149f53ca4fb6af5814124b3433a4fe57e214782457664`  
		Last Modified: Wed, 11 Aug 2021 13:29:31 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed64d631b20fa6a2ca7e09eca20fd2e38188e2c5bc403a2eb944f6287397a17`  
		Last Modified: Wed, 11 Aug 2021 13:29:38 GMT  
		Size: 25.4 MB (25449457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f305eae5b6818e3197738445312b2df80302891cbc00f133a0cd4b7ed7046af`  
		Last Modified: Wed, 11 Aug 2021 13:34:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421f7dec205350b61882c53b043a854bd0ab162395ee7016c15d2ff781492b3b`  
		Last Modified: Wed, 11 Aug 2021 13:34:12 GMT  
		Size: 321.8 KB (321814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1959338b6b9981d256f2bfb4620c4ed5381b9b0a82b5f9be48d15ca97b9bf02`  
		Last Modified: Wed, 11 Aug 2021 13:34:12 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b5e2784251d81abc926c9e399929ffe51c2b7a7d34023289da3c6fb4db65ae`  
		Last Modified: Wed, 11 Aug 2021 13:34:44 GMT  
		Size: 139.3 MB (139343081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f1889787fe27cffd35a0cffa025a0b7e3c4fd42bd8186d190ac5ead0c6a796`  
		Last Modified: Wed, 11 Aug 2021 13:34:12 GMT  
		Size: 1.6 KB (1597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.14393.4583; amd64

```console
$ docker pull golang@sha256:d2d5513c5c544adaffb3be2c0f21cec74f453186a8360feaa563770deb7b20ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6440523868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ae3e560f9a0bef52d4be9654d5826a416d09c4c4132516e2697f62c5357a49`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Aug 2021 12:51:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 12:51:38 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Aug 2021 12:51:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Aug 2021 12:51:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Aug 2021 12:51:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Aug 2021 12:53:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Aug 2021 13:08:32 GMT
ENV GOPATH=C:\gopath
# Wed, 11 Aug 2021 13:10:03 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Aug 2021 13:10:06 GMT
ENV GOLANG_VERSION=1.16.7
# Wed, 11 Aug 2021 13:13:50 GMT
RUN $url = 'https://dl.google.com/go/go1.16.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '56b3a9024268f226f679c3a8ffb21f4214a75f84050b2c395b362ae2cc8e53e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Aug 2021 13:13:55 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d4b5c087d85e7fbeffd8b282ecd862da1fb7ff00c37657c5712888936292097`  
		Last Modified: Wed, 11 Aug 2021 13:30:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf069d22adc9f9317381fb00edfaf147e2a08bbd9b9aa4e7668fced1fb98f7`  
		Last Modified: Wed, 11 Aug 2021 13:30:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fe66e8167823a0c5cbb100a89928213f61cf164cf8709d9fe899aed2983048`  
		Last Modified: Wed, 11 Aug 2021 13:30:24 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75da9fc8465c5617c2e9b3a97701f9cdfe7a723af01dc99760b253e5baccb50`  
		Last Modified: Wed, 11 Aug 2021 13:30:23 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c3e058e701d1a72c8549ecca35484b40559546a5a523f18483669e7be3b724`  
		Last Modified: Wed, 11 Aug 2021 13:30:23 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368b8f9d5f23a5a86293ff894ff67bf071ab9c9a6bcc127538fb406bbd86de0d`  
		Last Modified: Wed, 11 Aug 2021 13:30:56 GMT  
		Size: 25.4 MB (25443893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f4bdf1c17a2e86c1c05ea97436b17677c95a7900f2e9b2915cf67586841e97`  
		Last Modified: Wed, 11 Aug 2021 13:35:02 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9a1555160c8de681bd8743b3c5aba399c5849616b4e97e98ec7e1c4c2e005e`  
		Last Modified: Wed, 11 Aug 2021 13:35:02 GMT  
		Size: 312.4 KB (312414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337206097d4b8859d9ab8f271c8e34cf80ebebde1f65ef3dda8e43e466d3487e`  
		Last Modified: Wed, 11 Aug 2021 13:35:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86907a0988f9b57e4ea49e1a417c12cadb4ea9210fc7fb666606440cde4bd7a9`  
		Last Modified: Wed, 11 Aug 2021 13:35:36 GMT  
		Size: 143.8 MB (143790012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7beb41edb3bbda013ee0b275190cc4ea84514559a60a3523aeea2553c4cbf`  
		Last Modified: Wed, 11 Aug 2021 13:35:02 GMT  
		Size: 1.6 KB (1592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

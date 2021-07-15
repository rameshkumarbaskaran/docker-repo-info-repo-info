## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:f0154eaa9e2dbf0c3cdcaff8538332c786fe497522a1e2277d7bee2afa8829e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull caddy@sha256:64455ff9cc52a6eaa711eafb2f11ebc5fa78a5f15e7c1be1e4a05d2039c5eb04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6440905132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46bc0ac245d8871ca7a2ef877724591c00e6f40eb64608a40f20e5728bdd7ae`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 02:46:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 04:31:42 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Jul 2021 04:31:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Jul 2021 04:31:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Jul 2021 04:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Jul 2021 04:33:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Jul 2021 04:33:36 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Jul 2021 04:35:06 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Jul 2021 04:46:08 GMT
ENV GOLANG_VERSION=1.16.6
# Wed, 14 Jul 2021 04:49:49 GMT
RUN $url = 'https://dl.google.com/go/go1.16.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c1132ba4e6263a1712355fb0745bf4f23e1602e1661c20f071e08bdcc5fe8db5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Jul 2021 04:49:53 GMT
WORKDIR C:\gopath
# Wed, 14 Jul 2021 18:01:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 18:01:24 GMT
ENV XCADDY_VERSION=v0.1.9
# Wed, 14 Jul 2021 18:01:27 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 14 Jul 2021 18:01:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Jul 2021 18:03:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Jul 2021 18:03:04 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:624cc64d28951435759fcbbc930532718666f3285fc939c97e36c2cda79f80f2`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f667c0fc8186714bfddbd565e9cdd1dd6497e3c112f1eddb17a37d1abae30c93`  
		Last Modified: Wed, 14 Jul 2021 05:04:30 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3566f190f34782035012abf2530315039000f1d137ad0098f1903a99127b3b8e`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036fdd63bb05506922a2462b2487bb4ff12b9c29097537ee7d0ca4c18cad7507`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8904dd19478585c0fa1c9b4a25c5ac4560759b61f3f9e2ef0e6475729d5d482`  
		Last Modified: Wed, 14 Jul 2021 05:04:24 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a50006063e099df0e3d1f22baa504b0f0de1563cd642c48340cf2a8b7152bd`  
		Last Modified: Wed, 14 Jul 2021 05:04:30 GMT  
		Size: 25.4 MB (25447622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97445d6d1bd7224c109fda54abaaa5909b43be941934bc54c3aff8754b852ebd`  
		Last Modified: Wed, 14 Jul 2021 05:04:20 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187f6db85279d8f0ab2b263b47845afa4452a66c28c251f571d776001e4d300`  
		Last Modified: Wed, 14 Jul 2021 05:04:21 GMT  
		Size: 318.8 KB (318791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4a18e3af73fb6a22be9e13447c4dc03d831112dcc5d479c52c994c324b1bca`  
		Last Modified: Wed, 14 Jul 2021 05:06:53 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b18fe05fb046103c962da798acc46523e448a87265015bd0e9870d49013e2`  
		Last Modified: Wed, 14 Jul 2021 05:07:32 GMT  
		Size: 143.8 MB (143795404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eacae5fc4eee1b8807585646451e54ef2f58b632b6d045038d647606936b8f`  
		Last Modified: Wed, 14 Jul 2021 05:06:53 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9145f72acba1daf6003e68907818ef42985c05eb03e5eb0886fd4f833a7b916d`  
		Last Modified: Wed, 14 Jul 2021 18:05:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c947cad69b975374c14de848aaa54c4a57260a151a320dbe96a6348db9a8a200`  
		Last Modified: Wed, 14 Jul 2021 18:05:06 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f30145eea91938fd9fabc5f8f26fe49414b7c7807a32d8cba919c9e493f826f`  
		Last Modified: Wed, 14 Jul 2021 18:05:06 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52eadb657f23ec662680db8a9bc4e1ade309bf93d0203e4b1c07fccf629772aa`  
		Last Modified: Wed, 14 Jul 2021 18:05:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0920c1f5b52107603b2811da4a1f8d4d3582979217761675db22876a07e3cd`  
		Last Modified: Wed, 14 Jul 2021 18:05:09 GMT  
		Size: 1.7 MB (1693422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1239173a5587fc73012d57cf4f1387c28f9bb618c4bb423eaa0656dce5585a5c`  
		Last Modified: Wed, 14 Jul 2021 18:05:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

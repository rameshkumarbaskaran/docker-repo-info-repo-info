## `openjdk:16-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:0716f39330a21decffdcdb1dfc19c0ff24489ea1d91ac0e738da108bcd277f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:16-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:3070b1d145c39bc23ef7a5433366e9cdb66eff60c82e43751d6a9ed3379c1340
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2633786387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f116e1f7338a907e0dd6b0ff1cbfe3d4ae22f5c8e0037d6dcec4794c3f624124`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:39:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:46:40 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Feb 2021 16:46:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:46:59 GMT
ENV JAVA_VERSION=16
# Fri, 12 Feb 2021 23:19:52 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_windows-x64_bin.zip
# Fri, 12 Feb 2021 23:19:53 GMT
ENV JAVA_SHA256=a78bdeaad186297601edac6772d931224d7af6f682a43372e693c37020bd37d6
# Fri, 12 Feb 2021 23:21:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Feb 2021 23:21:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9fdb3b9c58e6d398b7f6c8c351559fc536c4ad21618a63035a7223b88bd65f`  
		Last Modified: Wed, 10 Feb 2021 17:16:08 GMT  
		Size: 9.4 MB (9416675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cbae332cf45a88c474364718b94c4244994fce3571327f15de12a2ca47729f`  
		Last Modified: Wed, 10 Feb 2021 17:21:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec2d38d357a2ce1384e702999180667c832dd49b5ebba43ae77ddc4cbbc4ee`  
		Last Modified: Wed, 10 Feb 2021 17:21:26 GMT  
		Size: 318.7 KB (318687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9aa67f7f03bd91f0fb211ccee19c1c55c74d2bb62000f31da50bd06ac031ff`  
		Last Modified: Wed, 10 Feb 2021 17:21:23 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399618bd870a2541b4a5d3f59ddc248eb9ae435d9d7829dbc83f072996249596`  
		Last Modified: Fri, 12 Feb 2021 23:30:56 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44c1abd46682e57b77128b19736510ca60614b4e1ff5230112dee551a90672b`  
		Last Modified: Fri, 12 Feb 2021 23:30:56 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee49deea63839a19632a29830ab18c85d883512adf28591ecba1463c0e13047`  
		Last Modified: Fri, 12 Feb 2021 23:34:29 GMT  
		Size: 184.8 MB (184776034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a24f3233af13f2a3a4b7971a07efa0cde89e1f759cb00f63b8df4c054aca64f`  
		Last Modified: Fri, 12 Feb 2021 23:30:56 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

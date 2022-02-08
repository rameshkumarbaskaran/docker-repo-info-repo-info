## `openjdk:19-ea-8-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0aa6186f276c5892c909caa721a3d27513dedf882b9196d8a6716ee39c48e2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `openjdk:19-ea-8-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:97fe8267bceb2ddd878422990784a0e6eb79d753795e976ec4cffc196ae8c86d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394095378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc775a94a5506aa73bc9cf432f89c6f763d19289d8a6d7df25e485871c76c7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:13 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:23:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:16:01 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 02:16:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:16:04 GMT
ENV JAVA_SHA256=eba519024733a2420e4c45145f4995121a1612f2dc875c1d37b0b87b69d563c2
# Tue, 08 Feb 2022 02:17:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:17:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039cc436f8de7b22962fef11f63ff7fb05b1dad02d0b04d62c514a24ef045cf9`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880009a6e2005dbfbbe934f1896114d21a0e91c8bdaffaee2d5349c8e9de467f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 506.3 KB (506304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230bc8140a00773d1f98d4eb9740fdabf77c4a0e627411866f93c2bcf5fe44ba`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec6c117ceb6c768b0bd07254fe6340382589d2060e8847d99c4d495295872`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ac597910dd57dc269873625a983522abb78bd613c2b0e22e672f726e54bb2c`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fce07c0e9c2a1d8e7157af7537405e923e44e50a8f0658a8784fca5634c9ba9`  
		Last Modified: Tue, 08 Feb 2022 03:24:21 GMT  
		Size: 185.5 MB (185479512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc1b5d167fec337d8d7f7432a817b9bb184eda685bae5066ca8acb4a6558912`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

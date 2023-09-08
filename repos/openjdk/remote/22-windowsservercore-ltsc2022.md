## `openjdk:22-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c7f276322c03e489829543dc85a1beb7d39001ea3af90de212ab0f80d1b4583c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `openjdk:22-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull openjdk@sha256:3b2a7c95f953dc7e6606aab9865559b35d89b98e29644aee5c389c2c1cf45213
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997373928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a92d8cbffc8ad6d500cfdd7635ccc68b7eadc28c387ac9b9608f463385ccc5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:36:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:36:46 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 10 Aug 2023 02:37:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:34:04 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:34:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_windows-x64_bin.zip
# Fri, 08 Sep 2023 19:34:06 GMT
ENV JAVA_SHA256=5a35fb7df33acaa4b3c14709a44966425b87a11c401c62e341d0fd8496cc11a8
# Fri, 08 Sep 2023 19:35:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 08 Sep 2023 19:35:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18930eb7350c60f06351657db53550ff8c064f9f63673a2955eb64b696ffbd`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 452.7 KB (452708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c00de06770671fea1af1d4340401ecedf3ab6e36133f76fd965e626275a3ef6`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d260a183baa6941016ec79f387e49673760fd96dd3bae427fc4233c651e2046`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 262.5 KB (262490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd71ea24262331e485899b45446ecea780534abc2d4bbec0e6dee47b9f78b06f`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b729054f448b11b8b90878067a052928c71d8a020466b8404bc89aa29e44d`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8092e25ff8095a7334965ba94241cd664e90e44fcae9bb4072c604cbe3dd13b`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6218dc532877355508e38f38bd81bb3c76317d6c921bfd585619e80968ce200`  
		Last Modified: Fri, 08 Sep 2023 19:39:21 GMT  
		Size: 199.3 MB (199286494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d68875bbc0c35fa5c459d7fcb15bc2fe90f5f0d78c5fc5db6b285b96f128c`  
		Last Modified: Fri, 08 Sep 2023 19:39:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

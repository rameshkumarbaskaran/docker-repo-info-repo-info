## `openjdk:21-ea-30-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:314ff6ddcb521dc0409b053dbbb67607e9e459086ea9e173322914747087ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `openjdk:21-ea-30-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:e9d584a69200ab13d9dc5251568a73cbf632beeca56691edf7c2b77c46cb6c17
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625167354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748309dce7d81200ceca6f17277d99e4fe1e9c8b6d6b6b4dc106fa3e59ff948b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:03:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:07:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:07:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 10 Jul 2023 19:23:30 GMT
ENV JAVA_VERSION=21-ea+30
# Mon, 10 Jul 2023 19:23:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/30/GPL/openjdk-21-ea+30_windows-x64_bin.zip
# Mon, 10 Jul 2023 19:23:32 GMT
ENV JAVA_SHA256=058b77ba0f35accfa2d836fbc074104dce4200f87fadf36b4a790de8216c7d73
# Mon, 10 Jul 2023 19:24:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 10 Jul 2023 19:24:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de10d117b5ef80c7852b0714d37536955d84892882d5f3f97a4d53631493623`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 318.8 KB (318813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec6f45c20e189779c1a14ac267c15e9db3eefe85034e40b6f92372759a288a`  
		Last Modified: Sat, 24 Jun 2023 03:14:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb14372fe1d2fbfda13afae0e93eb2611308220211945e4daea088ac9989f16`  
		Last Modified: Sat, 24 Jun 2023 03:14:22 GMT  
		Size: 262.8 KB (262765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89683b160bbffba14d7f0a898384e1574fd76c2e5974cd071ee03709c3d3acd7`  
		Last Modified: Mon, 10 Jul 2023 20:18:59 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ccb3c9c474808f67cb41e27947a7792953e9dd3d8786055133f43eb36bab69`  
		Last Modified: Mon, 10 Jul 2023 20:18:59 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81a3de8148c92cd13b4cc76e5da8516be4915d9cdec456c5c310f2506871bb0`  
		Last Modified: Mon, 10 Jul 2023 20:18:59 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5c796e736c7bd3ff65445cde53c12a7cd2d5bacbcb3815a42c5496181a40a9`  
		Last Modified: Mon, 10 Jul 2023 20:19:18 GMT  
		Size: 198.3 MB (198278826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b408e6a1d3bb37cc413b90f2db4f6e4a0b8af43ec7822b94447f5750a6cf7bce`  
		Last Modified: Mon, 10 Jul 2023 20:18:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

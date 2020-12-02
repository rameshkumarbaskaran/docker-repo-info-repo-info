## `openjdk:16-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:4e71c0ca55a2445c11c88a1f7fc70a21cc1bd3ee74f699dae0a46fddd6a2271a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `openjdk:16-ea-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:c6f963cf6a915c7d77d9a97dbcc89dbd645e1b15bc484fd347d2641897e46293
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2582164434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d06b48ab2f1f539c733a81048e869b0bf28a4d6ef39391f39ff8681da63be3b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:45:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:45:36 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:45:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 01 Dec 2020 23:15:11 GMT
ENV JAVA_VERSION=16-ea+26
# Tue, 01 Dec 2020 23:15:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_windows-x64_bin.zip
# Tue, 01 Dec 2020 23:15:13 GMT
ENV JAVA_SHA256=c53a02f1881035b863fa7bd128e87c2cd95a8a0306feb753b6b2b1eeb0d777d9
# Tue, 01 Dec 2020 23:16:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 01 Dec 2020 23:16:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bee39b5545a888688525644d5ac139bf90e9e5031cc78ac03612316b125116`  
		Last Modified: Wed, 11 Nov 2020 18:25:54 GMT  
		Size: 9.2 MB (9240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137fed5035462ef3e8b61dc554137650a8cfdbda487936adb705e2cd184bf115`  
		Last Modified: Wed, 11 Nov 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c03d4f5a3977a1dad2edfe3806bcaa8f0d4ce2d47ea49f0fdc3a58fc019897f`  
		Last Modified: Wed, 11 Nov 2020 18:25:43 GMT  
		Size: 307.0 KB (307020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8bdbb2a8d2f1c069401388dfa0263e1338ff92189ade605061319d132eb08e`  
		Last Modified: Tue, 01 Dec 2020 23:24:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddc92b460c3992f7a0dc8e2e89d186d09528ba07f3a0927b08121ceb43e3a53`  
		Last Modified: Tue, 01 Dec 2020 23:24:38 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7ef7b13f775e47824eee2cddf0cbf13ccd6acb8d7433204eb353017ca7032`  
		Last Modified: Tue, 01 Dec 2020 23:24:38 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d95074474394a580fe8c505ed1ce76dc0dc45d74130b2ac35a3af324c51c9`  
		Last Modified: Tue, 01 Dec 2020 23:24:56 GMT  
		Size: 184.6 MB (184580970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa4c4237b330fc7865c6d55551df174ff00c4d209dbb386fa6a52f0a9b086a`  
		Last Modified: Tue, 01 Dec 2020 23:24:39 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:807a8cd57b18c5801735957e4aeb61621b2790dd7cc53c49e8b6a17ec56c60a8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5976072562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f8f16df6b7a2f42ddb8ed796512e36074357bace374ea82c138af26ae26480`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:49:02 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:50:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 01 Dec 2020 23:17:08 GMT
ENV JAVA_VERSION=16-ea+26
# Tue, 01 Dec 2020 23:17:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_windows-x64_bin.zip
# Tue, 01 Dec 2020 23:17:09 GMT
ENV JAVA_SHA256=c53a02f1881035b863fa7bd128e87c2cd95a8a0306feb753b6b2b1eeb0d777d9
# Tue, 01 Dec 2020 23:19:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 01 Dec 2020 23:19:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1222181efe25bb0d500f320707eb7dc24e576749c0897042ae1f3b8116e87990`  
		Last Modified: Wed, 11 Nov 2020 18:26:42 GMT  
		Size: 10.1 MB (10078764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e1a3de99f869c8010907852bce9306cb6693a16fc9fad69ea0bb744446cdc`  
		Last Modified: Wed, 11 Nov 2020 18:26:29 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd970ee1e99b8801c2230b471ed6d4dc79d30324c882f32ae8efb05d8be0d34d`  
		Last Modified: Wed, 11 Nov 2020 18:26:31 GMT  
		Size: 5.5 MB (5511761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc47daf079ce05d67622f58322963e44964c585b93f4210d950ec72d5fb434f`  
		Last Modified: Tue, 01 Dec 2020 23:25:26 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601e65c96a2a0a62719f74839cfdeb3f4032e35b08a6366120513f1ce13d5030`  
		Last Modified: Tue, 01 Dec 2020 23:25:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd7e40a74ca0f30309bb52c1e471f7421c20100b93eb1ac9aa7f77277e70ef3`  
		Last Modified: Tue, 01 Dec 2020 23:25:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a67569bc6b9acd3b6db119a1e268ffb79a958e3ae18e92cd24ed77d91e09e77`  
		Last Modified: Tue, 01 Dec 2020 23:25:45 GMT  
		Size: 189.9 MB (189916350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626cf699db54e0ce747262fe085b8de7b3062a61894c21e78941e289518b710`  
		Last Modified: Tue, 01 Dec 2020 23:25:25 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

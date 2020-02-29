## `openjdk:15-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f1be74955bdbb5b33d98c275d0f87cb8b59bf9869b6c79844e3839c79cfb1fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-jdk-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:5905a98c937f3a3016d05db6fcca25805550ab4beae567e988f47d4f3f3568c7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2429020000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63caa2742b8fa9dd0e63a074f918c487aadfd3da1b4205a7824f057795aecb17`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:14:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 01:14:34 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 01:15:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 29 Feb 2020 01:33:44 GMT
ENV JAVA_VERSION=15-ea+12
# Sat, 29 Feb 2020 01:33:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/12/GPL/openjdk-15-ea+12_windows-x64_bin.zip
# Sat, 29 Feb 2020 01:33:47 GMT
ENV JAVA_SHA256=78ef2cfe5338ebbbc564ded7fa44af2ea0d9904ada059123ef5db1128f9168bc
# Sat, 29 Feb 2020 01:36:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 29 Feb 2020 01:36:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f0782e4992ed8796b0b5659aad759ed2fb47d4fafaaa5a38afe4f993f94d68`  
		Last Modified: Thu, 20 Feb 2020 03:03:23 GMT  
		Size: 4.6 MB (4567940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b83b3b5abce3322c8ff4f4b887b48ae519c81efaf348894c9a75224c981e37`  
		Last Modified: Thu, 20 Feb 2020 03:03:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211d20742c6d6be7334058298e82bd2e728c2b30ec35eccc457a3a8283457c3e`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 291.1 KB (291148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91da643e7cdde8f13e14533b558ae0dbb029efd29fb10f7b89e22509bbb0b74`  
		Last Modified: Sat, 29 Feb 2020 01:45:28 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e796bf1b138a8b6160e5930abb26b5f783aa9089aa918d6163e1353bf096c`  
		Last Modified: Sat, 29 Feb 2020 01:45:28 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae8b13f3477b5a82d865d9d96bc3f0f845affc9513ae1eabe80c468a5f4d99`  
		Last Modified: Sat, 29 Feb 2020 01:45:28 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c7955851113a1304af365c2f69057e1b6fa128b4a4c8debd960609390f1bf7`  
		Last Modified: Sat, 29 Feb 2020 01:45:50 GMT  
		Size: 193.6 MB (193649860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5bbddf5bedf37842df69df07a13878f53063fd0a2d9800786475a1898cfa7e`  
		Last Modified: Sat, 29 Feb 2020 01:45:29 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

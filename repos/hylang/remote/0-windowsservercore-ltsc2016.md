## `hylang:0-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:5ac396bc959f9b8f70d772ee8f1496712837a8c5b57410466e68cef5027f5f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `hylang:0-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull hylang@sha256:d655a8fd5939b0975ac445fe16738cc9d0854015972dd648d76a261e4fafa351
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5805658944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906d05914bf794c3cb875d7de13c45a663299aee8efd9e1e86c0284f27f30717`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:03:05 GMT
ENV PYTHON_VERSION=3.8.2
# Wed, 13 May 2020 15:03:06 GMT
ENV PYTHON_RELEASE=3.8.2
# Wed, 13 May 2020 15:05:30 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:05:31 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 13 May 2020 15:05:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 13 May 2020 15:05:34 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 13 May 2020 15:07:15 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:07:16 GMT
CMD ["python"]
# Wed, 13 May 2020 21:24:19 GMT
ENV HY_VERSION=0.18.0
# Wed, 13 May 2020 21:25:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 13 May 2020 21:25:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f7367062910f530778e9ee19dcc10d40cbc5cbebd7f3fde461d44fba50b4c`  
		Last Modified: Wed, 13 May 2020 15:18:21 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556e62081eb46acc1ff222ad395cd34a96757ae241bae1000302d864065d03d`  
		Last Modified: Wed, 13 May 2020 15:18:21 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c807258e3d35f36e5a79adeb49adcf44333293a2e8a4a66cc260533157687a51`  
		Last Modified: Wed, 13 May 2020 15:19:25 GMT  
		Size: 57.1 MB (57084743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5f6aff38fcf5fd267ce50dabf9294d922512204f9b7b9df00c68c45970666a`  
		Last Modified: Wed, 13 May 2020 15:18:19 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eada7477bdd04378a0346a295315e13cf41480db1603aae8d5332098287827b`  
		Last Modified: Wed, 13 May 2020 15:18:18 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ff440e8b82b4c9259f2a88a84a41d816d004da15476589a1a0206573136e6`  
		Last Modified: Wed, 13 May 2020 15:18:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7270c6d36f59c1f1600399bcae7d6ab3c6adacfda2df9546791b323c707445aa`  
		Last Modified: Wed, 13 May 2020 15:18:22 GMT  
		Size: 10.5 MB (10522664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180d2afa65f3a5a6c18059bc13eab2495a6c4174b20d42dbe9a1e180d5371eb1`  
		Last Modified: Wed, 13 May 2020 15:18:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094dd8b29c2718d588360f0c62f2ece6da8baf022903df8e5072101703e1c8da`  
		Last Modified: Wed, 13 May 2020 21:29:43 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d337a01745d934cd445f6bec34a0586fc7da01e44b1a44d63a6afb5fab56a71e`  
		Last Modified: Wed, 13 May 2020 21:29:48 GMT  
		Size: 6.2 MB (6151454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906019d19f9bcd6484ecc50bdce9df198f4ef6aa4e25422f15df3ed44100dca`  
		Last Modified: Wed, 13 May 2020 21:29:42 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

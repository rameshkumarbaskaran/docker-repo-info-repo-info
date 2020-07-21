## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:05e1e160bdd91cbe090af9e9e00abf94fe398f342933165330712b8f882ee93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull hylang@sha256:72da18695142feb2fdf6d0f48fc0f303098cf162ab3c5b72527f8bc4b566ad33
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2383171992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e05b877adf41dda4312d135cdde6a53d486de64ba517ea69e6a1d31bfc8e63c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jul 2020 17:59:19 GMT
ENV PYTHON_VERSION=3.8.5
# Tue, 21 Jul 2020 17:59:20 GMT
ENV PYTHON_RELEASE=3.8.5
# Tue, 21 Jul 2020 18:01:13 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 18:01:15 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Tue, 21 Jul 2020 18:01:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Tue, 21 Jul 2020 18:01:18 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Tue, 21 Jul 2020 18:02:14 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 21 Jul 2020 18:02:15 GMT
CMD ["python"]
# Tue, 21 Jul 2020 18:22:22 GMT
ENV HY_VERSION=0.19.0
# Tue, 21 Jul 2020 18:23:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 21 Jul 2020 18:23:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c52a6ec89baf38b2adeff80bfedafe024701e7afd8c0d9f44beb3d7a900390b`  
		Last Modified: Tue, 21 Jul 2020 18:05:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abfc904f19103a80691c36bf6b6a1eebecc64f238c52d63bf3f4d8ec0b01d0e`  
		Last Modified: Tue, 21 Jul 2020 18:05:37 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a38f858f03e608b81eb40402577a50cc276491287658a339ee703ac9df59f8`  
		Last Modified: Tue, 21 Jul 2020 18:05:47 GMT  
		Size: 57.2 MB (57214214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a67e24ea51446e663427a202060c67251d05403becbb3ae46b306e93fd080e`  
		Last Modified: Tue, 21 Jul 2020 18:05:35 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d11882edd2a077788cea57afd5f4adb18c242968f7fc1ba9e95d795c094c9e`  
		Last Modified: Tue, 21 Jul 2020 18:05:34 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a5849bc20f17269a2d9534a4bf6c91c532fed73a6f32043fc8303f52cd1388`  
		Last Modified: Tue, 21 Jul 2020 18:05:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a615582fb7878c80746776335fd5aeabb4b54d5eb81946b3e56664c9fe3242c`  
		Last Modified: Tue, 21 Jul 2020 18:05:46 GMT  
		Size: 10.2 MB (10234845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98c2242cb6ea6a4d2d32e8fbf63be7e635e5ef49e656dee5ed6915274305a84`  
		Last Modified: Tue, 21 Jul 2020 18:05:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9a7cd5099e0da61940ec22257695d1631abc5495177873b3460f42823bfc7`  
		Last Modified: Tue, 21 Jul 2020 18:28:03 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bd7d886c067dda261f0b1060077262d1cc6dfa179952d61cb12047e5e1ebfa`  
		Last Modified: Tue, 21 Jul 2020 18:28:09 GMT  
		Size: 5.5 MB (5520318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd53b7375454edde75891f190fa41533e81e5ba67a60bc70fcea42cfa734df13`  
		Last Modified: Tue, 21 Jul 2020 18:28:02 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `hylang:python3.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:485c4398b7d9f1a13085512f81b78df46f8543ea59ecbc0d7726e308145938ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `hylang:python3.7-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull hylang@sha256:eaf64512d52bdccbcc5e5f317f0ad409c568c24a88517f9e5d18d1c9ac45a82a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328047296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01986e2a84479959874e218fe55a221d63a1c641e8a7ff406ab4faae9c2e8ac7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Tue, 14 Apr 2020 21:32:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 17:15:58 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 15 Apr 2020 17:15:59 GMT
ENV PYTHON_RELEASE=3.7.7
# Wed, 15 Apr 2020 17:17:34 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 15 Apr 2020 17:17:35 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 15 Apr 2020 17:17:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 15 Apr 2020 17:17:38 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 15 Apr 2020 17:18:19 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 15 Apr 2020 17:18:20 GMT
CMD ["python"]
# Wed, 15 Apr 2020 21:24:03 GMT
ENV HY_VERSION=0.18.0
# Wed, 15 Apr 2020 21:24:37 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 15 Apr 2020 21:24:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edc29de224149bd438350512f7a31a67edbd3fcafce757aa60620dc459c184ad`  
		Last Modified: Tue, 14 Apr 2020 22:15:56 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b562599961df718e05ccbf1159be085db8c901f1016b3499096d89fc02712ffa`  
		Last Modified: Wed, 15 Apr 2020 17:28:30 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44041a0ecfef9920517a388bf1b208848353482531cfe09592074d716d2fdfe9`  
		Last Modified: Wed, 15 Apr 2020 17:28:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a717d414041f4e425ca15b6ad8af67a1926c43ccf9ed55d401f7fb9ed245d790`  
		Last Modified: Wed, 15 Apr 2020 17:28:37 GMT  
		Size: 50.9 MB (50891926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8f11e2a49afdcedf6bcd2b89bc4284004c98c0aab15de4dc655a06f31e81f5`  
		Last Modified: Wed, 15 Apr 2020 17:28:27 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9bd1b245aadb55c66414eea16b68822304803d536710ff642b53809b6ca04e`  
		Last Modified: Wed, 15 Apr 2020 17:28:28 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9901a38b3416270af6d21408d18ae79e89cf2bafc4cb991d82ab835eb8d509cf`  
		Last Modified: Wed, 15 Apr 2020 17:28:27 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c26ec7dfeb04657a3d713123579a7ed893f17c306aece85dcc63bb890cccf`  
		Last Modified: Wed, 15 Apr 2020 17:28:29 GMT  
		Size: 5.3 MB (5317149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96821d77409f7f996993f108310c98255d2608bea34da0e50b6c5bad6437ce9`  
		Last Modified: Wed, 15 Apr 2020 17:28:27 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03fb3a1cc8bd061e1912d2e8fad0796acae6a6faf81a37a335ee81c3db7381`  
		Last Modified: Wed, 15 Apr 2020 21:27:51 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138c6e1719d74ea724d0d4747b73487ca1486c09c4196c6587af97af8dfede11`  
		Last Modified: Wed, 15 Apr 2020 21:27:52 GMT  
		Size: 1.1 MB (1120823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882e5521958b415b1d983381b91e81be3a4e43b50a319f9c9d3c744f9c26765`  
		Last Modified: Wed, 15 Apr 2020 21:27:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

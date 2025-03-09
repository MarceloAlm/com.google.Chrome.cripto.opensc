# com.google.Chrome.pki.opensc
This extension provides support for the OpenSC compatible tokens in Google Chrome. It includes the necessary libraries for communication with the token and its dependencies.

To use this extension, ensure that the Google Chrome Flatpak is installed and that you have a compatible token. The tokens will be loaded by the p11-kit-proxy.so library. In case of issues, verify that the pcscd service is running on the host system (recommended version 2.3.0).

## Instalation (testing branch)
Install the pre-requisites and the compatible testing branch of com.google.Chrome (https://github.com/flathub/com.google.Chrome/pull/378):

``` bash
flatpak install --user -y org.flatpak.Builder
flatpak install --user https://dl.flathub.org/build-repo/168688/com.google.Chrome.flatpakref
```
Clone the repository:
``` bash
git clone https://github.com/MarceloAlm/com.google.Chrome.opensc.git
cd com.google.Chrome.opensc/
```

Build:
``` bash
flatpak run org.flatpak.Builder --install --force-clean --user --install-deps-from=flathub --repo=.local-repo _build  com.google.Chrome.pki.opensc.yaml
```
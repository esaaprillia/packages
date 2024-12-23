include $(TOPDIR)/rules.mk

PKG_NAME:=python-homeassistant
PKG_VERSION:=2024.12.5
PKG_RELEASE:=1

PKG_MAINTAINER:=Andy Syam <privasisource@gmail.com>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE.md

PYPI_NAME:=homeassistant
PKG_HASH:=3df79d8a02561cbbf606a1ce81579d0f2271c714a67477b60af3cd6025a2e9a0

PKG_BUILD_DEPENDS:=python3/host python-build/host python-installer/host python-wheel/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-homeassistant
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Open-source home automation platform running on Python 3.
  URL:=https://www.home-assistant.io/
  DEPENDS:=+python3 +python3-asyncio +python3-codecs +python3-ctypes +python3-dbm +python3-decimal +python3-email +python3-logging +python3-lzma +python3-multiprocessing +python3-ncurses +python3-openssl +python3-pydoc +python3-readline +python3-sqlite3 +python3-unittest +python3-urllib +python3-uuid +python3-venv +python3-webbrowser +python3-xml +python3-aiodns +python3-aiohasupervisor +python3-aiohttp +python3-aiohttp-cors +python3-aiohttp-fast-zlib +python3-aiozoneinfo +python3-aioesphomeapi +python3-astral +python3-async-interrupt +python3-attrs +python3-atomicwrites-homeassistant +python3-audioop-lts +python3-awesomeversion +python3-bcrypt +python3-certifi +python3-ciso8601 +python3-fnv-hash-fast +python3-hass-nabucasa +python3-httpx +python3-home-assistant-bluetooth +python3-ifaddr +python3-jinja2 +python3-lru-dict +python3-pyjwt +python3-cryptography +python3-pillow +python3-propcache +python3-pyopenssl +python3-orjson +python3-packaging +python3-psutil-home-assistant +python3-slugify +python3-yaml +python3-requests +python3-securetar +python3-sqlalchemy +python3-standard-aifc +python3-standard-telnetlib +python3-typing-extensions +python3-ulid-transform +python3-urllib3 +python3-uv +python3-voluptuous +python3-voluptuous-serialize +python3-voluptuous-openapi +python3-yarl +python3-webrtc-models +python3-home-assistant-frontend  +python3-async-upnp-client +python3-hassil +python3-aiodhcpwatcher +python3-pyserial +python3-aiodiscover +python3-pymicro-vad +python3-pyspeex-noise +python3-ha-ffmpeg +python3-av +python3-go2rtc-client +python3-pyturbojpeg +python3-pyudev +python3-home-assistant-intents +python3-mutagen +python3-pynacl +python3-pymetno +python3-gtts +python3-radios +python3-matter-server +python3-pyqrcode +python3-pyotp +python3-numpy +python3-watchdog +python3-ical
endef

define Package/python3-homeassistant/description
Open source home automation that puts local control and privacy first. Powered by a worldwide community of tinkerers and DIY enthusiasts. Perfect to run on a Raspberry Pi or a local server.
endef

$(eval $(call Py3Package,python3-homeassistant))
$(eval $(call BuildPackage,python3-homeassistant))
$(eval $(call BuildPackage,python3-homeassistant-src))

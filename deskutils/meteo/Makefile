# $FreeBSD$

PORTNAME=	meteo
PORTVERSION=	0.9.7
PORTREVISION=	1
CATEGORIES=	deskutils

MAINTAINER=	tagattie@yandex.com
COMMENT=	Weather forecast application using OpenWeatherMap API

LICENSE=	GPLv3+
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	appstream-util:devel/appstream-glib \
		valac:lang/vala
LIB_DEPENDS=	libappindicator3.so:devel/libappindicator \
		libjson-glib-1.0.so:devel/json-glib \
		libsoup-2.4.so:devel/libsoup \
		libgeocode-glib.so:net/geocode-glib \
		libwebkit2gtk-4.0.so:www/webkit2-gtk3

USES=		compiler:c11 desktop-file-utils gettext gnome meson pkgconfig \
		python:3.5+,build shebangfix

USE_GITLAB=	yes
GL_ACCOUNT=	bitseater
GL_COMMIT=	c83cea9a31901911ed5f8d87756d33a36b547457

USE_GNOME=	gtk30

SHEBANG_FILES=	meson/post_install.py

GLIB_SCHEMAS=	com.gitlab.bitseater.meteo.gschema.xml
INSTALLS_ICONS=	yes

PORTDOCS=	AUTHORS CONTRIBUTING.md CREDITS.md README.md changelog

OPTIONS_DEFINE=	DOCS

post-extract:
	@${MV} ${WRKSRC}/debian/changelog ${WRKSRC}

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_MAN} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>

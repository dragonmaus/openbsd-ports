# $OpenBSD: Makefile,v 1.36 2020/07/03 21:12:58 sthen Exp $

COMMENT=		automatic color temperature adjustment

V=			1.12
PKGNAME=		redshift-console-${V}
DISTNAME=		redshift-${V}

CATEGORIES=		misc graphics

HOMEPAGE=		http://jonls.dk/redshift/

# GPLv3
PERMIT_PACKAGE=		Yes

WANTLIB=		X11 Xau Xdmcp Xext Xxf86vm c drm m xcb xcb-randr

MASTER_SITES=		https://github.com/jonls/redshift/releases/download/v${V}/
EXTRACT_SUFX=		.tar.xz

BUILD_DEPENDS=		devel/gettext,-tools textproc/intltool

SEPARATE_BUILD=		Yes
USE_GMAKE=		Yes
COMPILER=		base-gcc ports-gcc

CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS=		CC=cc \
			GCC=cc \
			--disable-apparmor \
			--disable-corelocation \
			--disable-geoclue2 \
			--disable-gui \
			--disable-nls \
			--disable-ubuntu

.include <bsd.port.mk>

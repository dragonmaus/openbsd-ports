# $OpenBSD: Makefile,v 1.10 2020/07/17 08:36:04 tb Exp $

ONLY_FOR_ARCHS =	${APM_ARCHS}

COMMENT =		dwm status bar statistics

V =			0.7
PKGNAME =		dstat-custom-${V}
DISTNAME =		dstat-${V}

CATEGORIES =		x11 sysutils

HOMEPAGE =		https://www.umaxx.net/

MAINTAINER =		Joerg Jung <jung@openbsd.org>

# ISC
PERMIT_PACKAGE =	Yes

WANTLIB =		X11 c util

MASTER_SITES =		${HOMEPAGE}/dl/

MAKE_FLAGS =		CC="${CC}"
MAKE_ENV =		LDFLAGS="${LDFLAGS}"
FAKE_FLAGS =		DESTDIR=""

NO_TEST =		Yes

.include <bsd.port.mk>

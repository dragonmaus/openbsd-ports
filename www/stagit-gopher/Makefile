# $OpenBSD: Makefile,v 1.13 2020/08/27 13:55:39 fcambus Exp $

COMMENT =		static git page generator for gopher

DISTNAME =		stagit-gopher-0.9.4

CATEGORIES =		www

HOMEPAGE =		https://codemadness.org/

MAINTAINER =		Hiltjo Posthuma <hiltjo@codemadness.org>

# MIT/X Consortium License
PERMIT_PACKAGE =	Yes

# uses pledge()
# uses unveil()
WANTLIB =		c git2

LIB_DEPENDS =		devel/libgit2/libgit2>=0.22

RUN_DEPENDS =		net/geomyidae

MASTER_SITES =		https://codemadness.org/releases/stagit-gopher/

MAKE_FLAGS =		CC='${CC}' \
			CFLAGS='${CFLAGS}' \
			LDFLAGS='${LDFLAGS}' \
			LIBGIT_INC='-I${LOCALBASE}/include' \
			LIBGIT_LIB='-L${LOCALBASE}/lib -lgit2' \
			COMPATOBJ=''

NO_TEST =		Yes

EXAMPLESDIR =		${PREFIX}/share/examples/stagit-gopher

post-install:
	${INSTALL_DATA_DIR} ${EXAMPLESDIR}/
	mv ${PREFIX}/share/doc/stagit-gopher/example_*.sh ${EXAMPLESDIR}/

.include <bsd.port.mk>

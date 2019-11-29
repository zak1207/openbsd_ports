# $OpenBSD: Makefile,v 1.27 2019/06/29 14:05:19 edd Exp $

COMMENT =	UDP-to-HTTP multicast traffic relay daemon

V =		1.0-24.1
DISTNAME =	udpxy-1.0.24.1
DISTFILES =	${V}${EXTRACT_SUFX}

CATEGORIES =	net
HOMEPAGE =	https://udpxy.net/

MAINTAINER =	Alexander Zotov <https://t.me/openbsd86>

# MPL 2.0
PERMIT_PACKAGE = Yes

WANTLIB += c

GH_ACCOUNT =	pcherenkov
GH_PROJECT =	udpxy
GH_COMMIT =	db6e88ac4281e8e5c6c0a1a5e3f444e9b544b83b

WRKDIST =		${WRKDIR}/udpxy-${V}/chipmunk
EXTRACT_SUFX =		.tar.gz

USE_GMAKE =		Yes

ALL_TARGET =		release

NO_TEST =	Yes

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/udpxy ${PREFIX}/bin/
	${INSTALL_PROGRAM} ${WRKSRC}/udpxrec ${PREFIX}/bin/
	${INSTALL_DATA} ${WRKSRC}/doc/en/*.1 ${PREFIX}/man/man1/

.include <bsd.port.mk>

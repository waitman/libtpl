# Created by: "Waitman Gobble" <waitman@waitman.net>
# $FreeBSD$

PORTNAME=	tpl
PORTVERSION=	1.6
CATEGORIES=	devel
MASTER_SITES=	GH

COMMENT=	Efficient serialization in C

LICENSE=        BSD
LICENSE_FILE=   ${WRKSRC}/LICENSE

USE_GITHUB=     yes
GH_ACCOUNT=     waitman
GH_TAGNAME=     ${GH_COMMIT}
GH_COMMIT=      9116c7c

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+= --enable-shared

PORTDOCS=	ChangeLog.txt examples.txt userguide.txt compiling.txt
PLIST_FILES= 	include/tpl.h lib/libtpl.la lib/libtpl.so.0 lib/libtpl.so lib/libtpl.a

.include <bsd.port.options.mk>

post-install:
.if ${PORT_OPTIONS:MDOCS}
	@${MKDIR} ${DOCSDIR}
.for f in ${PORTDOCS}
	@${INSTALL_DATA} ${WRKSRC}/doc/${f} ${DOCSDIR}
.endfor
.endif

.include <bsd.port.mk>

# Created by: ijliao
# $FreeBSD$

PORTNAME=	csstidy
PORTVERSION=	1.4
CATEGORIES=	www
MASTER_SITES=	SF/${PORTNAME}/CSSTidy%20%28C%2B%2B%2C%20stable%29/1.3
DISTNAME=	${PORTNAME}-source-${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Opensource CSS parser and optimiser

LICENSE=	GPLv2

USES=		zip
WRKSRC=		${WRKDIR}/${PORTNAME}
OPTIONS_DEFINE=	DOCS

PLIST_FILES=	bin/csstidy
PORTDOCS=	AUTHORS BUGS COPYING ChangeLog NEWS README TODO

do-build:
	${CXX} ${CXXFLAGS} ${LDFLAGS} -o ${WRKSRC}/${PORTNAME} ${WRKSRC}/*.cpp

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:C|^|${WRKDIR}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>

# $FreeBSD$

PORTNAME=	lokalize
PORTVERSION=	${KDE4_VERSION}
CATEGORIES=	devel kde kde-kde4

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Computer-aided translation system

LIB_DEPENDS=	libhunspell-1.3.so:textproc/hunspell

USES=		cmake:outsource kde:4 tar:xz
USE_KDE=	kdelibs automoc4
USE_QT4=	moc_build qmake_build rcc_build uic_build \
		sql

.include <bsd.port.mk>

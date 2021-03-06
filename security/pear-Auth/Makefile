# Created by: Thierry Thomas (<thierry@pompo.net>)
# $FreeBSD$

PORTNAME=	Auth
PORTVERSION=	1.6.4
CATEGORIES=	security pear

MAINTAINER=	joneum@bsdproject.de
COMMENT=	PEAR class for creating an authentication system

USES=	pear

OPTIONS_DEFINE=	PEAR_LOG PEAR_FILE_PASSWD PEAR_NET_POP3 PEAR_DB PEAR_MDB \
		PEAR_MDB2 PEAR_AUTH_RADIUS PEAR_CRYPT_CHAP PEAR_FILE_SMBPASSWD \
		PEAR_SOAP PEAR_NET_VPOPMAILD
PEAR_LOG_DESC=	PEAR::Log support
PEAR_FILE_PASSWD_DESC=	PEAR::File_Passwd support
PEAR_NET_POP3_DESC=	PEAR::Net_POP3 support
PEAR_DB_DESC=	PEAR::DB support
PEAR_MDB_DESC=	PEAR::MDB support
PEAR_MDB2_DESC=	PEAR::MDB2 support
PEAR_AUTH_RADIUS_DESC=	PEAR::AUTH_RADIUS support
PEAR_CRYPT_CHAP_DESC=	PEAR::CRYPT_CHAP support
PEAR_FILE_SMBPASSWD_DESC=	PEAR::File_SMBPasswd support
PEAR_SOAP_DESC=	PEAR::SOAP support
PEAR_NET_VPOPMAILD_DESC=	PEAR::Net_Vpopmaild support

PEAR_LOG_RUN_DEPENDS=	${PEARDIR}/Log/syslog.php:sysutils/pear-Log
PEAR_FILE_PASSWD_RUN_DEPENDS=	${PEARDIR}/File/Passwd.php:security/pear-File_Passwd
PEAR_CRYPT_CHAP_RUN_DEPENDS=	${PEARDIR}/Crypt/CHAP.php:security/pear-Crypt_CHAP
PEAR_NET_POP3_RUN_DEPENDS=	${PEARDIR}/Net/POP3.php:net/pear-Net_POP3
PEAR_DB_RUN_DEPENDS=	${PEARDIR}/DB.php:databases/pear-DB
PEAR_MDB_RUN_DEPENDS=	${PEARDIR}/MDB.php:databases/pear-MDB
PEAR_MDB2_RUN_DEPENDS=	${PEARDIR}/MDB2.php:databases/pear-MDB2
PEAR_AUTH_RADIUS_RUN_DEPENDS=	${PEARDIR}/Auth/RADIUS.php:net/pear-Auth_RADIUS
PEAR_FILE_SMBPASSWD_RUN_DEPENDS=	${PEARDIR}/File/SMBPasswd.php:security/pear-File_SMBPasswd
PEAR_SOAP_RUN_DEPENDS=	${PEARDIR}/SOAP/Base.php:net/pear-SOAP
PEAR_NET_VPOPMAILD_RUN_DEPENDS=	${PEARDIR}/Net/Vpopmaild.php:net/pear-Net_Vpopmaild

post-extract:
	@${REINPLACE_CMD} -e "s|@version@|${PORTVERSION}|" ${WRKSRC}/Auth.php

.include <bsd.port.mk>

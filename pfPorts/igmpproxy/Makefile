# New ports collection makefile for:  igmpproxy
# Date created:        5 January 2009
# Whom:                asami
#
# $FreeBSD$
#

PORTNAME=       igmpproxy
PORTVERSION=    0.1
#PORTREVISION=  2
CATEGORIES=     net
MASTER_SITES=   ${MASTER_SITE_SOURCEFORGE}
MASTER_SITE_SUBDIR=     ${PORTNAME}/${PORTNAME}/${PORTVERSION}-beta2
DISTNAME=       ${PORTNAME}-src-${PORTVERSION}-beta2

MAINTAINER=     melifaro@ipfw.ru
COMMENT=        Multicast router utilizing IGMP forwarding

HOMEPAGE=       http://igmpproxy.sourceforge.net/
WRKSRC=         ${WRKDIR}/igmpproxy/src

MAN5=           igmpproxy.conf.5
MAN8=           igmpproxy.8

PLIST_FILES=    sbin/igmpproxy \
                etc/igmpproxy.conf.sample \
                etc/rc.d/igmpproxy

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/igmpproxy ${PREFIX}/sbin
	${INSTALL_MAN} ${WRKSRC}/../doc/igmpproxy.8 ${PREFIX}/man/man8
	${INSTALL_MAN} ${WRKSRC}/../doc/igmpproxy.conf.5 ${PREFIX}/man/man5
	${INSTALL_DATA} ${WRKSRC}/igmpproxy.conf ${PREFIX}/etc/igmpproxy.conf.sample
	${INSTALL_SCRIPT} ${FILESDIR}/igmpproxy ${PREFIX}/etc/rc.d

.include <bsd.port.mk>

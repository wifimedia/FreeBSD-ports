# Created by: Matthias Petermann <matthias@petermann-it.de>
# $FreeBSD$

PORTNAME=	trytond28_calendar
PORTVERSION=	2.8.2
PORTREVISION=	2
CATEGORIES=	finance python
MASTER_SITES=	CHEESESHOP \
		http://downloads-cdn.tryton.org/${PORTVERSION:R}/
DISTNAME=	trytond_calendar-${PORTVERSION}

MAINTAINER=	matthias@petermann-it.de
COMMENT=	Tryton Application Platform (Calendar Module)

LICENSE=	GPLv3

RUN_DEPENDS=	trytond28>=2.8.2:finance/trytond28 \
		${PYTHON_PKGNAMEPREFIX}vobject>=0.8.1:deskutils/py-vobject@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}PyWebDAV>=0:www/py-pywebdav@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pytz>=0:devel/py-pytz@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}dateutil>=1.5:devel/py-dateutil@${PY_FLAVOR}

CONFLICTS=	trytond_calendar-2.[46].*

USES=		python:2.7
USE_PYTHON=	distutils autoplist

.include <bsd.port.mk>

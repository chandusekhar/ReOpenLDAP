# Makefile.in for overlays
## $ReOpenLDAP$
## Copyright (c) 2015,2016 Leonid Yuriev <leo@yuriev.ru>.
## Copyright (c) 2015,2016 Peter-Service R&D LLC <http://billing.ru/>.
##
## This file is part of ReOpenLDAP.
##
## ReOpenLDAP is free software; you can redistribute it and/or modify it under
## the terms of the GNU Affero General Public License as published by
## the Free Software Foundation; either version 3 of the License, or
## (at your option) any later version.
##
## ReOpenLDAP is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU Affero General Public License for more details.
##
## You should have received a copy of the GNU Affero General Public License
## along with this program.  If not, see <http://www.gnu.org/licenses/>.
##

noinst_LTLIBRARIES = liboverlays_builtin.la
pkglib_LTLIBRARIES =
BUILT_SOURCES =
EXTRA_DIST = README

AM_CPPFLAGS = -DSLAPD_IMPORT -I$(srcdir)/.. -I$(top_srcdir)/include
liboverlays_builtin_la_SOURCES = overlays.c

if BEHIND_CURTIAN

BUILT_SOURCES += accesslog_banner.c auditlog_banner.c \
	collect_banner.c valsort_banner.c constraint_banner.c \
	dds_banner.c deref_banner.c dyngroup_banner.c dynlist_banner.c \
	memberof_banner.c ppolicy_banner.c pcache_banner.c \
	refint_banner.c retcode_banner.c rwm_banner.c seqmod_banner.c \
	sssvlv_banner.c syncprov_banner.c translucent_banner.c
	unique_banner.c

accesslog_banner.c: Makefile
	$(MKBANNER) --name overlay_accesslog --global 'overlay-accesslog' > $@
auditlog_banner.c: Makefile
	$(MKBANNER) --name overlay_auditlog --global 'overlay-auditlog' > $@
collect_banner.c: Makefile
	$(MKBANNER) --name overlay_collect --global 'overlay-collect' > $@
valsort_banner.c: Makefile
	$(MKBANNER) --name overlay_valsort --global 'overlay-valsort' > $@
constraint_banner.c: Makefile
	$(MKBANNER) --name overlay_constraint --global 'overlay-constraint' > $@
dds_banner.c: Makefile
	$(MKBANNER) --name overlay_dds --global 'overlay-dds' > $@
deref_banner.c: Makefile
	$(MKBANNER) --name overlay_deref --global 'overlay-deref' > $@
dyngroup_banner.c: Makefile
	$(MKBANNER) --name overlay_dyngroup --global 'overlay-dyngroup' > $@
dynlist_banner.c: Makefile
	$(MKBANNER) --name overlay_dynlist --global 'overlay-dynlist' > $@
memberof_banner.c: Makefile
	$(MKBANNER) --name overlay_memberof --global 'overlay-memberof' > $@
ppolicy_banner.c: Makefile
	$(MKBANNER) --name overlay_ppolicy --global 'overlay-ppolicy' > $@
pcache_banner.c: Makefile
	$(MKBANNER) --name overlay_pcache --global 'overlay-pcache' > $@
refint_banner.c: Makefile
	$(MKBANNER) --name overlay_refint --global 'overlay-refint' > $@
retcode_banner.c: Makefile
	$(MKBANNER) --name overlay_retcode --global 'overlay-retcode' > $@
rwm_banner.c: Makefile
	$(MKBANNER) --name overlay_rwm --global 'overlay-rwm' > $@
seqmod_banner.c: Makefile
	$(MKBANNER) --name overlay_seqmod --global 'overlay-seqmod' > $@
sssvlv_banner.c: Makefile
	$(MKBANNER) --name overlay_sssvlv --global 'overlay-sssvlv' > $@
syncprov_banner.c: Makefile
	$(MKBANNER) --name overlay_syncprov --global 'overlay-syncprov' > $@
translucent_banner.c: Makefile
	$(MKBANNER) --name overlay_translucent --global 'overlay-translucent' > $@
unique_banner.c: Makefile
	$(MKBANNER) --name overlay_unique --global 'overlay-unique' > $@
endif

if BUILD_ACCESSLOG
if ACCESSLOG_DYNAMIC
pkglib_LTLIBRARIES += accesslog.la
accesslog_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
accesslog_la_SOURCES = accesslog.c accesslog_banner.c
else
liboverlays_builtin_la_SOURCES += accesslog.c
endif
endif

if BUILD_AUDITLOG
if AUDITLOG_DYNAMIC
pkglib_LTLIBRARIES += auditlog.la
auditlog_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
auditlog_la_SOURCES = auditlog.c auditlog_banner.c
else
liboverlays_builtin_la_SOURCES += auditlog.c
endif
endif

if BUILD_COLLECT
if COLLECT_DYNAMIC
pkglib_LTLIBRARIES += collect.la
collect_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
collect_la_SOURCES = collect.c collect_banner.c
else
liboverlays_builtin_la_SOURCES += collect.c
endif
endif

if BUILD_CONSTRAINT
if CONSTRAINT_DYNAMIC
pkglib_LTLIBRARIES += constraint.la
constraint_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
constraint_la_SOURCES = constraint.c constraint_banner.c
else
liboverlays_builtin_la_SOURCES += constraint.c
endif
endif

if BUILD_DDS
if DDS_DYNAMIC
pkglib_LTLIBRARIES += dds.la
dds_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
dds_la_SOURCES = dds.c dds_banner.c
else
liboverlays_builtin_la_SOURCES += dds.c
endif
endif

if BUILD_DEREF
if DEREF_DYNAMIC
pkglib_LTLIBRARIES += deref.la
deref_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
deref_la_SOURCES = deref.c deref_banner.c
else
liboverlays_builtin_la_SOURCES += deref.c
endif
endif

if BUILD_DYNGROUP
if DYNGROUP_DYNAMIC
pkglib_LTLIBRARIES += dyngroup.la
dyngroup_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
dyngroup_la_SOURCES = dyngroup.c dyngroup_banner.c
else
liboverlays_builtin_la_SOURCES += dyngroup.c
endif
endif

if BUILD_DYNLIST
if DYNLIST_DYNAMIC
pkglib_LTLIBRARIES += dynlist.la
dynlist_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
dynlist_la_SOURCES = dynlist.c dynlist_banner.c
else
liboverlays_builtin_la_SOURCES += dynlist.c
endif
endif

if BUILD_MEMBEROF
if MEMBEROF_DYNAMIC
pkglib_LTLIBRARIES += memberof.la
memberof_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
memberof_la_SOURCES = memberof.c memberof_banner.c
else
liboverlays_builtin_la_SOURCES += memberof.c
endif
endif

if BUILD_PPOLICY
if PPOLICY_DYNAMIC
pkglib_LTLIBRARIES += ppolicy.la
ppolicy_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
ppolicy_la_SOURCES = ppolicy.c ppolicy_banner.c
else
liboverlays_builtin_la_SOURCES += ppolicy.c
endif
endif

if BUILD_PCACHE
if PCACHE_DYNAMIC
pkglib_LTLIBRARIES += pcache.la
pcache_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION) \
	-weak proxycache.la
pcache_la_SOURCES = pcache.c pcache_banner.c
else
liboverlays_builtin_la_SOURCES += pcache.c
endif
endif

if BUILD_REFINT
if REFINT_DYNAMIC
pkglib_LTLIBRARIES += refint.la
refint_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
refint_la_SOURCES = refint.c refint_banner.c
else
liboverlays_builtin_la_SOURCES += refint.c
endif
endif

if BUILD_RETCODE
if RETCODE_DYNAMIC
pkglib_LTLIBRARIES += retcode.la
retcode_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
retcode_la_SOURCES = retcode.c retcode_banner.c
else
liboverlays_builtin_la_SOURCES += retcode.c
endif
endif

if BUILD_RWM
if RWM_DYNAMIC
pkglib_LTLIBRARIES += rwm.la
rwm_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
rwm_la_SOURCES = rwm_banner.c rwm.c rwmconf.c rwmdn.c rwm.h rwmmap.c
else
liboverlays_builtin_la_SOURCES += rwm_banner.c rwm.c rwmconf.c rwmdn.c rwm.h rwmmap.c
endif
endif

if BUILD_SEQMOD
if SEQMOD_DYNAMIC
pkglib_LTLIBRARIES += seqmod.la
seqmod_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
seqmod_la_SOURCES = seqmod.c seqmod_banner.c
else
liboverlays_builtin_la_SOURCES += seqmod.c
endif
endif

if BUILD_SSSVLV
if SSSVLV_DYNAMIC
pkglib_LTLIBRARIES += sssvlv.la
sssvlv_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
sssvlv_la_SOURCES = sssvlv.c sssvlv_banner.c
else
liboverlays_builtin_la_SOURCES += sssvlv.c
endif
endif

if BUILD_SYNCPROV
if SYNCPROV_DYNAMIC
pkglib_LTLIBRARIES += syncprov.la
syncprov_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
syncprov_la_SOURCES = syncprov.c syncprov_banner.c
else
liboverlays_builtin_la_SOURCES += syncprov.c
endif
endif

if BUILD_TRANSLUCENT
if TRANSLUCENT_DYNAMIC
pkglib_LTLIBRARIES += translucent.la
translucent_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
translucent_la_SOURCES = translucent.c translucent_banner.c
else
liboverlays_builtin_la_SOURCES += translucent.c
endif
endif

if BUILD_UNIQUE
if UNIQUE_DYNAMIC
pkglib_LTLIBRARIES += unique.la
unique_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
unique_la_SOURCES = unique.c unique_banner.c
else
liboverlays_builtin_la_SOURCES += unique.c
endif
endif

if BUILD_VALSORT
if VALSORT_DYNAMIC
pkglib_LTLIBRARIES += valsort.la
valsort_la_LDFLAGS = -module -export-dynamic \
	-release $(API_LIB_RELEASE) -version-info $(API_LIB_VERSION)
valsort_la_SOURCES = valsort.c valsort_banner.c
else
liboverlays_builtin_la_SOURCES += valsort.c
endif
endif
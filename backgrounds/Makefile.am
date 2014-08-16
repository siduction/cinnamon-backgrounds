backgrounddir = $(datadir)/backgrounds/cinnamon

background_DATA =\
	Blinds.jpg \
	Bokeh_Tails.jpg \
	Chmiri.jpg \
	Dark_Ivy.jpg \
	Fabric.jpg \
	Flowerbed.jpg \
	FootFall.png \
	Locked.jpg \
	Mirror.jpg \
	Road.jpg \
	Sandstone.jpg \
	Stones.jpg \
	Terraform-green.jpg \
	Waves.jpg \
	Whispy_Tails.jpg

metadata_in_files = cinnamon-backgrounds.xml.in
metadatadir = $(datadir)/cinnamon-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)
@INTLTOOL_XML_RULE@

noinst_DATA = cinnamon-backgrounds.xml.in
CLEANFILES = cinnamon-backgrounds.xml cinnamon-backgrounds.xml.in

EXTRA_DIST = $(background_DATA) cinnamon-backgrounds.xml.in.in

edit = sed \
	-e 's|@BACKGROUNDDIR[@]|$(backgrounddir)|g'

cinnamon-backgrounds.xml.in: cinnamon-backgrounds.xml.in.in Makefile
	$(edit) $< >$@

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk

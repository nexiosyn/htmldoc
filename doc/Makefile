#
# "$Id: Makefile,v 1.2 1999/11/11 17:10:37 mike Exp $"
#
#   Makefile for HTMLDOC documentation files.
#
#   Copyright 1997-1999 by Easy Software Products.
#
#   These coded instructions, statements, and computer programs are the
#   property of Easy Software Products and are protected by Federal
#   copyright law.  Distribution and use rights are outlined in the file
#   "COPYING.txt" which should have been included with this file.  If this
#   file is missing or damaged please contact Easy Software Products
#   at:
#
#       Attn: ESP Licensing Information
#       Easy Software Products
#       44141 Airport View Drive, Suite 204
#       Hollywood, Maryland 20636-3111 USA
#
#       Voice: (301) 373-9600
#       EMail: info@easysw.com
#         WWW: http://www.easysw.com
#

#
# Include common definitions...
#

include ../Makedefs


#
# Documentation files...
#

SOURCES	=	intro.html 1-compiling.html 2-guidelines.html \
		3-gui.html 4-cmdline.html 5-cgi.html \
		a-limits.html b-license.html

DOCUMENTS =	htmldoc.html htmldoc.pdf htmldoc.ps
DOCFILES =	htmldoc.html htmldoc.pdf htmldoc.ps \
		htmldoc-colors.gif htmldoc-fonts.gif \
		htmldoc-input.gif htmldoc-options.gif \
		htmldoc-output.gif htmldoc-page.gif \
		htmldoc-startmenu.gif htmldoc-toc.gif \
		htmldoc.gif


#
# Make everything...
#

all: $(DOCUMENTS)


#
# Install everything...
#

install: $(DOCUMENTS)
	$(MKDIR) $(datadir)/doc/htmldoc
	$(CP) $(DOCFILES) $(datadir)/doc/htmldoc
	$(CHMOD) ugo+r $(datadir)/doc/htmldoc/*
	$(MKDIR) $(mandir)/man1
	$(CP) htmldoc.man $(mandir)/man1/htmldoc.1
	$(CHMOD) ugo+r $(mandir)/man1/htmldoc.1
	$(MKDIR) $(mandir)/cat1
	$(CP) htmldoc.1 $(mandir)/cat1/htmldoc.1
	$(CHMOD) ugo+r $(mandir)/cat1/htmldoc.1


#
# Clean out document files...
#

clean:
	$(RM) $(DOCUMENTS)


#
# htmldoc.html
#

htmldoc.html:	$(SOURCES) ../htmldoc/htmldoc
	../htmldoc/htmldoc -v -f htmldoc.html --title htmldoc.gif \
		--datadir .. $(SOURCES)


#
# htmldoc.pdf
#

htmldoc.pdf:	$(SOURCES) ../htmldoc/htmldoc
	../htmldoc/htmldoc -v -f htmldoc.pdf --duplex --jpeg --compression=9 \
		--title htmldoc.png --datadir .. $(SOURCES)


#
# htmldoc.ps
#

htmldoc.ps:	$(SOURCES) ../htmldoc/htmldoc
	../htmldoc/htmldoc -v -f htmldoc.ps --duplex \
		--title htmldoc.png --datadir .. $(SOURCES)


#
# End of "$Id: Makefile,v 1.2 1999/11/11 17:10:37 mike Exp $".
#
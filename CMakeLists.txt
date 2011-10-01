#
# Basic settings
#
cmake_minimum_required (VERSION 2.6)
project (ibus-array)

INCLUDE(GNUInstallDirs)

#
# Checking essentional modules
#
FIND_PACKAGE(PkgConfig)
PKG_CHECK_MODULES(GTK2 REQUIRED gtk+-2.0)
PKG_CHECK_MODULES(GLIB REQUIRED glib-2.0)
PKG_CHECK_MODULES(IBUS REQUIRED ibus-1.0)
PKG_CHECK_MODULES(SQLITE3 REQUIRED sqlite3)

#
# Building
#
ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(data)
ADD_SUBDIRECTORY(icons)
ADD_SUBDIRECTORY(po)
ADD_SUBDIRECTORY(setup)
ADD_SUBDIRECTORY(tools)

#
# Installing
#

#
# Testing
#
ENABLE_TESTING()

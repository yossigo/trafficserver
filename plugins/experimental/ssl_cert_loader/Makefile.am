#  Licensed to the Apache Software Foundation (ASF) under one
#  or more contributor license agreements.  See the NOTICE file
#  distributed with this work for additional information
#  regarding copyright ownership.  The ASF licenses this file
#  to you under the Apache License, Version 2.0 (the
#  "License"); you may not use this file except in compliance
#  with the License.  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.

include $(top_srcdir)/build/plugins.mk

AM_CPPFLAGS += -I$(top_srcdir)/lib -I$(top_srcdir)/lib/ts

pkglib_LTLIBRARIES = ssl_cert_loader.la

ssl_cert_loader_la_SOURCES = ssl-cert-loader.cc domain-tree.cc
ssl_cert_loader_la_LDFLAGS = $(TS_PLUGIN_LD_FLAGS)
ssl_cert_loader_la_LIBADD = $(top_builddir)/lib/tsconfig/libtsconfig.la

include $(top_srcdir)/build/tidy.mk

tidy-local: $(DIST_SOURCES)
	$(CXX_Clang_Tidy)

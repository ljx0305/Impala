#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements. See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership. The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License. You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied. See the License for the
# specific language governing permissions and limitations
# under the License.
#

THRIFT = $(top_srcdir)/compiler/cpp/thrift

stubs: ../ConstantsDemo.thrift ../DebugProtoTest.thrift ../ThriftTest.thrift
	$(THRIFT) --gen hs ../ConstantsDemo.thrift
	$(THRIFT) --gen hs ../DebugProtoTest.thrift
	$(THRIFT) --gen hs ../ThriftTest.thrift

check: stubs
	sh run-test.sh ConstantsDemo
	sh run-test.sh DebugProtoTest
	sh run-test.sh ThriftTest

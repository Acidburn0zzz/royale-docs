---
# Licensed to the Apache Software Foundation (ASF) under one or more
# contributor license agreements.  See the NOTICE file distributed with
# this work for additional information regarding copyright ownership.
# The ASF licenses this file to You under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance with
# the License.  You may obtain a copy of the License at
# 
# http://www.apache.org/licenses/LICENSE-2.0
# 
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

layout: docpage
title: MXML
description: The declarative XML-based user interface markup language
permalink: /features/mxml
---

# MXML

The declarative XML-based user interface markup language

MXML is an XML language that you use, when building an application in Royale, to lay out user-interface components.

```mxml
<?xml version="1.0" encoding="utf-8"?>
<j:Group xmlns:fx="http://ns.adobe.com/mxml/2009" 
        xmlns:j="library://ns.apache.org/royale/jewel" 
        xmlns:html="library://ns.apache.org/royale/html">

    <fx:Script>
    <![CDATA[      
        private function clickHandler(event:MouseEvent):void {
            button.emphasis = (button.emphasis == Button.PRIMARY) ? "" : Button.PRIMARY;
        }
    ]]>
    </fx:Script>

    <j:Card width="600">
        <html:H3 text="items expand test"/>

        <j:HGroup itemsExpand="true" gap="3">
            <j:Button text="Hello" click="clickHandler(event)"/>
            <j:Button text="Apache"/>
            <j:Button text="Royale!!!!"/>
        </j:HGroup>
    </j:Card>
</j:Group>
```
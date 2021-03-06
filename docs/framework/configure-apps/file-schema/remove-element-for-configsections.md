---
title: "&lt;删除&gt;元素&lt;configSections&gt;"
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: article
f1_keywords: http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/remove
helpviewer_keywords:
- remove Element
- <remove> Element
ms.assetid: ae4d82e0-e8fe-468c-81ab-46d63c4d66a8
author: guardrex
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: bf2cb49fbeb01ad176a1d24d711cebc97ba14004
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="remove-element-for-configsections"></a>\<删除 > 元素\<configSections >

删除预定义的节或节组。

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;[**\<configSections >**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md)   
&nbsp;&nbsp;&nbsp;&nbsp;**\<删除 >**

## <a name="syntax"></a>语法

```xml
<remove name="section name or section group name" />
```

## <a name="attribute"></a>特性

|           | 描述 |
| --------- | ----------- |
| **name**  | 必需的特性。<br><br>指定的节或要删除的部分组的名称。 |

## <a name="parent-element"></a>父元素

|     | 描述 |
| --- | ----------- |
| [**\<configSections >**元素](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | 包含配置节和命名空间声明。 |

# <a name="child-elements"></a>子元素

无

## <a name="remarks"></a>备注

你可以使用**\<删除 >**元素从你在配置文件层次结构中较高级别定义的应用程序中删除节和节组。

## <a name="example"></a>示例

下面的示例演示如何使用**\<删除 >**删除先前在计算机配置文件中定义的节的应用程序配置文件中的元素。

下面的计算机配置文件代码声明部分 **\<sampleSection >**:

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

下面的应用程序配置文件代码移除 **\<sampleSection >**部分。 删除之后，应用程序无法检索中的设置 **\<sampleSection >**。

```xml
<!-- Application configuration file -->
<configuration>
  <configSections>
    <remove name="sampleSection"/>
  </configSections>
</configuration>
```

## <a name="configuration-file"></a>配置文件

此元素可在应用程序配置文件中，计算机配置文件 (*Machine.config*)，和*Web.config*不在应用程序的目录级别上的文件。

## <a name="see-also"></a>请参阅

[.NET Framework 的配置文件架构](~/docs/framework/configure-apps/file-schema/index.md)

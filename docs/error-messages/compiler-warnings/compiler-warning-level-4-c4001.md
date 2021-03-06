---
title: 编译器警告（等级4） C4001
ms.date: 11/04/2016
f1_keywords:
- C4001
helpviewer_keywords:
- C4001
ms.assetid: 414a47fe-d597-425e-9374-6a569231dc0a
ms.openlocfilehash: ceb7e65a292e5b9e9ef960ca9553183b703c93f0
ms.sourcegitcommit: 573b36b52b0de7be5cae309d45b68ac7ecf9a6d8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2019
ms.locfileid: "74991696"
---
# <a name="compiler-warning-level-4-c4001"></a>编译器警告（等级4） C4001

使用了非标准扩展 "单行注释"

> [!NOTE]
> Visual Studio 2017 版本15.5 中已删除此警告，因为单行注释在 C99 中是标准的。

单行注释在中是标准的C++ ，从 C99 开始是 C 标准。
在严格 ANSI 兼容性（[/za](../../build/reference/za-ze-disable-language-extensions.md)）下，包含单行注释的 C 文件将生成 C4001，因为使用了非标准扩展。 由于单行注释在中是标准的C++，因此，在通过 Microsoft 扩展（/ze）进行编译时，包含单行注释的 C 文件不会生成 C4001。

## <a name="example"></a>示例

若要禁用警告，请取消注释[#pragma 警告（禁用：4001）](../../preprocessor/warning.md)。

```cpp
// C4001.cpp
// compile with: /W4 /Za /TC
// #pragma warning(disable:4001)
int main()
{
   // single-line comment in main
   // C4001
}
```

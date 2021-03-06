---
title: /IMPLIB（命名导入库）
ms.date: 11/04/2016
f1_keywords:
- /implib
- VC.Project.VCLinkerTool.ImportLIbrary
helpviewer_keywords:
- IMPLIB linker option
- /IMPLIB linker option
- -IMPLIB linker option
- import libraries, overriding default name
ms.assetid: fe8f71ab-7055-41b5-8ef8-2b97cfa4a432
ms.openlocfilehash: dc9a9220d55f7831a00f70ec155cc5b57a695818
ms.sourcegitcommit: 0ab61bc3d2b6cfbd52a16c6ab2b97a8ea1864f12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2019
ms.locfileid: "62269981"
---
# <a name="implib-name-import-library"></a>/IMPLIB（命名导入库）

> /IMPLIB:*filename*

## <a name="parameters"></a>参数

*filename*<br/>
用户指定的导入库名称。 它将替换默认名称。

## <a name="remarks"></a>备注

/IMPLIB 选项可重写导入库链接时生成包含导出的程序创建的默认名称。 默认名称格式正确的主输出文件和扩展的基名称。 lib。 如果指定一个或多个以下，程序将包含导出：

- [__Declspec （dllexport)](../../cpp/dllexport-dllimport.md)的源代码中的关键字

- [导出](exports.md).def 文件语句

- [/Export](export-exports-a-function.md) LINK 命令中的规范

未创建导入库时，链接将忽略 /IMPLIB。 如果未指定导出，链接将不创建导入库。 如果在生成中使用导出文件时，链接将假定导入库已存在且不会创建一个。 导入库和导出文件的信息，请参阅[LIB 引用](lib-reference.md)。

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此链接器选项

1. 打开项目的“属性页”  对话框。 有关详细信息，请参阅[设置C++Visual Studio 中的编译器和生成属性](../working-with-project-properties.md)。

1. 单击**链接器**文件夹。

1. 单击**高级**属性页。

1. 修改**导入库**属性。

### <a name="to-set-this-linker-option-programmatically"></a>以编程方式设置此链接器选项

- 请参阅 <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ImportLibrary%2A>。

## <a name="see-also"></a>请参阅

[MSVC 链接器参考](linking.md)<br/>
[MSVC 链接器选项](linker-options.md)

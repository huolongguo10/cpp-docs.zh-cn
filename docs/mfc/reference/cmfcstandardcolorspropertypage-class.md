---
title: CMFCStandardColorsPropertyPage 类
ms.date: 11/04/2016
helpviewer_keywords:
- CMFCStandardColorsPropertyPage class [MFC]
ms.assetid: b84b7cfb-bb24-4c65-804a-5b642cb64400
ms.openlocfilehash: 91cfa609c31e83c02cce8b2a474a9b66ec3ba56f
ms.sourcegitcommit: 0ab61bc3d2b6cfbd52a16c6ab2b97a8ea1864f12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2019
ms.locfileid: "62388626"
---
# <a name="cmfcstandardcolorspropertypage-class"></a>CMFCStandardColorsPropertyPage 类

表示用户用来在颜色对话框中选择标准颜色的属性页。

## <a name="syntax"></a>语法

```
class CMFCStandardColorsPropertyPage : public CPropertyPage
```

## <a name="members"></a>成员

### <a name="public-constructors"></a>公共构造函数

|||
|-|-|
|名称|描述|
|`CMFCStandardColorsPropertyPage::CMFCStandardColorsPropertyPage`|默认构造函数。|

### <a name="public-methods"></a>公共方法

|||
|-|-|
|名称|描述|
|`CMFCStandardColorsPropertyPage::CreateObject`|由框架用于创建此类类型的动态实例。|
|`CMFCStandardColorsPropertyPage::GetThisClass`|由框架用于获取一个指向[CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md)与此类类型相关联的对象。|

### <a name="remarks"></a>备注

`CMFCColorDialog`类使用此类可显示标准颜色属性页。 有关详细信息`CMFCColorDialog`，请参阅[CMFCColorDialog 类](../../mfc/reference/cmfccolordialog-class.md)。

## <a name="inheritance-hierarchy"></a>继承层次结构

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CPropertyPage](../../mfc/reference/cpropertypage-class.md)

[CMFCStandardColorsPropertyPage](../../mfc/reference/cmfcstandardcolorspropertypage-class.md)

## <a name="requirements"></a>要求

**标头：** afxstandardcolorspropertypage.h

## <a name="see-also"></a>请参阅

[层次结构图](../../mfc/hierarchy-chart.md)<br/>
[类](../../mfc/reference/mfc-classes.md)<br/>
[CMFCColorDialog 类](../../mfc/reference/cmfccolordialog-class.md)<br/>
[CMFCCustomColorsPropertyPage 类](../../mfc/reference/cmfccustomcolorspropertypage-class.md)

---
title: CMapWordToPtr 类
ms.date: 11/04/2016
f1_keywords:
- CMapWordToPtr
- AFXCOLL/CMapWordToPtr
- AFXCOLL/CMapWordToPtr::CMapWordToPtr
- AFXCOLL/CMapWordToPtr::GetCount
- AFXCOLL/CMapWordToPtr::GetHashTableSize
- AFXCOLL/CMapWordToPtr::GetNextAssoc
- AFXCOLL/CMapWordToPtr::GetSize
- AFXCOLL/CMapWordToPtr::GetStartPosition
- AFXCOLL/CMapWordToPtr::HashKey
- AFXCOLL/CMapWordToPtr::InitHashTable
- AFXCOLL/CMapWordToPtr::IsEmpty
- AFXCOLL/CMapWordToPtr::Lookup
- AFXCOLL/CMapWordToPtr::LookupKey
- AFXCOLL/CMapWordToPtr::RemoveAll
- AFXCOLL/CMapWordToPtr::RemoveKey
- AFXCOLL/CMapWordToPtr::SetAt
helpviewer_keywords:
- CMapWordToPtr [MFC], CMapWordToPtr
- CMapWordToPtr [MFC], GetCount
- CMapWordToPtr [MFC], GetHashTableSize
- CMapWordToPtr [MFC], GetNextAssoc
- CMapWordToPtr [MFC], GetSize
- CMapWordToPtr [MFC], GetStartPosition
- CMapWordToPtr [MFC], HashKey
- CMapWordToPtr [MFC], InitHashTable
- CMapWordToPtr [MFC], IsEmpty
- CMapWordToPtr [MFC], Lookup
- CMapWordToPtr [MFC], LookupKey
- CMapWordToPtr [MFC], RemoveAll
- CMapWordToPtr [MFC], RemoveKey
- CMapWordToPtr [MFC], SetAt
ms.assetid: b204d87f-6427-43e1-93e3-a4b1bb41099f
ms.openlocfilehash: 3374b3123e150a4cac127e30bf7e9a6569371b5c
ms.sourcegitcommit: 1f009ab0f2cc4a177f2d1353d5a38f164612bdb1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/27/2020
ms.locfileid: "87222974"
---
# <a name="cmapwordtoptr-class"></a>CMapWordToPtr 类

支持 16 位键控的 void 指针的映射。

## <a name="syntax"></a>语法

```
class CMapWordToPtr : public CObject
```

## <a name="members"></a>成员

的成员函数 `CMapWordToPtr` 类似于类[CMapStringToOb](../../mfc/reference/cmapstringtoob-class.md)的成员函数。 由于此相似性，因此你可以使用 `CMapStringToOb` 参考文档获取成员函数细节。 无论你在何处看到 `CObject` 作为函数参数或返回值的指针，都要将指针替换为 **`void`** 。 无论你在何处看到 `CString` **`const`** **`char`** 作为函数参数或返回值的指针，都可以替换为 WORD。

`BOOL CMapWordToPtr::Lookup( WORD <key>, void*& <rValue> ) const;`

例如，转换为

`BOOL CMapStringToOb::Lookup( const char* <key>, CObject*& <rValue> ) const;`

### <a name="public-constructors"></a>公共构造函数

|名称|说明|
|----------|-----------------|
|[CMapWordToPtr::CMapWordToPtr](../../mfc/reference/cmapstringtoob-class.md#cmapstringtoob)|构造函数。|

### <a name="public-methods"></a>公共方法

|“属性”|说明|
|----------|-----------------|
|[CMapWordToPtr：： GetCount](../../mfc/reference/cmapstringtoob-class.md#getcount)|返回此映射中的元素数。|
|[CMapWordToPtr::GetHashTableSize](../../mfc/reference/cmapstringtoob-class.md#gethashtablesize)|确定哈希表中元素的当前数目。|
|[CMapWordToPtr::GetNextAssoc](../../mfc/reference/cmapstringtoob-class.md#getnextassoc)|获取用于循环访问的下一个元素。|
|[CMapWordToPtr：： GetSize](../../mfc/reference/cmapstringtoob-class.md#getsize)|返回此映射中的元素数。|
|[CMapWordToPtr::GetStartPosition](../../mfc/reference/cmapstringtoob-class.md#getstartposition)|返回第一个元素的位置。|
|[CMapWordToPtr::HashKey](../../mfc/reference/cmapstringtoob-class.md#hashkey)|计算指定键的哈希值。|
|[CMapWordToPtr::InitHashTable](../../mfc/reference/cmapstringtoob-class.md#inithashtable)|初始化哈希表。|
|[CMapWordToPtr：： IsEmpty](../../mfc/reference/cmapstringtoob-class.md#isempty)|测试空映射条件（无元素）。|
|[CMapWordToPtr：： Lookup](../../mfc/reference/cmapstringtoob-class.md#lookup)|基于 void 指针键查找 void 指针。 指针值（而不是它指向的实体）用于键比较。|
|[CMapWordToPtr：： LookupKey](../../mfc/reference/cmapstringtoob-class.md#lookupkey)|返回对与指定键值关联的键的引用。|
|[CMapWordToPtr：： RemoveAll](../../mfc/reference/cmapstringtoob-class.md#removeall)|从此映射中移除所有元素。|
|[CMapWordToPtr::RemoveKey](../../mfc/reference/cmapstringtoob-class.md#removekey)|移除由键指定的元素。|
|[CMapWordToPtr：： SetAt](../../mfc/reference/cmapstringtoob-class.md#setat)|将元素插入到映射中;如果找到匹配的键，则替换现有元素。|

### <a name="public-operators"></a>公共运算符

|名称|说明|
|----------|-----------------|
|[CMapWordToPtr：： operator \[\]](../../mfc/reference/cmapstringtoob-class.md#operator_at)|将元素插入到映射中-的运算符替换 `SetAt` 。|

## <a name="remarks"></a>备注

`CMapWordToPtr`合并了 IMPLEMENT_DYNAMIC 宏，以支持运行时类型访问和转储到 `CDumpContext` 对象。 如果需要单个地图元素的转储，则必须将转储上下文的深度设置为1或更大。

不能序列化单词到指针的映射。

`CMapWordToPtr`删除对象时，或删除其元素时，将删除单词和指针。 不删除指针引用的实体。

有关的详细信息 `CMapWordToPtr` ，请参阅文章[集合](../../mfc/collections.md)。

## <a name="inheritance-hierarchy"></a>继承层次结构

[CObject](../../mfc/reference/cobject-class.md)

`CMapWordToPtr`

## <a name="requirements"></a>要求

**标头：** afxcoll。h

## <a name="see-also"></a>另请参阅

[CObject 类](../../mfc/reference/cobject-class.md)<br/>
[层次结构图](../../mfc/hierarchy-chart.md)

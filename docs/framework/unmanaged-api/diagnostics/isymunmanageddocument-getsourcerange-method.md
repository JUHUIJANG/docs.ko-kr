---
title: ISymUnmanagedDocument::GetSourceRange 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59420cfd29c3228aece9fc5ae02b950db6099ea0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59218474"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a>ISymUnmanagedDocument::GetSourceRange 메서드
지정 된 버퍼에 지정된 된 포함된 된 소스 범위를 반환합니다. 버퍼는 소스를 포함할 수 있는 크기 여야 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
## <a name="parameters"></a>매개 변수  
 `startLine`  
 [in] 현재 문서의 시작 줄입니다.  
  
 `startColumn`  
 [in] 현재 문서의 시작 열입니다.  
  
 `endLine`  
 [in] 현재 문서의 마지막 줄입니다.  
  
 `endColumn`  
 [in] 현재 문서의 마지막 열입니다.  
  
 `cSourceBytes`  
 [in] 크기 (바이트)에서 소스입니다.  
  
 `pcSourceBytes`  
 [out] 원본 크기를 수신 하는 변수에 대 한 포인터입니다.  
  
 `source`  
 [out] 크기 및 소스 문서의 바이트 단위로 지정 된 범위의 길이입니다.  
  
## <a name="return-value"></a>반환 값  
 메서드가 성공 하면 S_OK입니다.  
  
## <a name="see-also"></a>참고자료

- [ISymUnmanagedDocument 인터페이스](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)

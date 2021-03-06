---
title: '방법: 4원수를 사용하여 3차원 회전에 애니메이션 효과 주기'
ms.date: 03/30/2017
helpviewer_keywords:
- quaternions [WPF]
- animation [WPF], 3-D translations [WPF], with quaternions
- 3-D translations [WPF], animating [WPF], with quaternions
ms.assetid: adca9cb1-066b-4de8-abbb-6b4007579ee7
ms.openlocfilehash: d994ac2ae67fd366f27f123d5bd15f14d5ac7abe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59183224"
---
# <a name="how-to-animate-a-3-d-rotation-using-quaternions"></a>방법: 4원수를 사용하여 3차원 회전에 애니메이션 효과 주기
이 예제에는 4 원수를 사용 하 여 3 차원 개체를 회전에 애니메이션을 적용 하는 방법을 보여 줍니다.  
  
 아래 코드를 <xref:System.Windows.Media.Media3D.QuaternionRotation3D> 에 대 한 값으로 사용 합니다 <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> 의 속성을 <xref:System.Windows.Media.Media3D.RotateTransform3D>.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline1)]  
  
 이 <xref:System.Windows.Media.Media3D.QuaternionRotation3D> 사용 하 여 애니메이션 효과가 적용 됩니다는 <xref:System.Windows.Media.Animation.QuaternionAnimation> 내에서 <xref:System.Windows.Media.Animation.Storyboard> 아래 코드를 사용 합니다.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline2)]  
  
## <a name="example"></a>예제  
 다음 코드에는 전체 샘플을 보여 줍니다.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexamplewholepage)]  
  
## <a name="see-also"></a>참고자료

- [애니메이션 개요](animation-overview.md)
- [3차원 장면 만들기](how-to-create-a-3-d-scene.md)
- [3차원 그래픽 개요](3-d-graphics-overview.md)
- [Transform 개요](transforms-overview.md)
- [Storyboard를 사용하여 3차원 회전에 애니메이션 효과 주기](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Rotation3DAnimation을 사용하여 3차원 회전에 애니메이션 효과 주기](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)

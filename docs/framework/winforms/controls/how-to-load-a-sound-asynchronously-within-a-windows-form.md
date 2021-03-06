---
title: '방법: Windows Form에서 비동기적으로 소리 로드'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SoundPlayer class [Windows Forms], loading sounds asynchronously
- sounds [Windows Forms], loading on separate threads
- threading [Windows Forms], sounds
ms.assetid: 3b6a9296-1d5e-4d52-a4ba-94366d6fe302
ms.openlocfilehash: 1d710f1e6d3b208365d5b1eb2524fbeeaa673c2d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59185759"
---
# <a name="how-to-load-a-sound-asynchronously-within-a-windows-form"></a>방법: Windows Form에서 비동기적으로 소리 로드
다음 코드 예제는 URL에서 소리를 비동기적으로 로드한 다음 새 스레드에서 재생합니다.  
  
## <a name="example"></a>예제  
 [!code-csharp[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>코드 컴파일  
 이 예제에는 다음 사항이 필요합니다.  
  
-   System 및 System.Windows.Forms 어셈블리에 대한 참조  
  
-   파일 이름 `"http://www.tailspintoys.com/sounds/stop.wav"`를 유효한 파일 이름으로 바꿉니다.  
  
 Visual Basic 또는 Visual C#에 대 한 명령줄에서이 예제를 빌드하는 방법에 대 한 내용은 [명령줄에서 빌드](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) 하거나 [csc.exe를 사용한 명령줄 빌드](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)합니다. 또한 새 프로젝트에 코드를 붙여 넣어 Visual Studio에서이 예제를 빌드할 수 있습니다.  
  
## <a name="robust-programming"></a>강력한 프로그래밍  
 파일 작업을 적절한 예외 처리 블록 내에 묶어야 합니다.  
  
 다음 조건에서 예외가 발생합니다.  
  
-   경로 이름 형식이 잘못되었습니다. 예를 들어 잘못된 문자를 포함하거나 공백만 포함합니다(<xref:System.ArgumentException> 클래스).  
  
-   경로가 읽기 전용입니다(<xref:System.IO.IOException> 클래스).  
  
-   경로 이름이 `Nothing`입니다(<xref:System.ArgumentNullException> 클래스).  
  
-   경로 이름이 너무 깁니다(<xref:System.IO.PathTooLongException> 클래스).  
  
-   경로가 잘못되었습니다(<xref:System.IO.DirectoryNotFoundException> 클래스).  
  
-   경로가 콜론 “:”뿐입니다(<xref:System.NotSupportedException> 클래스).  
  
## <a name="net-framework-security"></a>.NET Framework 보안  
 파일 이름을 바탕으로 파일 내용을 판단하면 안 됩니다. 예를 들어 `Form1.vb` 파일이 Visual Basic 소스 파일이 아닐 수도 있습니다. 애플리케이션에서 데이터를 사용하기 전에 모든 입력을 확인해야 합니다.  
  
## <a name="see-also"></a>참고자료

- <xref:System.Media.SoundPlayer.LoadAsync%2A>
- <xref:System.Media.SoundPlayer.LoadCompleted>
- <xref:System.Media.SoundPlayer.Play%2A>
- [방법: Windows Form에서 소리 재생](how-to-play-a-sound-from-a-windows-form.md)

---
title: "如何：从现有 Windows 窗体控件继承"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- custom controls [Windows Forms], inheritance
ms.assetid: 1e1fc8ea-c615-4cf0-a356-16d6df7444ab
caps.latest.revision: "18"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: fb50e5b301095cce72e59dc2899d44a47215b536
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-inherit-from-existing-windows-forms-controls"></a>如何：从现有 Windows 窗体控件继承
如果想要扩展现有控件的功能，可以通过继承创建一个派生自现有控件的控件。 从现有控件继承时，将继承该控件的的所有功能和可视属性。 例如，如果您已创建继承自一个控件<xref:System.Windows.Forms.Button>，新控件将如下 act 完全像和一个标准<xref:System.Windows.Forms.Button>控件。 然后可以通过实现自定义方法和属性来扩展或修改新控件的功能。 在某些控件中，你还可以更改继承的控件的可视外观通过重写其<xref:System.Windows.Forms.Control.OnPaint%2A>方法。  
  
> [!NOTE]
>  显示的对话框和菜单命令可能会与“帮助”中的描述不同，具体取决于你现用的设置或版本。 若要更改设置，请在 **“工具”** 菜单上选择 **“导入和导出设置”** 。 有关详细信息，请参阅[在 Visual Studio 中自定义开发设置](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3)。  
  
### <a name="to-create-an-inherited-control"></a>创建继承的控件  
  
1.  创建新的 **Windows 窗体应用程序**项目。  
  
2.  从“项目”菜单中选择“添加新项”。  
  
     “添加新项”对话框随即出现。  
  
3.  在“添加新项”对话框中，双击“自定义控件”。  
  
     一个新的自定义控件将被添加到项目中。  
  
4.  如果使用的是 Visual Basic，则在“解决方案资源管理器”的顶部单击“显示所有文件”。 展开 CustomControl1.vb，然后在“代码编辑器”中打开 CustomControl1.Designer.vb。  
  
5.  如果使用的 C#，则在“代码编辑器”中打开CustomControl1.cs。  
  
6.  找到类声明，该类继承自<xref:System.Windows.Forms.Control>。  
  
7.  将基类更改为要从中继承的控件。  
  
     例如，如果你想要从继承<xref:System.Windows.Forms.Button>，将类声明更改为以下：  
  
    ```vb  
    Partial Class CustomControl1  
        Inherits System.Windows.Forms.Button  
    ```  
  
    ```csharp  
    public partial class CustomControl1 : System.Windows.Forms.Button  
    ```  
  
8.  如果使用的是 Visual Basic，则保存并关闭 CustomControl1.Designer.vb。 在“代码编辑器”中打开 CustomControl1.vb。  
  
9. 实现控件将纳入的任何自定义方法或属性。  
  
10. 如果你想要修改的图形的外观的控件，重写<xref:System.Windows.Forms.Control.OnPaint%2A>方法。  
  
    > [!NOTE]
    >  重写<xref:System.Windows.Forms.Control.OnPaint%2A>不可以进行修改的所有控件的外观。 这些具有所有由 Windows 完成其绘制的控件 (例如， <xref:System.Windows.Forms.TextBox>) 永远不会调用其<xref:System.Windows.Forms.Control.OnPaint%2A>方法，并因此将永远不会使用自定义代码。 请参阅你想要修改以查看是否特定控件的帮助文档<xref:System.Windows.Forms.Control.OnPaint%2A>方法才有效。 有关所有 Windows 窗体控件的列表，请参阅[在 Windows 窗体上使用的控件](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)。 如果控件不具有<xref:System.Windows.Forms.Control.OnPaint%2A>列为成员方法，您不能通过重写此方法改变其外观。 有关自定义绘制的详细信息，请参阅[自定义控件的绘制和呈现](../../../../docs/framework/winforms/controls/custom-control-painting-and-rendering.md)。  
  
    ```vb  
    Protected Overrides Sub OnPaint(ByVal e As _  
       System.Windows.Forms.PaintEventArgs)  
       MyBase.OnPaint(e)  
       ' Insert code to do custom painting.   
       ' If you want to completely change the appearance of your control,  
       ' do not call MyBase.OnPaint(e).  
    End Sub  
    ```  
  
    ```csharp  
    protected override void OnPaint(PaintEventArgs pe)  
    {  
       base.OnPaint(pe);  
       // Insert code to do custom painting.  
       // If you want to completely change the appearance of your control,  
       // do not call base.OnPaint(pe).  
    }  
    ```  
  
11. 保存并测试控件。  
  
## <a name="see-also"></a>请参阅  
 [各种自定义控件](../../../../docs/framework/winforms/controls/varieties-of-custom-controls.md)  
 [如何：从 Control 类继承](../../../../docs/framework/winforms/controls/how-to-inherit-from-the-control-class.md)  
 [如何：从 UserControl 类继承](../../../../docs/framework/winforms/controls/how-to-inherit-from-the-usercontrol-class.md)  
 [如何：创作 Windows 窗体的控件](../../../../docs/framework/winforms/controls/how-to-author-controls-for-windows-forms.md)  
 [Visual Basic 中继承的事件处理程序疑难解答](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)  
 [演练：使用 Visual Basic 从 Windows 窗体控件继承](../../../../docs/framework/winforms/controls/walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
 [演练：使用 Visual C# 从 Windows 窗体控件继承](../../../../docs/framework/winforms/controls/walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)

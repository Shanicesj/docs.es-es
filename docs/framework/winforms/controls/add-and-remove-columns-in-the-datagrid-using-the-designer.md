---
title: Filtrar Agregar y quitar columnas en el Control de DataGridView de Windows Forms mediante el diseñador
ms.date: 03/30/2017
f1_keywords:
- vs.DataGridViewAddColumnDialog
helpviewer_keywords:
- DataGridView control [Windows Forms], adding columns
- DataGridView control [Windows Forms], removing columns
ms.assetid: 9e709f35-0a8c-4e7e-b4c4-bacb7a834077
ms.openlocfilehash: 01ae8987f7a92abf79a758e82ed0ac863fad57ce
ms.sourcegitcommit: 0069cb3de8eed4e92b2195d29e5769a76111acdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/16/2019
ms.locfileid: "56332694"
---
# <a name="how-to-add-and-remove-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a>Filtrar Agregar y quitar columnas en el Control de DataGridView de Windows Forms mediante el diseñador
Los formularios de Windows <xref:System.Windows.Forms.DataGridView> control debe contener columnas con el fin de mostrar los datos. Si va a rellenar el control manualmente, debe agregar las columnas. Como alternativa, puede enlazar el control a un origen de datos, que genera y rellena las columnas automáticamente. Si el origen de datos contiene más columnas que desea mostrar, puede quitar las columnas innecesarias.  
  
 Los procedimientos siguientes requieren un **aplicación Windows** proyecto con un formulario que contenga un <xref:System.Windows.Forms.DataGridView> control. Para obtener información acerca de cómo configurar un proyecto de este tipo, vea [Cómo: Cree un proyecto de aplicación de Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) y [Cómo: Agregar controles a Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Los cuadros de diálogo y comandos de menú que se ven pueden diferir de los descritos en la Ayuda, en función de los valores de configuración o de edición activos. Para cambiar la configuración, elija la opción **Importar y exportar configuraciones** del menú **Herramientas** . Para más información, vea [Personalizar el IDE de Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-a-column-using-the-designer"></a>Para agregar una columna mediante el diseñador  
  
1.  Haga clic en el glifo de etiqueta inteligente (![glifo de etiqueta inteligente](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) en la esquina superior derecha de la <xref:System.Windows.Forms.DataGridView> control y, a continuación, seleccione **Agregar columna**.  
  
2.  En el **Agregar columna** diálogo cuadro, elija el **columna enlazada a datos** opción y seleccione una columna del origen de datos o elija el **columna sin enlazar** opción y definir la columna uso de los campos correspondientes.  
  
3.  Haga clic en el **agregar** para agregar la columna, haciendo que aparezca en el diseñador si las columnas existentes no ya rellena el área de presentación del control.  
  
    > [!NOTE]
    >  Puede modificar las propiedades de columna en la **Edit Columns** cuadro de diálogo, que puede tener acceso desde la etiqueta inteligente del control.  
  
### <a name="to-remove-a-column-using-the-designer"></a>Para quitar una columna mediante el diseñador  
  
1.  Elija **Editar columnas** de etiqueta inteligente del control.  
  
2.  Seleccione una columna en la **columnas seleccionadas** lista.  
  
3.  Haga clic en el **quitar** botón para eliminar la columna, lo que hace que desaparece del diseñador.  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.Forms.DataGridView>
- [Cómo: Crear un proyecto de aplicación de Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Cómo: Agregar controles a Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)

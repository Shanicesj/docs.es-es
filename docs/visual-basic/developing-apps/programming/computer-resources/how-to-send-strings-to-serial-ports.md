---
title: Procedimiento para enviar cadenas a puertos serie en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- ports, sending strings to
- strings [Visual Basic], sending to serial ports
- My.Computer.Ports object
- serial ports, sending strings to
ms.assetid: 6ebf46cd-b2d0-4b2c-9a1f-be177b22ad52
ms.openlocfilehash: b2ba25f4ca3f63e1e7831d26745fa35cd337dc48
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54503032"
---
# <a name="how-to-send-strings-to-serial-ports-in-visual-basic"></a>Procedimiento para enviar cadenas a puertos serie en Visual Basic
En este tema se explica cómo usar `My.Computer.Ports` para enviar cadenas a los puertos serie del equipo en Visual Basic.  
  
## <a name="example"></a>Ejemplo  
 En este ejemplo se envía una cadena al puerto serie COM1. Es posible que tenga que usar un puerto serie diferente en el equipo.  
  
 Use el método `My.Computer.Ports.OpenSerialPort` para obtener una referencia al puerto. Para obtener más información, vea <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>.  
  
 El bloque `Using` permite a la aplicación cerrar el puerto serie aun cuando se genere una excepción. Todo el código que manipula el puerto serie debe aparecer dentro de este bloque o dentro un bloque `Try...Catch...Finally`.  
  
 El método <xref:System.IO.Ports.SerialPort.WriteLine%2A> envía los datos al puerto serie.  
  
 [!code-vb[VbVbalrMyComputer#33](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-send-strings-to-serial-ports_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilar el código  
  
-   En este ejemplo se presupone que el equipo usa `COM1`.  
  
## <a name="robust-programming"></a>Programación sólida  
 En este ejemplo se presupone que el equipo está usando `COM1`. Para obtener mayor flexibilidad, el código debe permitir al usuario seleccionar el puerto serie deseado entre una lista de puertos disponibles. Para obtener más información, vea [Cómo: Mostrar los puertos serie disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md).  
  
 En este ejemplo se usa un bloque `Using` para asegurarse de que la aplicación cierra el puerto incluso si se produce una excepción. Para obtener más información, vea [Using (Instrucción)](../../../../visual-basic/language-reference/statements/using-statement.md).  
  
## <a name="see-also"></a>Vea también
- <xref:Microsoft.VisualBasic.Devices.Ports>
- <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>
- [Cómo: Marcar a través de módems conectados a puertos serie](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-dial-modems-attached-to-serial-ports.md)
- [Cómo: Mostrar los puertos serie disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)

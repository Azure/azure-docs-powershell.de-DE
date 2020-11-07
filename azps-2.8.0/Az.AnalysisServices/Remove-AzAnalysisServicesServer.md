---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: b64ba86a6aab80910ac09bd3757565df433690dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658365"
---
# Remove-AzAnalysisServicesServer

## Synopsis
Löscht eine Instanz des Analysis Services-Servers

## Syntax

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzAnalysisServicesServer-Cmdlet löscht eine Instanz des Analysis Services-Servers

## Beispiele

### Beispiel 1
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

Mit diesem Befehl wird der Server mit dem Namen "Testserver" in der testgroup der ResourceGroup entfernt

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des Analysis Services-Servers

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Azure-Ressourcengruppe, zu der der Server gehört

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer

## Notizen
Alias: Remove-AzAs

## Verwandte Links

[Get-AzAnalysisServicesServer](./Get-AzAnalysisServicesServer.md)

[Neu – AzAnalysisServicesServer](./New-AzAnalysisServicesServer.md)

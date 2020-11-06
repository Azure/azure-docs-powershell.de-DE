---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: e93e38ef2914635cab61bf225c0d905d011ae643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479818"
---
# Export-AzureAnalysisServicesInstance

## Synopsis
Exportiert ein Protokoll aus einer Instanz des Analysis Services-Servers in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## Beschreibung
Das Export-AzureAnalysisServicesInstance-Cmdlet exportiert das Protokoll aus einer Instanz von Azure Analysis Services-Server in eine Datei

## Beispiele

### Beispiel 1
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

Mit diesem Befehl wird das Protokoll aus dem Server "Testserver" in der im Add-AzureAnalysisServicesAccount-Befehl angegebenen Umgebung exportiert und in der in OutputPath "C:\path\to\log\testserver.log" angegebenen Datei gespeichert.

## Parameter

### -Instanz
Name der Analysis Services-Serverinstanz

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
Ausgabepfad zur Datei zum Exportprotokoll

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Datei überschreiben, falls vorhanden, ohne zu Fragen

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen
Alias: Export-AzureAsInstanceLog

## Verwandte Links


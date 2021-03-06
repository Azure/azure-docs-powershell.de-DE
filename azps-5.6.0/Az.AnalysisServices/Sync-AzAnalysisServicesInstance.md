---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922227"
---
# Sync-AzAnalysisServicesInstance

## SYNOPSIS

Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben

## SYNTAX

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG

Das Sync-AzAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrageskaloutinstanzen in der aktuell angemeldeten Umgebung, wie im Befehl Add-AzAnalysisServicesAccount angegeben

## BEISPIELE

### Beispiel 1

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Mit diesem Befehl wird die Datenbank mit dem Namen "SalesOrders" auf dem Server namens "contoso" in der Umgebung synchronisiert westus.asazure.windows.net vorausgesetzt, der Benutzer hat sich mit dem Befehl "Add-AzAnalysisServicesAccount" bei dieser Umgebung angemeldet.

## PARAMETER

### -Database

Identität der zu synchronisierende Datenbank

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Instanz

Name der Analysis Services-Serverinstanz, die neu gestartet werden soll

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.

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

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails

## NOTIZEN

Alias: Sync-AzAsInstance

## VERWANDTE LINKS

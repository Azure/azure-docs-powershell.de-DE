---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300507"
---
# Update-AzSignalR

## Synopsis
Aktualisieren Sie einen Signalisierungs Dienst.

## Syntax

### ResourceGroupParameterSet (Standard)
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectParameterSet
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Aktualisieren Sie einen Signalisierungs Dienst.
Die folgenden Werte werden für die Parameter verwendet, wenn Sie nicht angegeben werden:
* `ResourceGroupName`: die standardmäßige Ressourcengruppe, die von eingerichtet wird `Set-AzDefault -ResourceGroupName` .
* `Sku`: `Standard_S1`

## Beispiele

### Aktualisieren Sie einen bestimmten Signalisierungs Dienst.
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### Angeben von ServiceMode und AllowedOrigin
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## Parameter

### -AllowedOrigin
Die zulässigen Ursprünge für den Signalisierungs Dienst. Wenn Sie alle zulassen möchten, verwenden Sie "*", und entfernen Sie alle anderen Ursprünge aus der Liste. Schrägstriche sind als Teil der Domäne oder nach TLD nicht zulässig.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Führen Sie das Cmdlet im Hintergrund Auftrag aus.

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

### -Inputobject
Das Resource-Objekt des Signals.

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Signal Dienstanbieters.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.
Wenn nicht angegeben, wird der Standardwert verwendet.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID des Signal Dienstanbieters.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceMode
Der Dienstmodus für den Signalisierungs Dienst.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Die signaldienst-SKU.
Standardmäßig auf "Standard_S1".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Die Tags für den Signalisierungs Dienst.

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnitCount
Die Anzahl der Signalisierungs Dienst Einheiten, nur Wert von {1, 2, 5, 10, 20, 50, 100}.
Standardwert 1.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. signalr. Models. PSSignalRResource

## Ausgaben

### Microsoft. Azure. Commands. signalr. Models. PSSignalRResource

## Notizen

## Verwandte Links

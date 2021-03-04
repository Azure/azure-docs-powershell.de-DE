---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: b94a7158830530be9df31531101c9c9c5be90df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938992"
---
# Get-AzBlockchainMemberApiKey

## SYNOPSIS
Listet die API-Schlüssel für ein Mitglied der Blockkette auf.

## SYNTAX

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Listet die API-Schlüssel für ein Mitglied der Blockkette auf.

## BEISPIELE

### Beispiel 1: Auflisten von Schlüsseln für die Blockkette
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

In diesem Befehl werden die Api-Schlüssel für ein Element der Blockkette aufgeführt.

## PARAMETER

### -BlockchainMemberName
Name des Mitgliedes der Blockkette.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die die Ressource enthält.
Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.
Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey

## NOTIZEN

ALIASE

## VERWANDTE LINKS


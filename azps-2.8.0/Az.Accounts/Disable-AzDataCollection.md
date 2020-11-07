---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: e78a361bfb332bc2a8bcb226fae946a3abc0a05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658477"
---
# Disable-AzDataCollection

## Synopsis
Entscheidet sich, Daten zu sammeln, um die AzurePowerShell-Cmdlets zu verbessern. Daten werden nicht erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.

## Syntax

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.
Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.
Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.
Führen Sie das Disable-AzDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer zu deaktivieren.
Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.
Wenn Sie die Datensammlung für den aktuellen Benutzer aktivieren möchten, führen Sie das Enable-AzDataCollection-Cmdlet aus.

## Beispiele

### Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer
```
PS C:\> Disable-AzDataCollection
```

In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren. 

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Enable-AzDataCollection](./Enable-AzDataCollection.md)


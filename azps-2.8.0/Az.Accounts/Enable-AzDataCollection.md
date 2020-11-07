---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658471"
---
# Enable-AzDataCollection

## Synopsis
Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit AzurePowerShell-Cmdlets zu verbessern.
Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.
Es werden keine Daten erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.

## Syntax

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.
Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.
Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.
Führen Sie das Enable-AzDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer zu aktivieren.
Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.
Wenn Sie die Datensammlung für den aktuellen Benutzer deaktivieren möchten, führen Sie das Disable-AzDataCollection-Cmdlet aus.

## Beispiele

### Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer
```
PS C:\> Enable-AzDataCollection
```

In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.

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

[Deaktivieren-AzDataCollection](./Disable-AzDataCollection.md)


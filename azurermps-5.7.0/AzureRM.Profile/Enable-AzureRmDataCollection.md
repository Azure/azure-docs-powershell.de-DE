---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663459"
---
# Enable-AzureRmDataCollection

## Synopsis
Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit AzurePowerShell-Cmdlets zu verbessern.
Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.
Es werden keine Daten erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.
Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzureRmDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.
Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.

Führen Sie das Enable-AzureRMDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer zu aktivieren.
Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.

Wenn Sie die Datensammlung für den aktuellen Benutzer deaktivieren möchten, führen Sie das Disable-AzureRmDataCollection-Cmdlet aus.

## Beispiele

### Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer
```
PS C:\> Enable-AzureRmDataCollection
```

In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Keine

## Notizen

## Verwandte Links

[Deaktivieren-AzureRmDataCollection](./Disable-AzureRmDataCollection.md)


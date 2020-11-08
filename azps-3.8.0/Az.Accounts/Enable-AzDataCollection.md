---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "94005285"
---
# Enable-AzDataCollection

## Synopsis
Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit den Azure PowerShell-Cmdlets zu verbessern. Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer. Daten werden standardmäßig erfasst, es sei denn, dass Sie sich ausdrücklich entscheiden.

## Syntax

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung

Das `Enable-AzDataCollection` Cmdlet wird verwendet, um sich für die Datensammlung zu entscheiden. Azure PowerShell sammelt standardmäßig Telemetrie-Daten automatisch. Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Erfahrung von Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten. Wenn Sie die Datensammlung deaktivieren möchten, müssen Sie die Ausführung explizit ablehnen `Disable-AzDataCollection` .

## Beispiele

### Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer

Im folgenden Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.

```powershell
Enable-AzDataCollection
```

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

Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## Eingaben

### Keine

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Deaktivieren-AzDataCollection](./Disable-AzDataCollection.md)

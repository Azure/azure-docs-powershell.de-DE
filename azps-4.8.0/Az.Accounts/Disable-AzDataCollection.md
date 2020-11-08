---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166635"
---
# Disable-AzDataCollection

## Synopsis
Entscheidet sich, Daten zu sammeln, um die Azure PowerShell-Cmdlets zu verbessern. Daten werden standardmäßig erfasst, es sei denn, dass Sie sich ausdrücklich entscheiden.

## Syntax

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung

Das `Disable-AzDataCollection` Cmdlet wird verwendet, um die Datensammlung zu deaktivieren. Azure PowerShell sammelt standardmäßig Telemetrie-Daten automatisch. Wenn Sie die Datensammlung deaktivieren möchten, müssen Sie explizit abmelden. Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Erfahrung von Azure PowerShell zu verbessern. Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten. Wenn Sie sich zuvor entschieden haben, führen Sie das Cmdlet aus, `Enable-AzDataCollection` um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer erneut zu aktivieren.

## Beispiele

### Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer

Im folgenden Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.

```powershell
Disable-AzDataCollection
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

[Enable-AzDataCollection](./Enable-AzDataCollection.md)

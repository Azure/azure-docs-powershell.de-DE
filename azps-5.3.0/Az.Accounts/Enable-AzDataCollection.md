---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471595"
---
# Enable-AzDataCollection

## SYNOPSIS
Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzererfahrung mit den Azure -PowerShell-Cmdlets zu verbessern. Beim Ausführen dieses Cmdlets wird die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer optdiert. Daten werden standardmäßig erfasst, sofern Sie dies nicht explizit melden.

## SYNTAX

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Das `Enable-AzDataCollection` Cmdlet wird verwendet, um sich für die Datensammlung zu entscheiden. Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten. Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, häufige Probleme zu erkennen und die Benutzererfahrung mit Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten. Zum Deaktivieren der Datensammlung müssen Sie die Ausführung explizit `Disable-AzDataCollection` deaktivieren.

## BEISPIELE

### Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer

Das folgende Beispiel zeigt, wie die Datensammlung für den aktuellen Benutzer aktiviert wird.

```powershell
Enable-AzDataCollection
```

## PARAMETERS

### -DefaultProfile

Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Confirm

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn

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

Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## EINGABEN

### Keine

## AUSGABEN

### System.Void

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Disable-AzDataCollection](./Disable-AzDataCollection.md)

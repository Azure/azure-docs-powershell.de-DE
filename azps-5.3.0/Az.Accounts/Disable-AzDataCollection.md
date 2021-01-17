---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471600"
---
# Disable-AzDataCollection

## SYNOPSIS
Sie können das Sammeln von Daten nicht mehr nutzen, um die Azure PowerShell-Cmdlets zu verbessern. Daten werden standardmäßig erfasst, sofern Sie dies nicht explizit melden.

## SYNTAX

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Das `Disable-AzDataCollection` Cmdlet wird verwendet, um die Datensammlung zu melden. Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten. Um die Datensammlung zu deaktivieren, müssen Sie dies explizit deaktivieren. Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, häufige Probleme zu erkennen und die Benutzererfahrung mit Azure PowerShell zu verbessern. Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten. Wenn Sie sich zuvor abmelden, führen Sie das Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem `Enable-AzDataCollection` aktuellen Computer erneut zu aktivieren.

## BEISPIELE

### Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer

Das folgende Beispiel zeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.

```powershell
Disable-AzDataCollection
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

[Enable-AzDataCollection](./Enable-AzDataCollection.md)

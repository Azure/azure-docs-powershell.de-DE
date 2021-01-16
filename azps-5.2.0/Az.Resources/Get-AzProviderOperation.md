---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293801"
---
# Get-AzProviderOperation

## SYNOPSIS
Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mit Azure RBAC sicherungsfähig sind.

## SYNTAX

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Die Get-AzProviderOperation macht die Vorgänge von Azure-Ressourcenanbietern verfügbar.
Vorgänge können erstellt werden, um benutzerdefinierte Rollen in Azure RBAC zu erstellen.
Der Befehl verwendet als Eingabe eine Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen( ) Zeichen(en), die die anzuzeigende *Vorgangsdetails bestimmt. Verwenden Get-AzProviderOperation * zum Erhalten aller Vorgänge für alle Azure-Ressourcenanbieter. Verwenden Get-AzProviderOperation Microsoft.Compute/,* um alle Vorgänge des Microsoft.Compute-Ressourcenanbieters zu erhalten.

## BEISPIELE

### Beispiel 1: Alle Aktionen für alle Anbieter erhalten
```powershell
PS C:\> Get-AzProviderOperation *
```

### Beispiel 2: Erhalten von Aktionen für einen bestimmten Ressourcenanbieter
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Beispiel 3: Alle Aktionen erhalten, die auf virtuellen Computern ausgeführt werden können
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -OperationSearchString
Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (*) )

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS ZU VERWANDTEN THEMEN

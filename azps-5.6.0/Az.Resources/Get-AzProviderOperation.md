---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950635"
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
Die Get-AzProviderOperation ruft die Vorgänge ab, die von Azure-Ressourcenanbietern verfügbar gemacht werden.
Vorgänge können erstellt werden, um benutzerdefinierte Rollen in Azure RBAC zu erstellen.
Der Befehl übernimmt als Eingabe eine Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen(en)), die die anzuzeigende *Vorgangsdetails bestimmt. Verwenden Get-AzProviderOperation * zum Erhalten aller Vorgänge für alle Azure-Ressourcenanbieter. Verwenden Get-AzProviderOperation Microsoft.Compute/,* um alle Vorgänge des Microsoft.Compute-Ressourcenanbieters zu erhalten.

## BEISPIELE

### Beispiel 1: Alle Aktionen für alle Anbieter erhalten
```powershell
PS C:\> Get-AzProviderOperation *
```

### Beispiel 2: Erhalten von Aktionen für einen bestimmten Ressourcenanbieter
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Beispiel 3: Alle Aktionen, die auf virtuellen Computern ausgeführt werden können
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETER

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## NOTIZEN
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## VERWANDTE LINKS

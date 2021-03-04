---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943601"
---
# Get-AzResourceMoverMoveCollection

## SYNOPSIS
Ruft die Move-Sammlung ab.

## SYNTAX

### Liste (Standard)
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Erhalten
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Liste1
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## BESCHREIBUNG
Ruft die Move-Sammlung ab.

## BEISPIELE

### Beispiel 1: Details zu allen Sammlungen im Abonnement verschieben
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

Hier erhalten Sie Details zu allen "Verschieben"-Sammlungen im Abonnement.

### Beispiel 2: Anzeigen von Details zur Move-Sammlung mit einem angegebenen Namen für die Umzugssammlung im Abonnement
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

Hier erhalten Sie Details zur Sammlung Verschieben mit einem angegebenen Namen für die Umzugssammlung im Abonnement.

### Beispiel 3: Erhalten von Details zur Sammlung Verschieben mit einem angegebenen Ressourcengruppennamen im Abonnement
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

Hier erhalten Sie Details zur Sammlung verschieben mit einem angegebenen Ressourcengruppennamen im Abonnement.

## PARAMETER

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

### -Name
Der Name der Sammlung verschieben.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Die Abonnement-ID.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection

## NOTIZEN

ALIASE

## VERWANDTE LINKS


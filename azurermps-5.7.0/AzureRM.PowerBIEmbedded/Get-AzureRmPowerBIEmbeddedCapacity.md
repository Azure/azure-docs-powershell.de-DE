---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662457"
---
# Get-AzureRmPowerBIEmbeddedCapacity

## Synopsis
Ruft die Details einer eingebetteten PowerBI-Kapazität ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## Beschreibung
Das Get-AzureRmPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.

## Beispiele

### Beispiel 1: Abrufen von Ressourcengruppenkapazitäten
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

Dieser Befehl ruft alle Azure PowerBI eingebettete Kapazität in der Ressourcengruppe mit dem Namen testRG

### Beispiel 2: Abrufen einer Kapazität
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen testcapacity in der Ressourcengruppe mit dem Namen testRG.

## Parameter

### -ResourceGroupName
Name der Azure-Ressourcengruppe, zu der die Kapazität gehört

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -Name
Name der eingebetteten PowerBI-Kapazität

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### -Resourcen-Nr
Azure-Ressourcen-ID

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Liste<Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity>

## Notizen

## Verwandte Links

[Neu – AzureRmPowerBIEmbeddedCapacity ](./New-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity ](./Remove-AzureRmPowerBIEmbeddedCapacity.md)

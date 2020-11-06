---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479609"
---
# <span data-ttu-id="c2cad-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c2cad-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c2cad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2cad-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cad-103">Erstellt eine neue PowerBI-eingebettete Kapazität.</span><span class="sxs-lookup"><span data-stu-id="c2cad-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2cad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2cad-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="c2cad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2cad-105">DESCRIPTION</span></span>
<span data-ttu-id="c2cad-106">Das New-AzureRmPowerBIEmbeddedCapacity-Cmdlet erstellt eine neue PowerBI-eingebettete Kapazität</span><span class="sxs-lookup"><span data-stu-id="c2cad-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c2cad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2cad-107">EXAMPLES</span></span>

### <span data-ttu-id="c2cad-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2cad-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="c2cad-109">Erstellt eine Kapazität mit dem Namen testcapacity im Azure Region West Central US und in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="c2cad-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="c2cad-110">Die SKU-Ebene für die Kapazität ist a1.</span><span class="sxs-lookup"><span data-stu-id="c2cad-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="c2cad-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2cad-111">PARAMETERS</span></span>

### <span data-ttu-id="c2cad-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cad-112">-ResourceGroupName</span></span>
<span data-ttu-id="c2cad-113">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="c2cad-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c2cad-114">-Name</span></span>
<span data-ttu-id="c2cad-115">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="c2cad-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2cad-116">-Location</span></span>
<span data-ttu-id="c2cad-117">Der Azure-Bereich, in dem die eingebettete PowerBI-Kapazität gehostet wird</span><span class="sxs-lookup"><span data-stu-id="c2cad-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-118">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2cad-118">-Sku</span></span>
<span data-ttu-id="c2cad-119">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="c2cad-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-120">– Administrator</span><span class="sxs-lookup"><span data-stu-id="c2cad-120">-Administrator</span></span>
<span data-ttu-id="c2cad-121">Eine durch Kommas getrennte Kapazitäts Namen, die als Administrator auf der Kapazität eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="c2cad-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2cad-122">-Tag</span></span>
<span data-ttu-id="c2cad-123">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c2cad-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2cad-124">-Confirm</span></span>
<span data-ttu-id="c2cad-125">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="c2cad-125">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2cad-126">-WhatIf</span></span>
<span data-ttu-id="c2cad-127">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="c2cad-127">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cad-128">CommonParameters</span></span>
<span data-ttu-id="c2cad-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cad-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cad-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2cad-131">INPUTS</span></span>

### <span data-ttu-id="c2cad-132">Keine</span><span class="sxs-lookup"><span data-stu-id="c2cad-132">None</span></span>
<span data-ttu-id="c2cad-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c2cad-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2cad-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2cad-134">OUTPUTS</span></span>

### <span data-ttu-id="c2cad-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c2cad-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c2cad-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2cad-136">NOTES</span></span>

## <span data-ttu-id="c2cad-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2cad-137">RELATED LINKS</span></span>

[<span data-ttu-id="c2cad-138">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c2cad-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c2cad-139">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c2cad-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)

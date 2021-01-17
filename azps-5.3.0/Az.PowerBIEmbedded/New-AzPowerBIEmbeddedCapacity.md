---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376688"
---
# <span data-ttu-id="335a8-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="335a8-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="335a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="335a8-102">SYNOPSIS</span></span>
<span data-ttu-id="335a8-103">Erstellt eine neue eingebettete PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="335a8-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="335a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="335a8-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335a8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="335a8-105">DESCRIPTION</span></span>
<span data-ttu-id="335a8-106">Das New-AzPowerBIEmbeddedCapacity A0 erstellt eine neue eingebettete PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="335a8-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="335a8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="335a8-107">EXAMPLES</span></span>

### <span data-ttu-id="335a8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="335a8-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="335a8-109">Erstellt in der Azure-Region "West Central USA" und in "resource group testRG" eine Kapazitätsprobe mit namen".</span><span class="sxs-lookup"><span data-stu-id="335a8-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="335a8-110">Die SKU-Ebene für die Kapazität ist A1.</span><span class="sxs-lookup"><span data-stu-id="335a8-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="335a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="335a8-111">PARAMETERS</span></span>

### <span data-ttu-id="335a8-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="335a8-112">-Administrator</span></span>
<span data-ttu-id="335a8-113">Durch Kommas getrennte Namen, die als Administrator für die Kapazität festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="335a8-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335a8-114">-DefaultProfile</span></span>
<span data-ttu-id="335a8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="335a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="335a8-116">-Location</span><span class="sxs-lookup"><span data-stu-id="335a8-116">-Location</span></span>
<span data-ttu-id="335a8-117">Azure-Region, in der die eingebettete PowerBI-Kapazität gehostet wird</span><span class="sxs-lookup"><span data-stu-id="335a8-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="335a8-118">-Name</span></span>
<span data-ttu-id="335a8-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="335a8-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="335a8-121">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="335a8-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="335a8-122">-Sku</span></span>
<span data-ttu-id="335a8-123">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="335a8-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="335a8-124">-Tag</span></span>
<span data-ttu-id="335a8-125">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="335a8-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="335a8-126">-Confirm</span></span>
<span data-ttu-id="335a8-127">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="335a8-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="335a8-128">-WhatIf</span></span>
<span data-ttu-id="335a8-129">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen wird, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="335a8-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="335a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335a8-130">CommonParameters</span></span>
<span data-ttu-id="335a8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335a8-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335a8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335a8-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="335a8-133">INPUTS</span></span>

### <span data-ttu-id="335a8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="335a8-134">System.String</span></span>

### <span data-ttu-id="335a8-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="335a8-135">System.String[]</span></span>

### <span data-ttu-id="335a8-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="335a8-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="335a8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="335a8-137">OUTPUTS</span></span>

### <span data-ttu-id="335a8-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="335a8-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="335a8-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="335a8-139">NOTES</span></span>

## <span data-ttu-id="335a8-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="335a8-140">RELATED LINKS</span></span>

[<span data-ttu-id="335a8-141">Get-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="335a8-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="335a8-142">Remove-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="335a8-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995328"
---
# <span data-ttu-id="3ad12-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ad12-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ad12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ad12-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad12-103">Erstellt eine neue PowerBI-eingebettete Kapazität.</span><span class="sxs-lookup"><span data-stu-id="3ad12-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3ad12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ad12-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ad12-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad12-106">Das New-AzPowerBIEmbeddedCapacity-Cmdlet erstellt eine neue PowerBI-eingebettete Kapazität</span><span class="sxs-lookup"><span data-stu-id="3ad12-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3ad12-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ad12-107">EXAMPLES</span></span>

### <span data-ttu-id="3ad12-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ad12-108">Example 1</span></span>
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

<span data-ttu-id="3ad12-109">Erstellt eine Kapazität mit dem Namen testcapacity im Azure Region West Central US und in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="3ad12-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="3ad12-110">Die SKU-Ebene für die Kapazität ist a1.</span><span class="sxs-lookup"><span data-stu-id="3ad12-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="3ad12-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ad12-111">PARAMETERS</span></span>

### <span data-ttu-id="3ad12-112">– Administrator</span><span class="sxs-lookup"><span data-stu-id="3ad12-112">-Administrator</span></span>
<span data-ttu-id="3ad12-113">Ein durch Kommas getrennte Namen, der als Administrator für die Kapazität gesetzt wird</span><span class="sxs-lookup"><span data-stu-id="3ad12-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="3ad12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad12-114">-DefaultProfile</span></span>
<span data-ttu-id="3ad12-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ad12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad12-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="3ad12-116">-Location</span></span>
<span data-ttu-id="3ad12-117">Der Azure-Bereich, in dem die eingebettete PowerBI-Kapazität gehostet wird</span><span class="sxs-lookup"><span data-stu-id="3ad12-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="3ad12-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3ad12-118">-Name</span></span>
<span data-ttu-id="3ad12-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="3ad12-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3ad12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad12-120">-ResourceGroupName</span></span>
<span data-ttu-id="3ad12-121">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="3ad12-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3ad12-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="3ad12-122">-Sku</span></span>
<span data-ttu-id="3ad12-123">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="3ad12-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="3ad12-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ad12-124">-Tag</span></span>
<span data-ttu-id="3ad12-125">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3ad12-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="3ad12-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ad12-126">-Confirm</span></span>
<span data-ttu-id="3ad12-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="3ad12-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3ad12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad12-128">-WhatIf</span></span>
<span data-ttu-id="3ad12-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="3ad12-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3ad12-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad12-130">CommonParameters</span></span>
<span data-ttu-id="3ad12-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad12-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad12-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad12-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad12-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ad12-133">INPUTS</span></span>

### <span data-ttu-id="3ad12-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ad12-134">System.String</span></span>

### <span data-ttu-id="3ad12-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="3ad12-135">System.String[]</span></span>

### <span data-ttu-id="3ad12-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ad12-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3ad12-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ad12-137">OUTPUTS</span></span>

### <span data-ttu-id="3ad12-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ad12-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3ad12-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ad12-139">NOTES</span></span>

## <span data-ttu-id="3ad12-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ad12-140">RELATED LINKS</span></span>

[<span data-ttu-id="3ad12-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ad12-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3ad12-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3ad12-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3f2515a1c1039dbf9ff4a0635111c95a610d9834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823935"
---
# <span data-ttu-id="e5781-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e5781-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e5781-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5781-102">SYNOPSIS</span></span>
<span data-ttu-id="e5781-103">Erstellt eine neue PowerBI-eingebettete Kapazität.</span><span class="sxs-lookup"><span data-stu-id="e5781-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e5781-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5781-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5781-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5781-105">DESCRIPTION</span></span>
<span data-ttu-id="e5781-106">Das New-AzPowerBIEmbeddedCapacity-Cmdlet erstellt eine neue PowerBI-eingebettete Kapazität</span><span class="sxs-lookup"><span data-stu-id="e5781-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e5781-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5781-107">EXAMPLES</span></span>

### <span data-ttu-id="e5781-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5781-108">Example 1</span></span>
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

<span data-ttu-id="e5781-109">Erstellt eine Kapazität mit dem Namen testcapacity im Azure Region West Central US und in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="e5781-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="e5781-110">Die SKU-Ebene für die Kapazität ist a1.</span><span class="sxs-lookup"><span data-stu-id="e5781-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="e5781-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5781-111">PARAMETERS</span></span>

### <span data-ttu-id="e5781-112">– Administrator</span><span class="sxs-lookup"><span data-stu-id="e5781-112">-Administrator</span></span>
<span data-ttu-id="e5781-113">Ein durch Kommas getrennte Namen, der als Administrator für die Kapazität gesetzt wird</span><span class="sxs-lookup"><span data-stu-id="e5781-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="e5781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5781-114">-DefaultProfile</span></span>
<span data-ttu-id="e5781-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5781-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5781-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="e5781-116">-Location</span></span>
<span data-ttu-id="e5781-117">Der Azure-Bereich, in dem die eingebettete PowerBI-Kapazität gehostet wird</span><span class="sxs-lookup"><span data-stu-id="e5781-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="e5781-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e5781-118">-Name</span></span>
<span data-ttu-id="e5781-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e5781-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e5781-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5781-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5781-121">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="e5781-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e5781-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="e5781-122">-Sku</span></span>
<span data-ttu-id="e5781-123">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="e5781-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="e5781-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5781-124">-Tag</span></span>
<span data-ttu-id="e5781-125">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5781-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="e5781-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5781-126">-Confirm</span></span>
<span data-ttu-id="e5781-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="e5781-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e5781-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5781-128">-WhatIf</span></span>
<span data-ttu-id="e5781-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="e5781-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e5781-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5781-130">CommonParameters</span></span>
<span data-ttu-id="e5781-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5781-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5781-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5781-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5781-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5781-133">INPUTS</span></span>

### <span data-ttu-id="e5781-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5781-134">System.String</span></span>

### <span data-ttu-id="e5781-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="e5781-135">System.String[]</span></span>

### <span data-ttu-id="e5781-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5781-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5781-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5781-137">OUTPUTS</span></span>

### <span data-ttu-id="e5781-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e5781-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e5781-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5781-139">NOTES</span></span>

## <span data-ttu-id="e5781-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5781-140">RELATED LINKS</span></span>

[<span data-ttu-id="e5781-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e5781-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e5781-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e5781-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)

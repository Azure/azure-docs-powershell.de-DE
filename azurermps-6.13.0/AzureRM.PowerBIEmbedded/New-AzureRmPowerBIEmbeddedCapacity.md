---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495798"
---
# <span data-ttu-id="085a1-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="085a1-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="085a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="085a1-102">SYNOPSIS</span></span>
<span data-ttu-id="085a1-103">Erstellt eine neue PowerBI-eingebettete Kapazität.</span><span class="sxs-lookup"><span data-stu-id="085a1-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="085a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="085a1-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="085a1-105">DESCRIPTION</span></span>
<span data-ttu-id="085a1-106">Das New-AzureRmPowerBIEmbeddedCapacity-Cmdlet erstellt eine neue PowerBI-eingebettete Kapazität</span><span class="sxs-lookup"><span data-stu-id="085a1-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="085a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="085a1-107">EXAMPLES</span></span>

### <span data-ttu-id="085a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="085a1-108">Example 1</span></span>
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

<span data-ttu-id="085a1-109">Erstellt eine Kapazität mit dem Namen testcapacity im Azure Region West Central US und in der Ressourcengruppe testRG.</span><span class="sxs-lookup"><span data-stu-id="085a1-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="085a1-110">Die SKU-Ebene für die Kapazität ist a1.</span><span class="sxs-lookup"><span data-stu-id="085a1-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="085a1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="085a1-111">PARAMETERS</span></span>

### <span data-ttu-id="085a1-112">– Administrator</span><span class="sxs-lookup"><span data-stu-id="085a1-112">-Administrator</span></span>
<span data-ttu-id="085a1-113">Eine durch Kommas getrennte Kapazitäts Namen, die als Administrator auf der Kapazität eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="085a1-113">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="085a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085a1-114">-DefaultProfile</span></span>
<span data-ttu-id="085a1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="085a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="085a1-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="085a1-116">-Location</span></span>
<span data-ttu-id="085a1-117">Der Azure-Bereich, in dem die eingebettete PowerBI-Kapazität gehostet wird</span><span class="sxs-lookup"><span data-stu-id="085a1-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="085a1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="085a1-118">-Name</span></span>
<span data-ttu-id="085a1-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="085a1-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="085a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="085a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="085a1-121">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="085a1-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="085a1-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="085a1-122">-Sku</span></span>
<span data-ttu-id="085a1-123">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="085a1-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="085a1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="085a1-124">-Tag</span></span>
<span data-ttu-id="085a1-125">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="085a1-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="085a1-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="085a1-126">-Confirm</span></span>
<span data-ttu-id="085a1-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="085a1-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="085a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085a1-128">-WhatIf</span></span>
<span data-ttu-id="085a1-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="085a1-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="085a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085a1-130">CommonParameters</span></span>
<span data-ttu-id="085a1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085a1-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="085a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085a1-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="085a1-133">INPUTS</span></span>

### <span data-ttu-id="085a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="085a1-134">System.String</span></span>

### <span data-ttu-id="085a1-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="085a1-135">System.String[]</span></span>

### <span data-ttu-id="085a1-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="085a1-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="085a1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="085a1-137">OUTPUTS</span></span>

### <span data-ttu-id="085a1-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="085a1-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="085a1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="085a1-139">NOTES</span></span>

## <span data-ttu-id="085a1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="085a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="085a1-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="085a1-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="085a1-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="085a1-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)

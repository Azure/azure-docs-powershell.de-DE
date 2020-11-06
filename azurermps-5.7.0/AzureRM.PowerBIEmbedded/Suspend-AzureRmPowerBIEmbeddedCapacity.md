---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476698"
---
# <span data-ttu-id="12240-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12240-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="12240-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12240-102">SYNOPSIS</span></span>
<span data-ttu-id="12240-103">Unterbricht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="12240-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12240-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12240-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="12240-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12240-105">DESCRIPTION</span></span>
<span data-ttu-id="12240-106">Das Suspend-AzureRmPowerBIEmbeddedCapacity-Cmdlet unterbricht eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="12240-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="12240-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12240-107">EXAMPLES</span></span>

### <span data-ttu-id="12240-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12240-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="12240-109">Dieser Befehl unterbricht eine aktive Kapazität mit dem Namen "testcapacity" in der testgroup der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12240-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="12240-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12240-110">PARAMETERS</span></span>

### <span data-ttu-id="12240-111">-Name</span><span class="sxs-lookup"><span data-stu-id="12240-111">-Name</span></span>
<span data-ttu-id="12240-112">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="12240-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="12240-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12240-113">-ResourceGroupName</span></span>
<span data-ttu-id="12240-114">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="12240-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="12240-115">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12240-115">-ResourceId</span></span>
<span data-ttu-id="12240-116">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="12240-116">Azure resource ID</span></span>

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

### <span data-ttu-id="12240-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12240-117">-InputObject</span></span>
<span data-ttu-id="12240-118">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="12240-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12240-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12240-119">-Confirm</span></span>
<span data-ttu-id="12240-120">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="12240-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="12240-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12240-121">-WhatIf</span></span>
<span data-ttu-id="12240-122">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="12240-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="12240-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12240-123">CommonParameters</span></span>
<span data-ttu-id="12240-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12240-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12240-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12240-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12240-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12240-126">INPUTS</span></span>

### <span data-ttu-id="12240-127">Keine</span><span class="sxs-lookup"><span data-stu-id="12240-127">None</span></span>
<span data-ttu-id="12240-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="12240-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12240-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12240-129">OUTPUTS</span></span>

### <span data-ttu-id="12240-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12240-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="12240-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="12240-131">NOTES</span></span>

## <span data-ttu-id="12240-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12240-132">RELATED LINKS</span></span>

[<span data-ttu-id="12240-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12240-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="12240-134">Lebenslauf-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12240-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)


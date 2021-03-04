---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 54c546ed7bac74a13030a9ca2f18276761e2d381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940024"
---
# <span data-ttu-id="1ea31-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1ea31-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1ea31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ea31-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea31-103">Eine Instanz der eingebetteten PowerBI-Kapazität wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="1ea31-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="1ea31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ea31-104">SYNTAX</span></span>

### <span data-ttu-id="1ea31-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ea31-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea31-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ea31-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea31-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ea31-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea31-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ea31-108">DESCRIPTION</span></span>
<span data-ttu-id="1ea31-109">Das Suspend-AzPowerBIEmbeddedCapacity-Cmdlet setzt eine Instanz der eingebetteten PowerBI-Kapazität an.</span><span class="sxs-lookup"><span data-stu-id="1ea31-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1ea31-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ea31-110">EXAMPLES</span></span>

### <span data-ttu-id="1ea31-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ea31-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="1ea31-112">Mit diesem Befehl wird eine aktive Kapazität namens Testkapazität in der Testgruppe der Ressourcengruppe angehalten.</span><span class="sxs-lookup"><span data-stu-id="1ea31-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="1ea31-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ea31-113">PARAMETERS</span></span>

### <span data-ttu-id="1ea31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea31-114">-DefaultProfile</span></span>
<span data-ttu-id="1ea31-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ea31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ea31-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea31-116">-InputObject</span></span>
<span data-ttu-id="1ea31-117">Eingabeobjekt für Piping</span><span class="sxs-lookup"><span data-stu-id="1ea31-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea31-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1ea31-118">-Name</span></span>
<span data-ttu-id="1ea31-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="1ea31-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea31-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ea31-120">-PassThru</span></span>
<span data-ttu-id="1ea31-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1ea31-121">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea31-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ea31-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="1ea31-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea31-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ea31-124">-ResourceId</span></span>
<span data-ttu-id="1ea31-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1ea31-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea31-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ea31-126">-Confirm</span></span>
<span data-ttu-id="1ea31-127">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="1ea31-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="1ea31-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea31-128">-WhatIf</span></span>
<span data-ttu-id="1ea31-129">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen soll, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1ea31-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="1ea31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea31-130">CommonParameters</span></span>
<span data-ttu-id="1ea31-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea31-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea31-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea31-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ea31-133">INPUTS</span></span>

### <span data-ttu-id="1ea31-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1ea31-134">System.String</span></span>

### <span data-ttu-id="1ea31-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1ea31-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1ea31-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ea31-136">OUTPUTS</span></span>

### <span data-ttu-id="1ea31-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1ea31-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1ea31-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ea31-138">NOTES</span></span>

## <span data-ttu-id="1ea31-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ea31-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ea31-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1ea31-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1ea31-141">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1ea31-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)


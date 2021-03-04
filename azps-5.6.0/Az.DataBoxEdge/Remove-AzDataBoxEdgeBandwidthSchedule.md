---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 6b30f79f7ef1e2819004c8ac7e9d3b6737bfb7d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946204"
---
# <span data-ttu-id="04ab5-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="04ab5-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="04ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="04ab5-103">Entfernt einen Bandbreitenplan.</span><span class="sxs-lookup"><span data-stu-id="04ab5-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="04ab5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04ab5-104">SYNTAX</span></span>

### <span data-ttu-id="04ab5-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04ab5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ab5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ab5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ab5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ab5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ab5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="04ab5-109">Das **Cmdlet Remove-AzDataBoxEdgeBandwidthSchedule** entfernt den Bandbreitenplan für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="04ab5-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="04ab5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04ab5-110">EXAMPLES</span></span>

### <span data-ttu-id="04ab5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04ab5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="04ab5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04ab5-112">PARAMETERS</span></span>

### <span data-ttu-id="04ab5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ab5-113">-AsJob</span></span>
<span data-ttu-id="04ab5-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="04ab5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="04ab5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04ab5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ab5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="04ab5-117">-DeviceName</span></span>
<span data-ttu-id="04ab5-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="04ab5-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ab5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ab5-119">-InputObject</span></span>
<span data-ttu-id="04ab5-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="04ab5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04ab5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04ab5-121">-Name</span></span>
<span data-ttu-id="04ab5-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="04ab5-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ab5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04ab5-123">-PassThru</span></span>
<span data-ttu-id="04ab5-124">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="04ab5-124">returns true if successful</span></span>

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

### <span data-ttu-id="04ab5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ab5-125">-ResourceGroupName</span></span>
<span data-ttu-id="04ab5-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="04ab5-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ab5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ab5-127">-ResourceId</span></span>
<span data-ttu-id="04ab5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ab5-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ab5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04ab5-129">-Confirm</span></span>
<span data-ttu-id="04ab5-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04ab5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ab5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ab5-131">-WhatIf</span></span>
<span data-ttu-id="04ab5-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04ab5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04ab5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04ab5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ab5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ab5-134">CommonParameters</span></span>
<span data-ttu-id="04ab5-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ab5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ab5-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04ab5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ab5-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04ab5-137">INPUTS</span></span>

### <span data-ttu-id="04ab5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="04ab5-138">System.String</span></span>

### <span data-ttu-id="04ab5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="04ab5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="04ab5-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04ab5-140">OUTPUTS</span></span>

### <span data-ttu-id="04ab5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04ab5-141">System.Boolean</span></span>

## <span data-ttu-id="04ab5-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="04ab5-142">NOTES</span></span>

## <span data-ttu-id="04ab5-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="04ab5-143">RELATED LINKS</span></span>

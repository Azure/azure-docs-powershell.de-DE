---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307824"
---
# <span data-ttu-id="e1c22-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c22-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e1c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c22-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c22-103">Entfernt einen Bandbreitenplan.</span><span class="sxs-lookup"><span data-stu-id="e1c22-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="e1c22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1c22-104">SYNTAX</span></span>

### <span data-ttu-id="e1c22-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1c22-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c22-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1c22-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c22-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1c22-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c22-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1c22-108">DESCRIPTION</span></span>
<span data-ttu-id="e1c22-109">Das **Cmdlet "Remove-AzDataBoxEdgeBandwidthSchedule"** entfernt den Bandbreitenzeitplan für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e1c22-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="e1c22-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1c22-110">EXAMPLES</span></span>

### <span data-ttu-id="e1c22-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1c22-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="e1c22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c22-112">PARAMETERS</span></span>

### <span data-ttu-id="e1c22-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1c22-113">-AsJob</span></span>
<span data-ttu-id="e1c22-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e1c22-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1c22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c22-115">-DefaultProfile</span></span>
<span data-ttu-id="e1c22-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1c22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c22-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e1c22-117">-DeviceName</span></span>
<span data-ttu-id="e1c22-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="e1c22-118">Device Name</span></span>

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

### <span data-ttu-id="e1c22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1c22-119">-InputObject</span></span>
<span data-ttu-id="e1c22-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e1c22-120">Input Object</span></span>

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

### <span data-ttu-id="e1c22-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c22-121">-Name</span></span>
<span data-ttu-id="e1c22-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e1c22-122">Resource Name</span></span>

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

### <span data-ttu-id="e1c22-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1c22-123">-PassThru</span></span>
<span data-ttu-id="e1c22-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e1c22-124">returns true if successful</span></span>

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

### <span data-ttu-id="e1c22-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c22-125">-ResourceGroupName</span></span>
<span data-ttu-id="e1c22-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e1c22-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e1c22-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c22-127">-ResourceId</span></span>
<span data-ttu-id="e1c22-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c22-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e1c22-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c22-129">-Confirm</span></span>
<span data-ttu-id="e1c22-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1c22-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c22-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1c22-131">-WhatIf</span></span>
<span data-ttu-id="e1c22-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1c22-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c22-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1c22-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c22-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c22-134">CommonParameters</span></span>
<span data-ttu-id="e1c22-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c22-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c22-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1c22-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c22-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1c22-137">INPUTS</span></span>

### <span data-ttu-id="e1c22-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e1c22-138">System.String</span></span>

### <span data-ttu-id="e1c22-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e1c22-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e1c22-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1c22-140">OUTPUTS</span></span>

### <span data-ttu-id="e1c22-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1c22-141">System.Boolean</span></span>

## <span data-ttu-id="e1c22-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1c22-142">NOTES</span></span>

## <span data-ttu-id="e1c22-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1c22-143">RELATED LINKS</span></span>

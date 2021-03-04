---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8e8b26ac8bdb097ac87135f764e1dfc4f4450f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929048"
---
# <span data-ttu-id="2b1f3-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2b1f3-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="2b1f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1f3-103">Entfernt eine Freigabe vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-103">Removes a share from the device.</span></span>

## <span data-ttu-id="2b1f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b1f3-104">SYNTAX</span></span>

### <span data-ttu-id="2b1f3-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b1f3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b1f3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b1f3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b1f3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b1f3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b1f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f3-108">DESCRIPTION</span></span>
<span data-ttu-id="2b1f3-109">Das **Cmdlet Remove-AzDataBoxEdgeEdgeShare** entfernt die zugehörigen Edgefreigaben für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="2b1f3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b1f3-110">EXAMPLES</span></span>

### <span data-ttu-id="2b1f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b1f3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="2b1f3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b1f3-112">PARAMETERS</span></span>

### <span data-ttu-id="2b1f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b1f3-113">-AsJob</span></span>
<span data-ttu-id="2b1f3-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2b1f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b1f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1f3-115">-DefaultProfile</span></span>
<span data-ttu-id="2b1f3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b1f3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2b1f3-117">-DeviceName</span></span>
<span data-ttu-id="2b1f3-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="2b1f3-118">Device Name</span></span>

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

### <span data-ttu-id="2b1f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b1f3-119">-InputObject</span></span>
<span data-ttu-id="2b1f3-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="2b1f3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b1f3-121">-Name</span></span>
<span data-ttu-id="2b1f3-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="2b1f3-122">Resource Name</span></span>

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

### <span data-ttu-id="2b1f3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b1f3-123">-PassThru</span></span>
<span data-ttu-id="2b1f3-124">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2b1f3-124">returns true if successful</span></span>

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

### <span data-ttu-id="2b1f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b1f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b1f3-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2b1f3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2b1f3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b1f3-127">-ResourceId</span></span>
<span data-ttu-id="2b1f3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b1f3-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1f3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b1f3-129">-Confirm</span></span>
<span data-ttu-id="2b1f3-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b1f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b1f3-131">-WhatIf</span></span>
<span data-ttu-id="2b1f3-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b1f3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b1f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1f3-134">CommonParameters</span></span>
<span data-ttu-id="2b1f3-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1f3-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b1f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1f3-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b1f3-137">INPUTS</span></span>

### <span data-ttu-id="2b1f3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2b1f3-138">System.String</span></span>

### <span data-ttu-id="2b1f3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2b1f3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="2b1f3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b1f3-140">OUTPUTS</span></span>

### <span data-ttu-id="2b1f3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b1f3-141">System.Boolean</span></span>

## <span data-ttu-id="2b1f3-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b1f3-142">NOTES</span></span>

## <span data-ttu-id="2b1f3-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b1f3-143">RELATED LINKS</span></span>

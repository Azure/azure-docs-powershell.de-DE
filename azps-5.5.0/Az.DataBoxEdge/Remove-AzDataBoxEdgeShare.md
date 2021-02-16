---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170934"
---
# <span data-ttu-id="fa4e9-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fa4e9-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="fa4e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4e9-103">Entfernt eine Freigabe vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-103">Removes a share from the device.</span></span>

## <span data-ttu-id="fa4e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa4e9-104">SYNTAX</span></span>

### <span data-ttu-id="fa4e9-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa4e9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa4e9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa4e9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa4e9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa4e9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa4e9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa4e9-108">DESCRIPTION</span></span>
<span data-ttu-id="fa4e9-109">Das **Cmdlet "Remove-AzDataBoxEdgeEdgeShare"** entfernt die zugehörigen Edgefreigaben für ein Data Box-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="fa4e9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa4e9-110">EXAMPLES</span></span>

### <span data-ttu-id="fa4e9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa4e9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="fa4e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa4e9-112">PARAMETERS</span></span>

### <span data-ttu-id="fa4e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa4e9-113">-AsJob</span></span>
<span data-ttu-id="fa4e9-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa4e9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa4e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4e9-115">-DefaultProfile</span></span>
<span data-ttu-id="fa4e9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa4e9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fa4e9-117">-DeviceName</span></span>
<span data-ttu-id="fa4e9-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="fa4e9-118">Device Name</span></span>

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

### <span data-ttu-id="fa4e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa4e9-119">-InputObject</span></span>
<span data-ttu-id="fa4e9-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="fa4e9-120">Input Object</span></span>

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

### <span data-ttu-id="fa4e9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa4e9-121">-Name</span></span>
<span data-ttu-id="fa4e9-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="fa4e9-122">Resource Name</span></span>

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

### <span data-ttu-id="fa4e9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa4e9-123">-PassThru</span></span>
<span data-ttu-id="fa4e9-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-124">returns true if successful</span></span>

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

### <span data-ttu-id="fa4e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa4e9-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fa4e9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fa4e9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa4e9-127">-ResourceId</span></span>
<span data-ttu-id="fa4e9-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa4e9-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="fa4e9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa4e9-129">-Confirm</span></span>
<span data-ttu-id="fa4e9-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4e9-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa4e9-131">-WhatIf</span></span>
<span data-ttu-id="fa4e9-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa4e9-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4e9-134">CommonParameters</span></span>
<span data-ttu-id="fa4e9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4e9-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa4e9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4e9-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa4e9-137">INPUTS</span></span>

### <span data-ttu-id="fa4e9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fa4e9-138">System.String</span></span>

### <span data-ttu-id="fa4e9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fa4e9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="fa4e9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa4e9-140">OUTPUTS</span></span>

### <span data-ttu-id="fa4e9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa4e9-141">System.Boolean</span></span>

## <span data-ttu-id="fa4e9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa4e9-142">NOTES</span></span>

## <span data-ttu-id="fa4e9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa4e9-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168601"
---
# <span data-ttu-id="76faf-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="76faf-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="76faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76faf-102">SYNOPSIS</span></span>
<span data-ttu-id="76faf-103">Entfernt die zugeordnete IoT-Rolle für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="76faf-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="76faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76faf-104">SYNTAX</span></span>

### <span data-ttu-id="76faf-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76faf-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76faf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76faf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76faf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76faf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76faf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76faf-108">DESCRIPTION</span></span>
<span data-ttu-id="76faf-109">Das **Cmdlet "Remove-AzStackEdgeRole"** entfernt die zugehörige IoT-Rolle für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="76faf-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="76faf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76faf-110">EXAMPLES</span></span>

### <span data-ttu-id="76faf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76faf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="76faf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76faf-112">PARAMETERS</span></span>

### <span data-ttu-id="76faf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76faf-113">-AsJob</span></span>
<span data-ttu-id="76faf-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76faf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76faf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76faf-115">-DefaultProfile</span></span>
<span data-ttu-id="76faf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76faf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76faf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="76faf-117">-DeviceName</span></span>
<span data-ttu-id="76faf-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="76faf-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76faf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76faf-119">-InputObject</span></span>
<span data-ttu-id="76faf-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="76faf-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76faf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="76faf-121">-Name</span></span>
<span data-ttu-id="76faf-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="76faf-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76faf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76faf-123">-PassThru</span></span>
<span data-ttu-id="76faf-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="76faf-124">returns true if successful</span></span>

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

### <span data-ttu-id="76faf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76faf-125">-ResourceGroupName</span></span>
<span data-ttu-id="76faf-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="76faf-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76faf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76faf-127">-ResourceId</span></span>
<span data-ttu-id="76faf-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="76faf-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="76faf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76faf-129">-Confirm</span></span>
<span data-ttu-id="76faf-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76faf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76faf-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76faf-131">-WhatIf</span></span>
<span data-ttu-id="76faf-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76faf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76faf-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76faf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76faf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76faf-134">CommonParameters</span></span>
<span data-ttu-id="76faf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76faf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76faf-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76faf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76faf-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76faf-137">INPUTS</span></span>

### <span data-ttu-id="76faf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="76faf-138">System.String</span></span>

### <span data-ttu-id="76faf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="76faf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="76faf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76faf-140">OUTPUTS</span></span>

### <span data-ttu-id="76faf-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="76faf-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="76faf-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76faf-142">NOTES</span></span>

## <span data-ttu-id="76faf-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76faf-143">RELATED LINKS</span></span>

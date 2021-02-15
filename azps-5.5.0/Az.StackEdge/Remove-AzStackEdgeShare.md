---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145508"
---
# <span data-ttu-id="b298a-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b298a-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="b298a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b298a-102">SYNOPSIS</span></span>
<span data-ttu-id="b298a-103">Entfernt eine Freigabe vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="b298a-103">Removes a share from the device.</span></span>

## <span data-ttu-id="b298a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b298a-104">SYNTAX</span></span>

### <span data-ttu-id="b298a-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b298a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b298a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b298a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b298a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b298a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b298a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b298a-108">DESCRIPTION</span></span>
<span data-ttu-id="b298a-109">Das **Cmdlet "Remove-AzStackEdgeEdgeShare"** entfernt die zugehörigen Edgefreigaben für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b298a-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="b298a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b298a-110">EXAMPLES</span></span>

### <span data-ttu-id="b298a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b298a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="b298a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b298a-112">PARAMETERS</span></span>

### <span data-ttu-id="b298a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b298a-113">-AsJob</span></span>
<span data-ttu-id="b298a-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b298a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b298a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b298a-115">-DefaultProfile</span></span>
<span data-ttu-id="b298a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b298a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b298a-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b298a-117">-DeviceName</span></span>
<span data-ttu-id="b298a-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="b298a-118">Device Name</span></span>

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

### <span data-ttu-id="b298a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b298a-119">-InputObject</span></span>
<span data-ttu-id="b298a-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b298a-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b298a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b298a-121">-Name</span></span>
<span data-ttu-id="b298a-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b298a-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b298a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b298a-123">-PassThru</span></span>
<span data-ttu-id="b298a-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b298a-124">returns true if successful</span></span>

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

### <span data-ttu-id="b298a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b298a-125">-ResourceGroupName</span></span>
<span data-ttu-id="b298a-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b298a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b298a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b298a-127">-ResourceId</span></span>
<span data-ttu-id="b298a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b298a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b298a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b298a-129">-Confirm</span></span>
<span data-ttu-id="b298a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b298a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b298a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b298a-131">-WhatIf</span></span>
<span data-ttu-id="b298a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b298a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b298a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b298a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b298a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b298a-134">CommonParameters</span></span>
<span data-ttu-id="b298a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b298a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b298a-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b298a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b298a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b298a-137">INPUTS</span></span>

### <span data-ttu-id="b298a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b298a-138">System.String</span></span>

### <span data-ttu-id="b298a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b298a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="b298a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b298a-140">OUTPUTS</span></span>

### <span data-ttu-id="b298a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b298a-141">System.Boolean</span></span>

## <span data-ttu-id="b298a-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b298a-142">NOTES</span></span>

## <span data-ttu-id="b298a-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b298a-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467960"
---
# <span data-ttu-id="0501e-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0501e-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="0501e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0501e-102">SYNOPSIS</span></span>
<span data-ttu-id="0501e-103">Entfernt die Bestellung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="0501e-103">Removes the order for a device.</span></span>

## <span data-ttu-id="0501e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0501e-104">SYNTAX</span></span>

### <span data-ttu-id="0501e-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0501e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0501e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0501e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0501e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0501e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0501e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0501e-108">DESCRIPTION</span></span>
<span data-ttu-id="0501e-109">Das **Cmdlet "Remove-AzStackEdgeOrder"** löscht eine vorhandene Bestellung für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="0501e-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="0501e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0501e-110">EXAMPLES</span></span>

### <span data-ttu-id="0501e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0501e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="0501e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0501e-112">PARAMETERS</span></span>

### <span data-ttu-id="0501e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0501e-113">-AsJob</span></span>
<span data-ttu-id="0501e-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0501e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0501e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0501e-115">-DefaultProfile</span></span>
<span data-ttu-id="0501e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0501e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0501e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0501e-117">-DeviceName</span></span>
<span data-ttu-id="0501e-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="0501e-118">Device Name</span></span>

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

### <span data-ttu-id="0501e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0501e-119">-InputObject</span></span>
<span data-ttu-id="0501e-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="0501e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0501e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0501e-121">-PassThru</span></span>
<span data-ttu-id="0501e-122">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0501e-122">returns true if successful</span></span>

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

### <span data-ttu-id="0501e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0501e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0501e-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="0501e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0501e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0501e-125">-ResourceId</span></span>
<span data-ttu-id="0501e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0501e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="0501e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0501e-127">-Confirm</span></span>
<span data-ttu-id="0501e-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0501e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0501e-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0501e-129">-WhatIf</span></span>
<span data-ttu-id="0501e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0501e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0501e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0501e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0501e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0501e-132">CommonParameters</span></span>
<span data-ttu-id="0501e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0501e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0501e-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0501e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0501e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0501e-135">INPUTS</span></span>

### <span data-ttu-id="0501e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0501e-136">System.String</span></span>

### <span data-ttu-id="0501e-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0501e-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="0501e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0501e-138">OUTPUTS</span></span>

### <span data-ttu-id="0501e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0501e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="0501e-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0501e-140">NOTES</span></span>

## <span data-ttu-id="0501e-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0501e-141">RELATED LINKS</span></span>

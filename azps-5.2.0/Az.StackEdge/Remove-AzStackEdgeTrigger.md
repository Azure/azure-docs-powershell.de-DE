---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358699"
---
# <span data-ttu-id="b609c-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b609c-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="b609c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b609c-102">SYNOPSIS</span></span>
<span data-ttu-id="b609c-103">Entfernt einen vorhandenen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="b609c-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="b609c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b609c-104">SYNTAX</span></span>

### <span data-ttu-id="b609c-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b609c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b609c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b609c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b609c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b609c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b609c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b609c-108">DESCRIPTION</span></span>
<span data-ttu-id="b609c-109">Das **Cmdlet "Remove-AzStackEdgeTrigger"** entfernt einen vorhandenen Trigger auf dem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="b609c-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="b609c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b609c-110">EXAMPLES</span></span>

### <span data-ttu-id="b609c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b609c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="b609c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b609c-112">PARAMETERS</span></span>

### <span data-ttu-id="b609c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b609c-113">-AsJob</span></span>
<span data-ttu-id="b609c-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b609c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b609c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b609c-115">-DefaultProfile</span></span>
<span data-ttu-id="b609c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b609c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b609c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b609c-117">-DeviceName</span></span>
<span data-ttu-id="b609c-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="b609c-118">Device Name</span></span>

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

### <span data-ttu-id="b609c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b609c-119">-InputObject</span></span>
<span data-ttu-id="b609c-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b609c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b609c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b609c-121">-Name</span></span>
<span data-ttu-id="b609c-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b609c-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b609c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b609c-123">-PassThru</span></span>
<span data-ttu-id="b609c-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b609c-124">returns true if successful</span></span>

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

### <span data-ttu-id="b609c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b609c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b609c-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b609c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b609c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b609c-127">-ResourceId</span></span>
<span data-ttu-id="b609c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b609c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b609c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b609c-129">-Confirm</span></span>
<span data-ttu-id="b609c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b609c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b609c-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b609c-131">-WhatIf</span></span>
<span data-ttu-id="b609c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b609c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b609c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b609c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b609c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b609c-134">CommonParameters</span></span>
<span data-ttu-id="b609c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b609c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b609c-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b609c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b609c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b609c-137">INPUTS</span></span>

### <span data-ttu-id="b609c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b609c-138">System.String</span></span>

### <span data-ttu-id="b609c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b609c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="b609c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b609c-140">OUTPUTS</span></span>

### <span data-ttu-id="b609c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b609c-141">System.Boolean</span></span>

## <span data-ttu-id="b609c-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b609c-142">NOTES</span></span>

## <span data-ttu-id="b609c-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b609c-143">RELATED LINKS</span></span>

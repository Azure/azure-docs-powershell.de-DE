---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 2e1b3e3db319f724e22673e4139b4cb290879d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945196"
---
# <span data-ttu-id="3beca-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="3beca-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="3beca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3beca-102">SYNOPSIS</span></span>
<span data-ttu-id="3beca-103">Entfernt einen vorhandenen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="3beca-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="3beca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3beca-104">SYNTAX</span></span>

### <span data-ttu-id="3beca-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3beca-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3beca-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beca-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3beca-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3beca-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3beca-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3beca-108">DESCRIPTION</span></span>
<span data-ttu-id="3beca-109">Das **Cmdlet Remove-AzDataBoxEdgeTrigger** entfernt einen vorhandenen Trigger auf dem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="3beca-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="3beca-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3beca-110">EXAMPLES</span></span>

### <span data-ttu-id="3beca-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3beca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="3beca-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3beca-112">PARAMETERS</span></span>

### <span data-ttu-id="3beca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3beca-113">-AsJob</span></span>
<span data-ttu-id="3beca-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3beca-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3beca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3beca-115">-DefaultProfile</span></span>
<span data-ttu-id="3beca-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3beca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3beca-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3beca-117">-DeviceName</span></span>
<span data-ttu-id="3beca-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="3beca-118">Device Name</span></span>

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

### <span data-ttu-id="3beca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3beca-119">-InputObject</span></span>
<span data-ttu-id="3beca-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="3beca-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3beca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3beca-121">-Name</span></span>
<span data-ttu-id="3beca-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="3beca-122">Resource Name</span></span>

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

### <span data-ttu-id="3beca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3beca-123">-PassThru</span></span>
<span data-ttu-id="3beca-124">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="3beca-124">returns true if successful</span></span>

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

### <span data-ttu-id="3beca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3beca-125">-ResourceGroupName</span></span>
<span data-ttu-id="3beca-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3beca-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3beca-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3beca-127">-ResourceId</span></span>
<span data-ttu-id="3beca-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3beca-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3beca-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3beca-129">-Confirm</span></span>
<span data-ttu-id="3beca-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3beca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3beca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3beca-131">-WhatIf</span></span>
<span data-ttu-id="3beca-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3beca-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3beca-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3beca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3beca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3beca-134">CommonParameters</span></span>
<span data-ttu-id="3beca-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3beca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3beca-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3beca-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3beca-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3beca-137">INPUTS</span></span>

### <span data-ttu-id="3beca-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3beca-138">System.String</span></span>

### <span data-ttu-id="3beca-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="3beca-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="3beca-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3beca-140">OUTPUTS</span></span>

### <span data-ttu-id="3beca-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3beca-141">System.Boolean</span></span>

## <span data-ttu-id="3beca-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3beca-142">NOTES</span></span>

## <span data-ttu-id="3beca-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3beca-143">RELATED LINKS</span></span>

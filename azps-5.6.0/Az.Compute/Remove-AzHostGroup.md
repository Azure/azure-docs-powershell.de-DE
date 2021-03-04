---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934267"
---
# <span data-ttu-id="0833d-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="0833d-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="0833d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0833d-102">SYNOPSIS</span></span>
<span data-ttu-id="0833d-103">Entfernt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="0833d-103">Removes a host group.</span></span>

## <span data-ttu-id="0833d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0833d-104">SYNTAX</span></span>

### <span data-ttu-id="0833d-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="0833d-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0833d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0833d-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0833d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0833d-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0833d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0833d-108">DESCRIPTION</span></span>
<span data-ttu-id="0833d-109">Mit diesem Cmdlet wird eine Hostgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0833d-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="0833d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0833d-110">EXAMPLES</span></span>

### <span data-ttu-id="0833d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0833d-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="0833d-112">Dieser Befehl ruft die angegebene Hostgruppe ab und entfernt sie.</span><span class="sxs-lookup"><span data-stu-id="0833d-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="0833d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0833d-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="0833d-114">Mit diesem Befehl wird die angegebene Hostgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="0833d-114">This command removes the given host group.</span></span>

## <span data-ttu-id="0833d-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0833d-115">PARAMETERS</span></span>

### <span data-ttu-id="0833d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0833d-116">-AsJob</span></span>
<span data-ttu-id="0833d-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0833d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0833d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0833d-118">-DefaultProfile</span></span>
<span data-ttu-id="0833d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0833d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0833d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0833d-120">-InputObject</span></span>
<span data-ttu-id="0833d-121">Das lokale Objekt der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="0833d-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0833d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0833d-122">-Name</span></span>
<span data-ttu-id="0833d-123">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="0833d-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0833d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0833d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0833d-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0833d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0833d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0833d-126">-ResourceId</span></span>
<span data-ttu-id="0833d-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0833d-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0833d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0833d-128">-Confirm</span></span>
<span data-ttu-id="0833d-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0833d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0833d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0833d-130">-WhatIf</span></span>
<span data-ttu-id="0833d-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0833d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0833d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0833d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0833d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0833d-133">CommonParameters</span></span>
<span data-ttu-id="0833d-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0833d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0833d-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0833d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0833d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0833d-136">INPUTS</span></span>

### <span data-ttu-id="0833d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0833d-137">System.String</span></span>

### <span data-ttu-id="0833d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="0833d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="0833d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0833d-139">OUTPUTS</span></span>

### <span data-ttu-id="0833d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0833d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0833d-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0833d-141">NOTES</span></span>

## <span data-ttu-id="0833d-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0833d-142">RELATED LINKS</span></span>

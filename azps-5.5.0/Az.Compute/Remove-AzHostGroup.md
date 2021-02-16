---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171204"
---
# <span data-ttu-id="06128-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="06128-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="06128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06128-102">SYNOPSIS</span></span>
<span data-ttu-id="06128-103">Entfernt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="06128-103">Removes a host group.</span></span>

## <span data-ttu-id="06128-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06128-104">SYNTAX</span></span>

### <span data-ttu-id="06128-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="06128-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06128-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="06128-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06128-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="06128-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06128-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06128-108">DESCRIPTION</span></span>
<span data-ttu-id="06128-109">Mit diesem Cmdlet wird eine Hostgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="06128-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="06128-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06128-110">EXAMPLES</span></span>

### <span data-ttu-id="06128-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06128-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="06128-112">Dieser Befehl ruft die angegebene Hostgruppe ab und entfernt sie.</span><span class="sxs-lookup"><span data-stu-id="06128-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="06128-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="06128-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="06128-114">Mit diesem Befehl wird die angegebene Hostgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="06128-114">This command removes the given host group.</span></span>

## <span data-ttu-id="06128-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06128-115">PARAMETERS</span></span>

### <span data-ttu-id="06128-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06128-116">-AsJob</span></span>
<span data-ttu-id="06128-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="06128-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06128-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06128-118">-DefaultProfile</span></span>
<span data-ttu-id="06128-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06128-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06128-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06128-120">-InputObject</span></span>
<span data-ttu-id="06128-121">Das lokale Objekt der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="06128-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="06128-122">-Name</span><span class="sxs-lookup"><span data-stu-id="06128-122">-Name</span></span>
<span data-ttu-id="06128-123">Der Name der Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="06128-123">The name of the host group.</span></span>

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

### <span data-ttu-id="06128-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06128-124">-ResourceGroupName</span></span>
<span data-ttu-id="06128-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06128-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="06128-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06128-126">-ResourceId</span></span>
<span data-ttu-id="06128-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="06128-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="06128-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06128-128">-Confirm</span></span>
<span data-ttu-id="06128-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06128-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06128-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="06128-130">-WhatIf</span></span>
<span data-ttu-id="06128-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06128-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06128-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06128-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06128-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06128-133">CommonParameters</span></span>
<span data-ttu-id="06128-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06128-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06128-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06128-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06128-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06128-136">INPUTS</span></span>

### <span data-ttu-id="06128-137">System.String</span><span class="sxs-lookup"><span data-stu-id="06128-137">System.String</span></span>

### <span data-ttu-id="06128-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="06128-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="06128-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06128-139">OUTPUTS</span></span>

### <span data-ttu-id="06128-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="06128-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="06128-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06128-141">NOTES</span></span>

## <span data-ttu-id="06128-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06128-142">RELATED LINKS</span></span>

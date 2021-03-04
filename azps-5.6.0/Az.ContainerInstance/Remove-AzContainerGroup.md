---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: f4774ea7dec4ddd8df29c0a131fbaf080cbbba94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945269"
---
# <span data-ttu-id="4610e-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4610e-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="4610e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4610e-102">SYNOPSIS</span></span>
<span data-ttu-id="4610e-103">Entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4610e-103">Removes a container group.</span></span>

## <span data-ttu-id="4610e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4610e-104">SYNTAX</span></span>

### <span data-ttu-id="4610e-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4610e-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4610e-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="4610e-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4610e-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4610e-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4610e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4610e-108">DESCRIPTION</span></span>
<span data-ttu-id="4610e-109">Das **Cmdlet Remove-AzContainerGroup** entfernt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4610e-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="4610e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4610e-110">EXAMPLES</span></span>

### <span data-ttu-id="4610e-111">Beispiel 1: Entfernen einer Containergruppe</span><span class="sxs-lookup"><span data-stu-id="4610e-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="4610e-112">Mit diesem Befehl wird die angegebene Containergruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="4610e-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="4610e-113">Beispiel 2: Entfernt eine Containergruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="4610e-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="4610e-114">Mit diesem Befehl wird eine Containergruppe durch Piping entfernt.</span><span class="sxs-lookup"><span data-stu-id="4610e-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="4610e-115">Beispiel 3: Entfernt eine Containergruppe nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4610e-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="4610e-116">Mit diesem Befehl wird eine Containergruppe nach Ressourcen-ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="4610e-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="4610e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4610e-117">PARAMETERS</span></span>

### <span data-ttu-id="4610e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4610e-118">-DefaultProfile</span></span>
<span data-ttu-id="4610e-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4610e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4610e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4610e-120">-InputObject</span></span>
<span data-ttu-id="4610e-121">Die zu entfernende Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4610e-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4610e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4610e-122">-Name</span></span>
<span data-ttu-id="4610e-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4610e-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4610e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4610e-124">-PassThru</span></span>
<span data-ttu-id="4610e-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4610e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4610e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4610e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4610e-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4610e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4610e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4610e-128">-ResourceId</span></span>
<span data-ttu-id="4610e-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4610e-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4610e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4610e-130">-Confirm</span></span>
<span data-ttu-id="4610e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4610e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4610e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4610e-132">-WhatIf</span></span>
<span data-ttu-id="4610e-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4610e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4610e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4610e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4610e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4610e-135">CommonParameters</span></span>
<span data-ttu-id="4610e-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4610e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4610e-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4610e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4610e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4610e-138">INPUTS</span></span>

### <span data-ttu-id="4610e-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4610e-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="4610e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4610e-140">System.String</span></span>

## <span data-ttu-id="4610e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4610e-141">OUTPUTS</span></span>

### <span data-ttu-id="4610e-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4610e-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4610e-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4610e-143">NOTES</span></span>

## <span data-ttu-id="4610e-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4610e-144">RELATED LINKS</span></span>

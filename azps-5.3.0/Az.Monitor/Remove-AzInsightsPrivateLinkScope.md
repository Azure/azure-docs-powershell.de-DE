---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468312"
---
# <span data-ttu-id="e8abc-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e8abc-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="e8abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8abc-102">SYNOPSIS</span></span>
<span data-ttu-id="e8abc-103">Bereich für private Verknüpfungen löschen</span><span class="sxs-lookup"><span data-stu-id="e8abc-103">delete private link scope</span></span>

## <span data-ttu-id="e8abc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8abc-104">SYNTAX</span></span>

### <span data-ttu-id="e8abc-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8abc-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8abc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8abc-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8abc-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8abc-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8abc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8abc-108">DESCRIPTION</span></span>
<span data-ttu-id="e8abc-109">Bereich für private Verknüpfungen löschen</span><span class="sxs-lookup"><span data-stu-id="e8abc-109">delete private link scope</span></span>

## <span data-ttu-id="e8abc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8abc-110">EXAMPLES</span></span>

### <span data-ttu-id="e8abc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8abc-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="e8abc-112">Bereich für private Verknüpfungen löschen mit dem Namen "scope_name" unter der Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="e8abc-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="e8abc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e8abc-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="e8abc-114">Löschen eines privaten Verknüpfungsbereichs mit Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e8abc-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="e8abc-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e8abc-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="e8abc-116">Delete private link scope with input private link scope object</span><span class="sxs-lookup"><span data-stu-id="e8abc-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="e8abc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8abc-117">PARAMETERS</span></span>

### <span data-ttu-id="e8abc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8abc-118">-DefaultProfile</span></span>
<span data-ttu-id="e8abc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8abc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8abc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8abc-120">-InputObject</span></span>
<span data-ttu-id="e8abc-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e8abc-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8abc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8abc-122">-Name</span></span>
<span data-ttu-id="e8abc-123">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="e8abc-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8abc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8abc-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8abc-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e8abc-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8abc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8abc-126">-ResourceId</span></span>
<span data-ttu-id="e8abc-127">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e8abc-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8abc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8abc-128">-Confirm</span></span>
<span data-ttu-id="e8abc-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8abc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8abc-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e8abc-130">-WhatIf</span></span>
<span data-ttu-id="e8abc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8abc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8abc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8abc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8abc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8abc-133">CommonParameters</span></span>
<span data-ttu-id="e8abc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8abc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8abc-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8abc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8abc-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8abc-136">INPUTS</span></span>

### <span data-ttu-id="e8abc-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e8abc-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e8abc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e8abc-138">System.String</span></span>

## <span data-ttu-id="e8abc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8abc-139">OUTPUTS</span></span>

### <span data-ttu-id="e8abc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8abc-140">System.Boolean</span></span>

## <span data-ttu-id="e8abc-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8abc-141">NOTES</span></span>

## <span data-ttu-id="e8abc-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8abc-142">RELATED LINKS</span></span>

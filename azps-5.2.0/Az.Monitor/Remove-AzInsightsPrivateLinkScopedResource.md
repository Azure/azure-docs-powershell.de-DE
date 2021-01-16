---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289864"
---
# <span data-ttu-id="38114-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="38114-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="38114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38114-102">SYNOPSIS</span></span>
<span data-ttu-id="38114-103">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="38114-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="38114-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38114-104">SYNTAX</span></span>

### <span data-ttu-id="38114-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="38114-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38114-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38114-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38114-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38114-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38114-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38114-108">DESCRIPTION</span></span>
<span data-ttu-id="38114-109">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="38114-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="38114-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38114-110">EXAMPLES</span></span>

### <span data-ttu-id="38114-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38114-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="38114-112">Ressource mit Bereich "Private Verknüpfung" löschen</span><span class="sxs-lookup"><span data-stu-id="38114-112">delete private link scoped resource</span></span>

## <span data-ttu-id="38114-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38114-113">PARAMETERS</span></span>

### <span data-ttu-id="38114-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38114-114">-DefaultProfile</span></span>
<span data-ttu-id="38114-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38114-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38114-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38114-116">-InputObject</span></span>
<span data-ttu-id="38114-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="38114-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="38114-118">-Name</span><span class="sxs-lookup"><span data-stu-id="38114-118">-Name</span></span>
<span data-ttu-id="38114-119">Name der ressource mit Bereichsbereich</span><span class="sxs-lookup"><span data-stu-id="38114-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38114-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38114-120">-ResourceGroupName</span></span>
<span data-ttu-id="38114-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="38114-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38114-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38114-122">-ResourceId</span></span>
<span data-ttu-id="38114-123">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="38114-123">Resource Id</span></span>

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

### <span data-ttu-id="38114-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="38114-124">-ScopeName</span></span>
<span data-ttu-id="38114-125">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="38114-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38114-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38114-126">-Confirm</span></span>
<span data-ttu-id="38114-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38114-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38114-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38114-128">-WhatIf</span></span>
<span data-ttu-id="38114-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38114-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38114-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38114-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38114-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38114-131">CommonParameters</span></span>
<span data-ttu-id="38114-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38114-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38114-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38114-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38114-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38114-134">INPUTS</span></span>

### <span data-ttu-id="38114-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="38114-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="38114-136">System.String</span><span class="sxs-lookup"><span data-stu-id="38114-136">System.String</span></span>

## <span data-ttu-id="38114-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38114-137">OUTPUTS</span></span>

### <span data-ttu-id="38114-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38114-138">System.Boolean</span></span>

## <span data-ttu-id="38114-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38114-139">NOTES</span></span>

## <span data-ttu-id="38114-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38114-140">RELATED LINKS</span></span>

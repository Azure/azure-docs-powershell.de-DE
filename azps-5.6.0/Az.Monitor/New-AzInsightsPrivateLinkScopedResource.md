---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947368"
---
# <span data-ttu-id="87e49-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="87e49-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="87e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e49-102">SYNOPSIS</span></span>
<span data-ttu-id="87e49-103">Erstellen für eine Ressource mit privatem Linkbereich</span><span class="sxs-lookup"><span data-stu-id="87e49-103">create for private link scoped resource</span></span>

## <span data-ttu-id="87e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87e49-104">SYNTAX</span></span>

### <span data-ttu-id="87e49-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87e49-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87e49-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e49-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87e49-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87e49-107">DESCRIPTION</span></span>
<span data-ttu-id="87e49-108">Erstellen für eine Ressource mit privatem Linkbereich, bereicherte Ressource könnte der Log Analytics-Arbeitsbereich oder die Komponente "Application Insights" sein.</span><span class="sxs-lookup"><span data-stu-id="87e49-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="87e49-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87e49-109">EXAMPLES</span></span>

### <span data-ttu-id="87e49-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87e49-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="87e49-111">Erstellen von Ressourcenbereich "scoped_resource_name", die mit der Komponente "ai_name" verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="87e49-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="87e49-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87e49-112">PARAMETERS</span></span>

### <span data-ttu-id="87e49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e49-113">-DefaultProfile</span></span>
<span data-ttu-id="87e49-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87e49-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e49-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87e49-115">-InputObject</span></span>
<span data-ttu-id="87e49-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="87e49-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="87e49-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="87e49-117">-LinkedResourceId</span></span>
<span data-ttu-id="87e49-118">LA/AI-Ressourcen-ID zu Verknüpfen</span><span class="sxs-lookup"><span data-stu-id="87e49-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e49-119">-Name</span><span class="sxs-lookup"><span data-stu-id="87e49-119">-Name</span></span>
<span data-ttu-id="87e49-120">Name der Bereichsressource</span><span class="sxs-lookup"><span data-stu-id="87e49-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e49-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e49-121">-ResourceGroupName</span></span>
<span data-ttu-id="87e49-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="87e49-122">Resource Group Name</span></span>

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

### <span data-ttu-id="87e49-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="87e49-123">-ScopeName</span></span>
<span data-ttu-id="87e49-124">Name des Privaten Linkbereichs</span><span class="sxs-lookup"><span data-stu-id="87e49-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="87e49-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87e49-125">-Confirm</span></span>
<span data-ttu-id="87e49-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87e49-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87e49-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e49-127">-WhatIf</span></span>
<span data-ttu-id="87e49-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87e49-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87e49-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87e49-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87e49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e49-130">CommonParameters</span></span>
<span data-ttu-id="87e49-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e49-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87e49-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e49-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87e49-133">INPUTS</span></span>

### <span data-ttu-id="87e49-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="87e49-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="87e49-135">System.String</span><span class="sxs-lookup"><span data-stu-id="87e49-135">System.String</span></span>

## <span data-ttu-id="87e49-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87e49-136">OUTPUTS</span></span>

### <span data-ttu-id="87e49-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="87e49-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="87e49-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87e49-138">NOTES</span></span>

## <span data-ttu-id="87e49-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87e49-139">RELATED LINKS</span></span>

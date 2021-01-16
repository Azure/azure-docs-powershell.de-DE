---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305024"
---
# <span data-ttu-id="48daa-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="48daa-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="48daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48daa-102">SYNOPSIS</span></span>
<span data-ttu-id="48daa-103">Erstellen für Ressource mit Bereich "Private Verknüpfung"</span><span class="sxs-lookup"><span data-stu-id="48daa-103">create for private link scoped resource</span></span>

## <span data-ttu-id="48daa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48daa-104">SYNTAX</span></span>

### <span data-ttu-id="48daa-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48daa-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48daa-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48daa-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48daa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48daa-107">DESCRIPTION</span></span>
<span data-ttu-id="48daa-108">für eine Ressource mit Bereich "Privater Link" erstellen, könnte eine Ressource mit Bereichsbereich "Log Analytics Workspace" oder "Application Insights"-Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="48daa-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="48daa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48daa-109">EXAMPLES</span></span>

### <span data-ttu-id="48daa-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48daa-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="48daa-111">Erstellen einer mit der Komponente "scoped_resource_name" verknüpften Bereichsressource "ai_name"</span><span class="sxs-lookup"><span data-stu-id="48daa-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="48daa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48daa-112">PARAMETERS</span></span>

### <span data-ttu-id="48daa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48daa-113">-DefaultProfile</span></span>
<span data-ttu-id="48daa-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48daa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48daa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48daa-115">-InputObject</span></span>
<span data-ttu-id="48daa-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="48daa-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="48daa-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="48daa-117">-LinkedResourceId</span></span>
<span data-ttu-id="48daa-118">LA/AI Resource Id to Link</span><span class="sxs-lookup"><span data-stu-id="48daa-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="48daa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="48daa-119">-Name</span></span>
<span data-ttu-id="48daa-120">Name der ressource mit Bereichsbereich</span><span class="sxs-lookup"><span data-stu-id="48daa-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="48daa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48daa-121">-ResourceGroupName</span></span>
<span data-ttu-id="48daa-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="48daa-122">Resource Group Name</span></span>

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

### <span data-ttu-id="48daa-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="48daa-123">-ScopeName</span></span>
<span data-ttu-id="48daa-124">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="48daa-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="48daa-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48daa-125">-Confirm</span></span>
<span data-ttu-id="48daa-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48daa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48daa-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="48daa-127">-WhatIf</span></span>
<span data-ttu-id="48daa-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48daa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48daa-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48daa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48daa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48daa-130">CommonParameters</span></span>
<span data-ttu-id="48daa-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48daa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48daa-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48daa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48daa-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48daa-133">INPUTS</span></span>

### <span data-ttu-id="48daa-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="48daa-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="48daa-135">System.String</span><span class="sxs-lookup"><span data-stu-id="48daa-135">System.String</span></span>

## <span data-ttu-id="48daa-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48daa-136">OUTPUTS</span></span>

### <span data-ttu-id="48daa-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="48daa-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="48daa-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48daa-138">NOTES</span></span>

## <span data-ttu-id="48daa-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48daa-139">RELATED LINKS</span></span>

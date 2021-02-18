---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173073"
---
# <span data-ttu-id="b571d-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b571d-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b571d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b571d-102">SYNOPSIS</span></span>
<span data-ttu-id="b571d-103">Get for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="b571d-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="b571d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b571d-104">SYNTAX</span></span>

### <span data-ttu-id="b571d-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b571d-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b571d-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b571d-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b571d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b571d-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b571d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b571d-108">DESCRIPTION</span></span>
<span data-ttu-id="b571d-109">"Get or list for private link scoped resource, scoped" could be Log Analytics workspace or Application Insights component</span><span class="sxs-lookup"><span data-stu-id="b571d-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="b571d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b571d-110">EXAMPLES</span></span>

### <span data-ttu-id="b571d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b571d-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="b571d-112">Auflisten einer Ressource mit Bereichsbereich unter privatem Linkbereich "scope_name"</span><span class="sxs-lookup"><span data-stu-id="b571d-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="b571d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b571d-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="b571d-114">Ressource mit Bereichsbereich unter privatem Linkbereich "scope_name" mit dem Namen "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="b571d-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="b571d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b571d-115">PARAMETERS</span></span>

### <span data-ttu-id="b571d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b571d-116">-DefaultProfile</span></span>
<span data-ttu-id="b571d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b571d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b571d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b571d-118">-InputObject</span></span>
<span data-ttu-id="b571d-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b571d-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b571d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b571d-120">-Name</span></span>
<span data-ttu-id="b571d-121">Name der ressource mit Bereichsbereich</span><span class="sxs-lookup"><span data-stu-id="b571d-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b571d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b571d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b571d-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b571d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b571d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b571d-124">-ResourceId</span></span>
<span data-ttu-id="b571d-125">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b571d-125">Resource Id</span></span>

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

### <span data-ttu-id="b571d-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="b571d-126">-ScopeName</span></span>
<span data-ttu-id="b571d-127">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="b571d-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="b571d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b571d-128">CommonParameters</span></span>
<span data-ttu-id="b571d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b571d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b571d-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b571d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b571d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b571d-131">INPUTS</span></span>

### <span data-ttu-id="b571d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b571d-132">System.String</span></span>

## <span data-ttu-id="b571d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b571d-133">OUTPUTS</span></span>

### <span data-ttu-id="b571d-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b571d-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b571d-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b571d-135">NOTES</span></span>

## <span data-ttu-id="b571d-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b571d-136">RELATED LINKS</span></span>

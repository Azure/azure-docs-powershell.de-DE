---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932635"
---
# <span data-ttu-id="fae43-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="fae43-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="fae43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae43-102">SYNOPSIS</span></span>
<span data-ttu-id="fae43-103">Für ressource mit privatem Linkbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="fae43-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="fae43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fae43-104">SYNTAX</span></span>

### <span data-ttu-id="fae43-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fae43-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae43-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae43-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae43-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae43-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fae43-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fae43-108">DESCRIPTION</span></span>
<span data-ttu-id="fae43-109">Eine Liste oder Eine Liste für die Ressource mit privatem Linkbereich kann der Arbeitsbereich "Log Analytics" oder "Application Insights"-Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="fae43-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="fae43-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fae43-110">EXAMPLES</span></span>

### <span data-ttu-id="fae43-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fae43-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="fae43-112">Auflisten einer Ressource mit Bereichsbereich unter privatem Linkbereich "scope_name"</span><span class="sxs-lookup"><span data-stu-id="fae43-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="fae43-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fae43-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="fae43-114">Ressource mit Bereichsbereich unter privatem Linkbereich "scope_name" mit dem Namen "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="fae43-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="fae43-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fae43-115">PARAMETERS</span></span>

### <span data-ttu-id="fae43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae43-116">-DefaultProfile</span></span>
<span data-ttu-id="fae43-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fae43-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae43-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fae43-118">-InputObject</span></span>
<span data-ttu-id="fae43-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fae43-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="fae43-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fae43-120">-Name</span></span>
<span data-ttu-id="fae43-121">Name der Bereichsressource</span><span class="sxs-lookup"><span data-stu-id="fae43-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="fae43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae43-122">-ResourceGroupName</span></span>
<span data-ttu-id="fae43-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fae43-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fae43-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fae43-124">-ResourceId</span></span>
<span data-ttu-id="fae43-125">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fae43-125">Resource Id</span></span>

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

### <span data-ttu-id="fae43-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="fae43-126">-ScopeName</span></span>
<span data-ttu-id="fae43-127">Name des Privaten Linkbereichs</span><span class="sxs-lookup"><span data-stu-id="fae43-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="fae43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae43-128">CommonParameters</span></span>
<span data-ttu-id="fae43-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae43-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fae43-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae43-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fae43-131">INPUTS</span></span>

### <span data-ttu-id="fae43-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fae43-132">System.String</span></span>

## <span data-ttu-id="fae43-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fae43-133">OUTPUTS</span></span>

### <span data-ttu-id="fae43-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="fae43-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="fae43-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fae43-135">NOTES</span></span>

## <span data-ttu-id="fae43-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fae43-136">RELATED LINKS</span></span>

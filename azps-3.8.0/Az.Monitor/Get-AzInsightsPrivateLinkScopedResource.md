---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996572"
---
# <span data-ttu-id="62b94-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="62b94-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="62b94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62b94-102">SYNOPSIS</span></span>
<span data-ttu-id="62b94-103">Ressource für privaten Link mit Gültigkeitsbereich abrufen</span><span class="sxs-lookup"><span data-stu-id="62b94-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="62b94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62b94-104">SYNTAX</span></span>

### <span data-ttu-id="62b94-105">ByScopeParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="62b94-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62b94-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b94-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62b94-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b94-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62b94-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62b94-108">DESCRIPTION</span></span>
<span data-ttu-id="62b94-109">Abrufen oder auflisten für eine Ressource mit Gültigkeitsbereich für privaten Link, Bereichs Ressource könnte Protokollanalyse-Arbeitsbereich oder Anwendungs Einblicke-Komponente sein</span><span class="sxs-lookup"><span data-stu-id="62b94-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="62b94-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62b94-110">EXAMPLES</span></span>

### <span data-ttu-id="62b94-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62b94-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="62b94-112">Liste der bereichsbezogenen Ressourcen im Bereich "privater Link" "scope_name"</span><span class="sxs-lookup"><span data-stu-id="62b94-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="62b94-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="62b94-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="62b94-114">Abrufen einer bereichsbezogenen Ressource unter einem privaten Linkbereich "scope_name" mit dem Namen "scoped_resource_name"</span><span class="sxs-lookup"><span data-stu-id="62b94-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="62b94-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="62b94-115">PARAMETERS</span></span>

### <span data-ttu-id="62b94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b94-116">-DefaultProfile</span></span>
<span data-ttu-id="62b94-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62b94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b94-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62b94-118">-InputObject</span></span>
<span data-ttu-id="62b94-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="62b94-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="62b94-120">-Name</span><span class="sxs-lookup"><span data-stu-id="62b94-120">-Name</span></span>
<span data-ttu-id="62b94-121">Name der Bereichs Ressource</span><span class="sxs-lookup"><span data-stu-id="62b94-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="62b94-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b94-122">-ResourceGroupName</span></span>
<span data-ttu-id="62b94-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="62b94-123">Resource Group Name</span></span>

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

### <span data-ttu-id="62b94-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="62b94-124">-ResourceId</span></span>
<span data-ttu-id="62b94-125">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="62b94-125">Resource Id</span></span>

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

### <span data-ttu-id="62b94-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="62b94-126">-ScopeName</span></span>
<span data-ttu-id="62b94-127">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="62b94-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="62b94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b94-128">CommonParameters</span></span>
<span data-ttu-id="62b94-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b94-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62b94-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b94-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62b94-131">INPUTS</span></span>

### <span data-ttu-id="62b94-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62b94-132">System.String</span></span>

## <span data-ttu-id="62b94-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62b94-133">OUTPUTS</span></span>

### <span data-ttu-id="62b94-134">icrosoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="62b94-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="62b94-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="62b94-135">NOTES</span></span>

## <span data-ttu-id="62b94-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62b94-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385691"
---
# <span data-ttu-id="23635-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="23635-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="23635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23635-102">SYNOPSIS</span></span>
<span data-ttu-id="23635-103">Bereich für private Verknüpfungen erhalten</span><span class="sxs-lookup"><span data-stu-id="23635-103">Get private link scope</span></span>

## <span data-ttu-id="23635-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23635-104">SYNTAX</span></span>

### <span data-ttu-id="23635-105">ByResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23635-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23635-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23635-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23635-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23635-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23635-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23635-108">DESCRIPTION</span></span>
<span data-ttu-id="23635-109">Auflisten oder Erhalten des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="23635-109">List or get private link scope</span></span> 

## <span data-ttu-id="23635-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23635-110">EXAMPLES</span></span>

### <span data-ttu-id="23635-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23635-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="23635-112">Auflisten privater Linkbereiche unter der Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="23635-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="23635-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="23635-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="23635-114">Bereich für private Verknüpfungen mit dem Namen "scope_name" unter der Ressourcengruppe "rg_name"</span><span class="sxs-lookup"><span data-stu-id="23635-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="23635-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23635-115">PARAMETERS</span></span>

### <span data-ttu-id="23635-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23635-116">-DefaultProfile</span></span>
<span data-ttu-id="23635-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23635-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23635-118">-Name</span><span class="sxs-lookup"><span data-stu-id="23635-118">-Name</span></span>
<span data-ttu-id="23635-119">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="23635-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="23635-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23635-120">-ResourceGroupName</span></span>
<span data-ttu-id="23635-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="23635-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="23635-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23635-122">-ResourceId</span></span>
<span data-ttu-id="23635-123">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="23635-123">Resource Id</span></span>

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

### <span data-ttu-id="23635-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23635-124">CommonParameters</span></span>
<span data-ttu-id="23635-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23635-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23635-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23635-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23635-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23635-127">INPUTS</span></span>

### <span data-ttu-id="23635-128">System.String</span><span class="sxs-lookup"><span data-stu-id="23635-128">System.String</span></span>

## <span data-ttu-id="23635-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23635-129">OUTPUTS</span></span>

### <span data-ttu-id="23635-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="23635-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="23635-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23635-131">NOTES</span></span>

## <span data-ttu-id="23635-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23635-132">RELATED LINKS</span></span>

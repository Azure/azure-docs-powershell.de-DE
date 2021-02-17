---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169560"
---
# <span data-ttu-id="8cb52-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="8cb52-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="8cb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cb52-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb52-103">Löschen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="8cb52-103">Delete cluster</span></span>

## <span data-ttu-id="8cb52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cb52-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb52-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cb52-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb52-106">Löschen eines Clusters, gilt nur für Cluster mit dem Bereitstellungszustand "Succeeded"</span><span class="sxs-lookup"><span data-stu-id="8cb52-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="8cb52-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cb52-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb52-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cb52-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="8cb52-109">Löschen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="8cb52-109">Delete cluster</span></span>

## <span data-ttu-id="8cb52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cb52-110">PARAMETERS</span></span>

### <span data-ttu-id="8cb52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cb52-111">-AsJob</span></span>
<span data-ttu-id="8cb52-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8cb52-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8cb52-113">-ClusterName</span></span>
<span data-ttu-id="8cb52-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="8cb52-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb52-115">-DefaultProfile</span></span>
<span data-ttu-id="8cb52-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb52-117">-ResourceGroupName</span></span>
<span data-ttu-id="8cb52-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8cb52-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cb52-119">-Confirm</span></span>
<span data-ttu-id="8cb52-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cb52-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8cb52-121">-WhatIf</span></span>
<span data-ttu-id="8cb52-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb52-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb52-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb52-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb52-124">CommonParameters</span></span>
<span data-ttu-id="8cb52-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb52-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cb52-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb52-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cb52-127">INPUTS</span></span>

### <span data-ttu-id="8cb52-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8cb52-128">System.String</span></span>

## <span data-ttu-id="8cb52-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cb52-129">OUTPUTS</span></span>

### <span data-ttu-id="8cb52-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8cb52-130">System.Boolean</span></span>

## <span data-ttu-id="8cb52-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8cb52-131">NOTES</span></span>

## <span data-ttu-id="8cb52-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8cb52-132">RELATED LINKS</span></span>

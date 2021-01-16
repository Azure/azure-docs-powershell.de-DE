---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358166"
---
# <span data-ttu-id="1cff2-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="1cff2-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="1cff2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cff2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cff2-103">Cluster löschen</span><span class="sxs-lookup"><span data-stu-id="1cff2-103">Delete cluster</span></span>

## <span data-ttu-id="1cff2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cff2-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cff2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cff2-105">DESCRIPTION</span></span>
<span data-ttu-id="1cff2-106">Cluster löschen, nur auf Cluster mit Bereitstellungszustand "Succeeded" anwenden</span><span class="sxs-lookup"><span data-stu-id="1cff2-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="1cff2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1cff2-107">EXAMPLES</span></span>

### <span data-ttu-id="1cff2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1cff2-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="1cff2-109">Cluster löschen</span><span class="sxs-lookup"><span data-stu-id="1cff2-109">Delete cluster</span></span>

## <span data-ttu-id="1cff2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cff2-110">PARAMETERS</span></span>

### <span data-ttu-id="1cff2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cff2-111">-AsJob</span></span>
<span data-ttu-id="1cff2-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1cff2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cff2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1cff2-113">-ClusterName</span></span>
<span data-ttu-id="1cff2-114">Der Clustername.</span><span class="sxs-lookup"><span data-stu-id="1cff2-114">The cluster name.</span></span>

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

### <span data-ttu-id="1cff2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cff2-115">-DefaultProfile</span></span>
<span data-ttu-id="1cff2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cff2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cff2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cff2-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cff2-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1cff2-118">The resource group name.</span></span>

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

### <span data-ttu-id="1cff2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cff2-119">-Confirm</span></span>
<span data-ttu-id="1cff2-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cff2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cff2-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1cff2-121">-WhatIf</span></span>
<span data-ttu-id="1cff2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cff2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cff2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cff2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cff2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cff2-124">CommonParameters</span></span>
<span data-ttu-id="1cff2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cff2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cff2-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cff2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cff2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1cff2-127">INPUTS</span></span>

### <span data-ttu-id="1cff2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1cff2-128">System.String</span></span>

## <span data-ttu-id="1cff2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1cff2-129">OUTPUTS</span></span>

### <span data-ttu-id="1cff2-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cff2-130">System.Boolean</span></span>

## <span data-ttu-id="1cff2-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1cff2-131">NOTES</span></span>

## <span data-ttu-id="1cff2-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1cff2-132">RELATED LINKS</span></span>

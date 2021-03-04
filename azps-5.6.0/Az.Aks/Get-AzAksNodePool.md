---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 4d6fab247a56054b8c78914f5e47bc5737f8828f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926067"
---
# <span data-ttu-id="299ee-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="299ee-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="299ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299ee-102">SYNOPSIS</span></span>
<span data-ttu-id="299ee-103">Erstellen Sie den Notizenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="299ee-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="299ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="299ee-104">SYNTAX</span></span>

### <span data-ttu-id="299ee-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="299ee-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299ee-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="299ee-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299ee-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="299ee-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299ee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="299ee-108">DESCRIPTION</span></span>
<span data-ttu-id="299ee-109">Erstellen Sie den Notizenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="299ee-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="299ee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="299ee-110">EXAMPLES</span></span>

### <span data-ttu-id="299ee-111">Alle Knotenpools innerhalb eines angegebenen Clusters erhalten</span><span class="sxs-lookup"><span data-stu-id="299ee-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="299ee-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="299ee-112">PARAMETERS</span></span>

### <span data-ttu-id="299ee-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="299ee-113">-ClusterName</span></span>
<span data-ttu-id="299ee-114">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="299ee-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299ee-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="299ee-115">-ClusterObject</span></span>
<span data-ttu-id="299ee-116">Das Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="299ee-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="299ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299ee-117">-DefaultProfile</span></span>
<span data-ttu-id="299ee-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="299ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299ee-119">-ID</span><span class="sxs-lookup"><span data-stu-id="299ee-119">-Id</span></span>
<span data-ttu-id="299ee-120">ID eines Knotenpools im verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="299ee-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299ee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="299ee-121">-Name</span></span>
<span data-ttu-id="299ee-122">Der Name des Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="299ee-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="299ee-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="299ee-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299ee-125">CommonParameters</span></span>
<span data-ttu-id="299ee-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299ee-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="299ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299ee-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="299ee-128">INPUTS</span></span>

### <span data-ttu-id="299ee-129">System.String</span><span class="sxs-lookup"><span data-stu-id="299ee-129">System.String</span></span>

## <span data-ttu-id="299ee-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="299ee-130">OUTPUTS</span></span>

### <span data-ttu-id="299ee-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="299ee-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="299ee-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="299ee-132">NOTES</span></span>

## <span data-ttu-id="299ee-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="299ee-133">RELATED LINKS</span></span>

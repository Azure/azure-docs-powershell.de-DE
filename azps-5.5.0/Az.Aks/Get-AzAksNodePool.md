---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167105"
---
# <span data-ttu-id="b11ba-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="b11ba-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="b11ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b11ba-103">Erstellen Sie einen Notizenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="b11ba-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b11ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b11ba-104">SYNTAX</span></span>

### <span data-ttu-id="b11ba-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b11ba-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b11ba-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b11ba-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b11ba-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b11ba-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11ba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b11ba-108">DESCRIPTION</span></span>
<span data-ttu-id="b11ba-109">Erstellen Sie einen Notizenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="b11ba-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b11ba-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b11ba-110">EXAMPLES</span></span>

### <span data-ttu-id="b11ba-111">Alle Knotenpools innerhalb eines angegebenen Clusters erhalten</span><span class="sxs-lookup"><span data-stu-id="b11ba-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="b11ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b11ba-112">PARAMETERS</span></span>

### <span data-ttu-id="b11ba-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b11ba-113">-ClusterName</span></span>
<span data-ttu-id="b11ba-114">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="b11ba-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="b11ba-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b11ba-115">-ClusterObject</span></span>
<span data-ttu-id="b11ba-116">Das Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="b11ba-116">The cluster object.</span></span>

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

### <span data-ttu-id="b11ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11ba-117">-DefaultProfile</span></span>
<span data-ttu-id="b11ba-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b11ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b11ba-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b11ba-119">-Id</span></span>
<span data-ttu-id="b11ba-120">ID eines Knotenpools im verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="b11ba-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="b11ba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b11ba-121">-Name</span></span>
<span data-ttu-id="b11ba-122">Der Name des Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="b11ba-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="b11ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="b11ba-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b11ba-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b11ba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11ba-125">CommonParameters</span></span>
<span data-ttu-id="b11ba-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11ba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11ba-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b11ba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11ba-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b11ba-128">INPUTS</span></span>

### <span data-ttu-id="b11ba-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b11ba-129">System.String</span></span>

## <span data-ttu-id="b11ba-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b11ba-130">OUTPUTS</span></span>

### <span data-ttu-id="b11ba-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="b11ba-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="b11ba-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b11ba-132">NOTES</span></span>

## <span data-ttu-id="b11ba-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b11ba-133">RELATED LINKS</span></span>

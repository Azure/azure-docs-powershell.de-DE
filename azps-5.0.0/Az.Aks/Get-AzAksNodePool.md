---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177323"
---
# <span data-ttu-id="9e3aa-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="9e3aa-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="9e3aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3aa-103">Erstellen eines Notizen Pools in einem bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="9e3aa-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="9e3aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e3aa-104">SYNTAX</span></span>

### <span data-ttu-id="9e3aa-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e3aa-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3aa-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3aa-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3aa-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3aa-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3aa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e3aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9e3aa-109">Erstellen eines Notizen Pools in einem bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="9e3aa-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="9e3aa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e3aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9e3aa-111">Abrufen aller Knoten Pools innerhalb des angegebenen Clusters</span><span class="sxs-lookup"><span data-stu-id="9e3aa-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="9e3aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e3aa-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3aa-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="9e3aa-113">-ClusterName</span></span>
<span data-ttu-id="9e3aa-114">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="9e3aa-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="9e3aa-115">-ClusterObject</span></span>
<span data-ttu-id="9e3aa-116">Das Clusterobjekt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-116">The cluster object.</span></span>

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

### <span data-ttu-id="9e3aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3aa-117">-DefaultProfile</span></span>
<span data-ttu-id="9e3aa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3aa-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9e3aa-119">-Id</span></span>
<span data-ttu-id="9e3aa-120">ID eines Knoten Pools in verwaltetem Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="9e3aa-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9e3aa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9e3aa-121">-Name</span></span>
<span data-ttu-id="9e3aa-122">Der Name des Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="9e3aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e3aa-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e3aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3aa-125">CommonParameters</span></span>
<span data-ttu-id="9e3aa-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3aa-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3aa-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e3aa-128">INPUTS</span></span>

### <span data-ttu-id="9e3aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3aa-129">System.String</span></span>

## <span data-ttu-id="9e3aa-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e3aa-130">OUTPUTS</span></span>

### <span data-ttu-id="9e3aa-131">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="9e3aa-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="9e3aa-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e3aa-132">NOTES</span></span>

## <span data-ttu-id="9e3aa-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e3aa-133">RELATED LINKS</span></span>

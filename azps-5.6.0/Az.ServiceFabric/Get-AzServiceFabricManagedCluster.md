---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 5a67faaf48d96a93fe1bc3e6380abb4fe6d03d98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920432"
---
# <span data-ttu-id="c613e-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c613e-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="c613e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c613e-102">SYNOPSIS</span></span>
<span data-ttu-id="c613e-103">Hier erhalten Sie die Ressourcendetails für verwaltete Cluster.</span><span class="sxs-lookup"><span data-stu-id="c613e-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="c613e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c613e-104">SYNTAX</span></span>

### <span data-ttu-id="c613e-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="c613e-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c613e-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c613e-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c613e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c613e-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c613e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c613e-108">DESCRIPTION</span></span>
<span data-ttu-id="c613e-109">Hier erhalten Sie die Ressourcendetails für verwaltete Cluster.</span><span class="sxs-lookup"><span data-stu-id="c613e-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="c613e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c613e-110">EXAMPLES</span></span>

### <span data-ttu-id="c613e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c613e-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="c613e-112">Erhalten Sie Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="c613e-112">Get cluster details.</span></span>

### <span data-ttu-id="c613e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c613e-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="c613e-114">Holen Sie sich eine Liste der Cluster unter der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c613e-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="c613e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c613e-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="c613e-116">Holen Sie sich eine Liste der Cluster unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c613e-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="c613e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c613e-117">PARAMETERS</span></span>

### <span data-ttu-id="c613e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c613e-118">-DefaultProfile</span></span>
<span data-ttu-id="c613e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c613e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c613e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c613e-120">-Name</span></span>
<span data-ttu-id="c613e-121">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c613e-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c613e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c613e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c613e-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c613e-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c613e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c613e-124">CommonParameters</span></span>
<span data-ttu-id="c613e-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c613e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c613e-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c613e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c613e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c613e-127">INPUTS</span></span>

### <span data-ttu-id="c613e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c613e-128">System.String</span></span>

## <span data-ttu-id="c613e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c613e-129">OUTPUTS</span></span>

### <span data-ttu-id="c613e-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c613e-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="c613e-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c613e-131">NOTES</span></span>

## <span data-ttu-id="c613e-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c613e-132">RELATED LINKS</span></span>

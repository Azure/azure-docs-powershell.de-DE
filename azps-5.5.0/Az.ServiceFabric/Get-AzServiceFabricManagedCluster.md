---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173977"
---
# <span data-ttu-id="7729d-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7729d-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="7729d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7729d-102">SYNOPSIS</span></span>
<span data-ttu-id="7729d-103">Erhalten Sie die Details der verwalteten Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="7729d-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7729d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7729d-104">SYNTAX</span></span>

### <span data-ttu-id="7729d-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="7729d-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7729d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7729d-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7729d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7729d-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7729d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7729d-108">DESCRIPTION</span></span>
<span data-ttu-id="7729d-109">Erhalten Sie die Details der verwalteten Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="7729d-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7729d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7729d-110">EXAMPLES</span></span>

### <span data-ttu-id="7729d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7729d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="7729d-112">Erhalten Sie Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="7729d-112">Get cluster details.</span></span>

### <span data-ttu-id="7729d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7729d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="7729d-114">Hier finden Sie eine Liste von Clustern unter der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7729d-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="7729d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7729d-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="7729d-116">Holen Sie sich die Liste der Cluster unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7729d-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="7729d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7729d-117">PARAMETERS</span></span>

### <span data-ttu-id="7729d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7729d-118">-DefaultProfile</span></span>
<span data-ttu-id="7729d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7729d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7729d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7729d-120">-Name</span></span>
<span data-ttu-id="7729d-121">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="7729d-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7729d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7729d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7729d-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7729d-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7729d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7729d-124">CommonParameters</span></span>
<span data-ttu-id="7729d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7729d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7729d-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7729d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7729d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7729d-127">INPUTS</span></span>

### <span data-ttu-id="7729d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7729d-128">System.String</span></span>

## <span data-ttu-id="7729d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7729d-129">OUTPUTS</span></span>

### <span data-ttu-id="7729d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7729d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7729d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7729d-131">NOTES</span></span>

## <span data-ttu-id="7729d-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7729d-132">RELATED LINKS</span></span>

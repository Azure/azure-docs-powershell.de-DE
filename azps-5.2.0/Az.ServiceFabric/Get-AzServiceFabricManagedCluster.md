---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303000"
---
# <span data-ttu-id="04c6c-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="04c6c-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="04c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="04c6c-103">Erhalten Sie die Details der verwalteten Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="04c6c-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="04c6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04c6c-104">SYNTAX</span></span>

### <span data-ttu-id="04c6c-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="04c6c-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04c6c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04c6c-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04c6c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="04c6c-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c6c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04c6c-108">DESCRIPTION</span></span>
<span data-ttu-id="04c6c-109">Erhalten Sie die Details der verwalteten Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="04c6c-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="04c6c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04c6c-110">EXAMPLES</span></span>

### <span data-ttu-id="04c6c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04c6c-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="04c6c-112">Erhalten Sie Clusterdetails.</span><span class="sxs-lookup"><span data-stu-id="04c6c-112">Get cluster details.</span></span>

### <span data-ttu-id="04c6c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="04c6c-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="04c6c-114">Hier finden Sie eine Liste von Clustern unter der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04c6c-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="04c6c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="04c6c-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="04c6c-116">Holen Sie sich die Liste der Cluster unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04c6c-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="04c6c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="04c6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c6c-118">-DefaultProfile</span></span>
<span data-ttu-id="04c6c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04c6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c6c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="04c6c-120">-Name</span></span>
<span data-ttu-id="04c6c-121">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="04c6c-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="04c6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="04c6c-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="04c6c-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="04c6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c6c-124">CommonParameters</span></span>
<span data-ttu-id="04c6c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c6c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04c6c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c6c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04c6c-127">INPUTS</span></span>

### <span data-ttu-id="04c6c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="04c6c-128">System.String</span></span>

## <span data-ttu-id="04c6c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04c6c-129">OUTPUTS</span></span>

### <span data-ttu-id="04c6c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="04c6c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="04c6c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04c6c-131">NOTES</span></span>

## <span data-ttu-id="04c6c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04c6c-132">RELATED LINKS</span></span>

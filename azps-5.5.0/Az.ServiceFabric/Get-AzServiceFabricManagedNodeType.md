---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173969"
---
# <span data-ttu-id="55403-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="55403-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="55403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55403-102">SYNOPSIS</span></span>
<span data-ttu-id="55403-103">Ressourcendetails für verwaltete Knotentypen</span><span class="sxs-lookup"><span data-stu-id="55403-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="55403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55403-104">SYNTAX</span></span>

### <span data-ttu-id="55403-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="55403-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55403-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55403-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55403-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55403-107">DESCRIPTION</span></span>
<span data-ttu-id="55403-108">Ressourcendetails für verwaltete Knotentypen</span><span class="sxs-lookup"><span data-stu-id="55403-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="55403-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55403-109">EXAMPLES</span></span>

### <span data-ttu-id="55403-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55403-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="55403-111">Details zum Knotentyp erhalten.</span><span class="sxs-lookup"><span data-stu-id="55403-111">Get node type details.</span></span>

### <span data-ttu-id="55403-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55403-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="55403-113">Liste der Knotentypen unter dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="55403-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="55403-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55403-114">PARAMETERS</span></span>

### <span data-ttu-id="55403-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="55403-115">-ClusterName</span></span>
<span data-ttu-id="55403-116">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="55403-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55403-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55403-117">-DefaultProfile</span></span>
<span data-ttu-id="55403-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55403-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55403-119">-Name</span><span class="sxs-lookup"><span data-stu-id="55403-119">-Name</span></span>
<span data-ttu-id="55403-120">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="55403-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55403-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55403-121">-ResourceGroupName</span></span>
<span data-ttu-id="55403-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="55403-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55403-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55403-123">CommonParameters</span></span>
<span data-ttu-id="55403-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55403-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55403-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55403-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55403-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55403-126">INPUTS</span></span>

### <span data-ttu-id="55403-127">System.String</span><span class="sxs-lookup"><span data-stu-id="55403-127">System.String</span></span>

## <span data-ttu-id="55403-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55403-128">OUTPUTS</span></span>

### <span data-ttu-id="55403-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="55403-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="55403-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55403-130">NOTES</span></span>

## <span data-ttu-id="55403-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55403-131">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924424"
---
# <span data-ttu-id="600c2-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="600c2-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="600c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600c2-102">SYNOPSIS</span></span>
<span data-ttu-id="600c2-103">Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="600c2-103">Get Service Fabric application details.</span></span> <span data-ttu-id="600c2-104">Unterstützt nur ARM bereitgestellte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="600c2-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="600c2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="600c2-105">SYNTAX</span></span>

### <span data-ttu-id="600c2-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="600c2-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600c2-107">ByName</span><span class="sxs-lookup"><span data-stu-id="600c2-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600c2-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="600c2-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="600c2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="600c2-109">DESCRIPTION</span></span>
<span data-ttu-id="600c2-110">Dieses Cmdlet ruft die Anwendungsdetails in der angegebenen Ressourcengruppe und dem angegebenen Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="600c2-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="600c2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="600c2-111">EXAMPLES</span></span>

### <span data-ttu-id="600c2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="600c2-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="600c2-113">In diesem Beispiel werden die Anwendungsressourcendetails für die Anwendung "testApp" ab.</span><span class="sxs-lookup"><span data-stu-id="600c2-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="600c2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="600c2-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="600c2-115">In diesem Beispiel wird eine Liste der Anwendungen unter dem Cluster "testCluster" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="600c2-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="600c2-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="600c2-116">PARAMETERS</span></span>

### <span data-ttu-id="600c2-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="600c2-117">-ClusterName</span></span>
<span data-ttu-id="600c2-118">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="600c2-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600c2-119">-DefaultProfile</span></span>
<span data-ttu-id="600c2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="600c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600c2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="600c2-121">-Name</span></span>
<span data-ttu-id="600c2-122">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="600c2-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="600c2-124">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="600c2-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600c2-125">-ResourceId</span></span>
<span data-ttu-id="600c2-126">Arm ResourceId der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="600c2-126">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600c2-127">CommonParameters</span></span>
<span data-ttu-id="600c2-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600c2-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="600c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600c2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="600c2-130">INPUTS</span></span>

### <span data-ttu-id="600c2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="600c2-131">System.String</span></span>

## <span data-ttu-id="600c2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="600c2-132">OUTPUTS</span></span>

### <span data-ttu-id="600c2-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="600c2-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="600c2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="600c2-134">NOTES</span></span>

## <span data-ttu-id="600c2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="600c2-135">RELATED LINKS</span></span>

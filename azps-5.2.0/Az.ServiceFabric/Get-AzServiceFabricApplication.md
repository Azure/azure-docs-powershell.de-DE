---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289817"
---
# <span data-ttu-id="40c2b-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="40c2b-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="40c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="40c2b-103">Erhalten Sie Service Fabric-Anwendungsdetails.</span><span class="sxs-lookup"><span data-stu-id="40c2b-103">Get Service Fabric application details.</span></span> <span data-ttu-id="40c2b-104">Unterstützt nur ARM bereitgestellten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="40c2b-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="40c2b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40c2b-105">SYNTAX</span></span>

### <span data-ttu-id="40c2b-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="40c2b-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40c2b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="40c2b-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40c2b-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40c2b-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40c2b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40c2b-109">DESCRIPTION</span></span>
<span data-ttu-id="40c2b-110">Dieses Cmdlet ruft die Anwendungsdetails in der angegebenen Ressourcengruppe und dem angegebenen Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="40c2b-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="40c2b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40c2b-111">EXAMPLES</span></span>

### <span data-ttu-id="40c2b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40c2b-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="40c2b-113">In diesem Beispiel werden die Anwendungsressourcendetails für die Anwendung "testApp" ruft.</span><span class="sxs-lookup"><span data-stu-id="40c2b-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="40c2b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="40c2b-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="40c2b-115">Dieses Beispiel ruft eine Liste der Anwendungen unter dem Cluster "testCluster" ab.</span><span class="sxs-lookup"><span data-stu-id="40c2b-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="40c2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40c2b-116">PARAMETERS</span></span>

### <span data-ttu-id="40c2b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="40c2b-117">-ClusterName</span></span>
<span data-ttu-id="40c2b-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="40c2b-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="40c2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c2b-119">-DefaultProfile</span></span>
<span data-ttu-id="40c2b-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40c2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c2b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40c2b-121">-Name</span></span>
<span data-ttu-id="40c2b-122">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="40c2b-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="40c2b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c2b-123">-ResourceGroupName</span></span>
<span data-ttu-id="40c2b-124">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="40c2b-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="40c2b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40c2b-125">-ResourceId</span></span>
<span data-ttu-id="40c2b-126">Arm ResourceId der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="40c2b-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="40c2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c2b-127">CommonParameters</span></span>
<span data-ttu-id="40c2b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c2b-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40c2b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c2b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40c2b-130">INPUTS</span></span>

### <span data-ttu-id="40c2b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="40c2b-131">System.String</span></span>

## <span data-ttu-id="40c2b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40c2b-132">OUTPUTS</span></span>

### <span data-ttu-id="40c2b-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="40c2b-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="40c2b-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40c2b-134">NOTES</span></span>

## <span data-ttu-id="40c2b-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40c2b-135">RELATED LINKS</span></span>

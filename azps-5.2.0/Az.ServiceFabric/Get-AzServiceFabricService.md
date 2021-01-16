---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289816"
---
# <span data-ttu-id="9f8f7-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="9f8f7-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="9f8f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8f7-103">Service Fabric service details under the specified application and cluster.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="9f8f7-104">Unterstützt nur ARM bereitgestellten Dienste.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="9f8f7-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f8f7-105">SYNTAX</span></span>

### <span data-ttu-id="9f8f7-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f8f7-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f8f7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9f8f7-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f8f7-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f8f7-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f8f7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f8f7-109">DESCRIPTION</span></span>
<span data-ttu-id="9f8f7-110">Dieses Cmdlet gibt die Dienstdetails in der angegebenen Anwendung und dem angegebenen Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="9f8f7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f8f7-111">EXAMPLES</span></span>

### <span data-ttu-id="9f8f7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f8f7-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="9f8f7-113">In diesem Beispiel werden die Dienstressourcendetails für den Dienst "testApp~testService" ruft.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="9f8f7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9f8f7-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="9f8f7-115">In diesem Beispiel wird eine Liste der Dienste unter der Anwendung "testApp" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="9f8f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f8f7-116">PARAMETERS</span></span>

### <span data-ttu-id="9f8f7-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9f8f7-117">-ApplicationName</span></span>
<span data-ttu-id="9f8f7-118">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8f7-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9f8f7-119">-ClusterName</span></span>
<span data-ttu-id="9f8f7-120">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9f8f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8f7-121">-DefaultProfile</span></span>
<span data-ttu-id="9f8f7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8f7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9f8f7-123">-Name</span></span>
<span data-ttu-id="9f8f7-124">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f8f7-126">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9f8f7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f8f7-127">-ResourceId</span></span>
<span data-ttu-id="9f8f7-128">Arm ResourceId des Diensts.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="9f8f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8f7-129">CommonParameters</span></span>
<span data-ttu-id="9f8f7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8f7-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f8f7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8f7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f8f7-132">INPUTS</span></span>

### <span data-ttu-id="9f8f7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9f8f7-133">System.String</span></span>

## <span data-ttu-id="9f8f7-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f8f7-134">OUTPUTS</span></span>

### <span data-ttu-id="9f8f7-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="9f8f7-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="9f8f7-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f8f7-136">NOTES</span></span>

## <span data-ttu-id="9f8f7-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f8f7-137">RELATED LINKS</span></span>

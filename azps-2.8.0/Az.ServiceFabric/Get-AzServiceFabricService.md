---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 3076a405c47f165d2ace1e5251644cf4e4484a03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823183"
---
# <span data-ttu-id="38d1c-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="38d1c-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="38d1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="38d1c-103">Informationen zum Service Fabric-Dienst finden Sie unter der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="38d1c-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="38d1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d1c-104">SYNTAX</span></span>

### <span data-ttu-id="38d1c-105">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="38d1c-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d1c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="38d1c-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d1c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38d1c-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="38d1c-109">Dieses Cmdlet erhält die Dienstdetails in der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="38d1c-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="38d1c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38d1c-110">EXAMPLES</span></span>

### <span data-ttu-id="38d1c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38d1c-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="38d1c-112">In diesem Beispiel werden die Dienst Ressourcendetails für den Dienst "testApp ~ Test Service" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="38d1c-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="38d1c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="38d1c-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="38d1c-114">In diesem Beispiel wird eine Liste der Dienste unter dem Anwendung "testApp" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="38d1c-114">This example gets a list of the services under the aplication "testApp".</span></span>

## <span data-ttu-id="38d1c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d1c-115">PARAMETERS</span></span>

### <span data-ttu-id="38d1c-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="38d1c-116">-ApplicationName</span></span>
<span data-ttu-id="38d1c-117">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="38d1c-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="38d1c-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="38d1c-118">-ClusterName</span></span>
<span data-ttu-id="38d1c-119">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="38d1c-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="38d1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d1c-120">-DefaultProfile</span></span>
<span data-ttu-id="38d1c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38d1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="38d1c-122">-Name</span></span>
<span data-ttu-id="38d1c-123">Geben Sie den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="38d1c-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="38d1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="38d1c-125">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="38d1c-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="38d1c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="38d1c-126">-ResourceId</span></span>
<span data-ttu-id="38d1c-127">Arm-resourcecode des Diensts.</span><span class="sxs-lookup"><span data-stu-id="38d1c-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="38d1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d1c-128">CommonParameters</span></span>
<span data-ttu-id="38d1c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d1c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d1c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38d1c-131">INPUTS</span></span>

### <span data-ttu-id="38d1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="38d1c-132">System.String</span></span>

## <span data-ttu-id="38d1c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38d1c-133">OUTPUTS</span></span>

### <span data-ttu-id="38d1c-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="38d1c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="38d1c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="38d1c-135">NOTES</span></span>

## <span data-ttu-id="38d1c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38d1c-136">RELATED LINKS</span></span>

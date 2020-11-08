---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004497"
---
# <span data-ttu-id="1923b-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1923b-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1923b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1923b-102">SYNOPSIS</span></span>
<span data-ttu-id="1923b-103">Abrufen von Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1923b-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="1923b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1923b-104">SYNTAX</span></span>

### <span data-ttu-id="1923b-105">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="1923b-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1923b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1923b-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1923b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1923b-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1923b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1923b-108">DESCRIPTION</span></span>
<span data-ttu-id="1923b-109">Dieses Cmdlet ruft die Anwendungsdetails in der angegebenen Ressourcengruppe und dem angegebenen Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="1923b-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="1923b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1923b-110">EXAMPLES</span></span>

### <span data-ttu-id="1923b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1923b-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="1923b-112">In diesem Beispiel werden die Details der Anwendungsressource für die Anwendung "testApp" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1923b-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="1923b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1923b-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="1923b-114">In diesem Beispiel wird eine Liste der Anwendungen unter dem Cluster "testCluster" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1923b-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="1923b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1923b-115">PARAMETERS</span></span>

### <span data-ttu-id="1923b-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1923b-116">-ClusterName</span></span>
<span data-ttu-id="1923b-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="1923b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1923b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1923b-118">-DefaultProfile</span></span>
<span data-ttu-id="1923b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1923b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1923b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1923b-120">-Name</span></span>
<span data-ttu-id="1923b-121">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="1923b-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="1923b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1923b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1923b-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1923b-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1923b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1923b-124">-ResourceId</span></span>
<span data-ttu-id="1923b-125">Arm-Quell Code der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1923b-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="1923b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1923b-126">CommonParameters</span></span>
<span data-ttu-id="1923b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1923b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1923b-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1923b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1923b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1923b-129">INPUTS</span></span>

### <span data-ttu-id="1923b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1923b-130">System.String</span></span>

## <span data-ttu-id="1923b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1923b-131">OUTPUTS</span></span>

### <span data-ttu-id="1923b-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1923b-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1923b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1923b-133">NOTES</span></span>

## <span data-ttu-id="1923b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1923b-134">RELATED LINKS</span></span>

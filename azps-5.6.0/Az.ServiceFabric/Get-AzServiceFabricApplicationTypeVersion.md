---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929771"
---
# <span data-ttu-id="7f29c-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7f29c-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="7f29c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f29c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f29c-103">Details zur Version des Service Fabric-Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="7f29c-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="7f29c-104">Unterstützt nur ARM bereitgestellte Anwendungstypversionen.</span><span class="sxs-lookup"><span data-stu-id="7f29c-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="7f29c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f29c-105">SYNTAX</span></span>

### <span data-ttu-id="7f29c-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f29c-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f29c-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="7f29c-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f29c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f29c-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f29c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f29c-109">DESCRIPTION</span></span>
<span data-ttu-id="7f29c-110">Verwenden Sie dieses Cmdlet, um die Versionsdetails des Anwendungstyps in der angegebenen Ressourcengruppe und dem angegebenen Cluster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7f29c-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="7f29c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f29c-111">EXAMPLES</span></span>

### <span data-ttu-id="7f29c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f29c-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="7f29c-113">In diesem Beispiel wird der Anwendungstyp "testAppType" mit der Version "v1" ab, wenn die Ressource nicht zu finden ist, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7f29c-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="7f29c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f29c-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="7f29c-115">Dieses Beispiel ruft eine Liste der Anwendungstypversionen ab, die unter dem angegebenen Cluster und Typ definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7f29c-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="7f29c-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7f29c-116">PARAMETERS</span></span>

### <span data-ttu-id="7f29c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7f29c-117">-ClusterName</span></span>
<span data-ttu-id="7f29c-118">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="7f29c-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f29c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f29c-119">-DefaultProfile</span></span>
<span data-ttu-id="7f29c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f29c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f29c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7f29c-121">-Name</span></span>
<span data-ttu-id="7f29c-122">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="7f29c-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f29c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f29c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f29c-124">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7f29c-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f29c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f29c-125">-ResourceId</span></span>
<span data-ttu-id="7f29c-126">Arm ResourceId der Anwendungstypversion.</span><span class="sxs-lookup"><span data-stu-id="7f29c-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="7f29c-127">-Version</span><span class="sxs-lookup"><span data-stu-id="7f29c-127">-Version</span></span>
<span data-ttu-id="7f29c-128">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="7f29c-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f29c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f29c-129">CommonParameters</span></span>
<span data-ttu-id="7f29c-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f29c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f29c-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f29c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f29c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f29c-132">INPUTS</span></span>

### <span data-ttu-id="7f29c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7f29c-133">System.String</span></span>

## <span data-ttu-id="7f29c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f29c-134">OUTPUTS</span></span>

### <span data-ttu-id="7f29c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7f29c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="7f29c-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7f29c-136">NOTES</span></span>

## <span data-ttu-id="7f29c-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7f29c-137">RELATED LINKS</span></span>

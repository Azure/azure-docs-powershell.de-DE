---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303008"
---
# <span data-ttu-id="8e80c-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e80c-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8e80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e80c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e80c-103">Get Service Fabric application type version details.</span><span class="sxs-lookup"><span data-stu-id="8e80c-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="8e80c-104">Unterstützt nur ARM bereitgestellten Anwendungstypversionen.</span><span class="sxs-lookup"><span data-stu-id="8e80c-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="8e80c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e80c-105">SYNTAX</span></span>

### <span data-ttu-id="8e80c-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e80c-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e80c-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="8e80c-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e80c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e80c-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e80c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e80c-109">DESCRIPTION</span></span>
<span data-ttu-id="8e80c-110">Verwenden Sie dieses Cmdlet, um Versionsdetails für den Anwendungstyp in der angegebenen Ressourcengruppe und dem angegebenen Cluster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e80c-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="8e80c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e80c-111">EXAMPLES</span></span>

### <span data-ttu-id="8e80c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e80c-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="8e80c-113">In diesem Beispiel wird der Anwendungstyp "testAppType" mit Der Version "v1" ausgelöst, wenn die Ressource nicht zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="8e80c-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="8e80c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e80c-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="8e80c-115">Dieses Beispiel ruft eine Liste der Anwendungstypversionen ab, die unter dem angegebenen Cluster und Typ definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8e80c-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="8e80c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e80c-116">PARAMETERS</span></span>

### <span data-ttu-id="8e80c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e80c-117">-ClusterName</span></span>
<span data-ttu-id="8e80c-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="8e80c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8e80c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e80c-119">-DefaultProfile</span></span>
<span data-ttu-id="8e80c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e80c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e80c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8e80c-121">-Name</span></span>
<span data-ttu-id="8e80c-122">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="8e80c-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="8e80c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e80c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e80c-124">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8e80c-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8e80c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e80c-125">-ResourceId</span></span>
<span data-ttu-id="8e80c-126">Arm ResourceId der Anwendungstypversion.</span><span class="sxs-lookup"><span data-stu-id="8e80c-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="8e80c-127">-Version</span><span class="sxs-lookup"><span data-stu-id="8e80c-127">-Version</span></span>
<span data-ttu-id="8e80c-128">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="8e80c-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="8e80c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e80c-129">CommonParameters</span></span>
<span data-ttu-id="8e80c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e80c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e80c-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e80c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e80c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e80c-132">INPUTS</span></span>

### <span data-ttu-id="8e80c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8e80c-133">System.String</span></span>

## <span data-ttu-id="8e80c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e80c-134">OUTPUTS</span></span>

### <span data-ttu-id="8e80c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8e80c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8e80c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e80c-136">NOTES</span></span>

## <span data-ttu-id="8e80c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e80c-137">RELATED LINKS</span></span>

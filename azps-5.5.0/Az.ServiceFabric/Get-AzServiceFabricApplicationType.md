---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173996"
---
# <span data-ttu-id="8b2f2-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b2f2-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="8b2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2f2-103">Get Service Fabric application type details.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="8b2f2-104">Unterstützt nur ARM bereitgestellten Anwendungstypen.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="8b2f2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b2f2-105">SYNTAX</span></span>

### <span data-ttu-id="8b2f2-106">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b2f2-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b2f2-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8b2f2-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b2f2-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b2f2-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b2f2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b2f2-109">DESCRIPTION</span></span>
<span data-ttu-id="8b2f2-110">Verwenden Sie dieses Cmdlet, um die Anwendungstypdetails in der angegebenen Ressourcengruppe und dem angegebenen Cluster zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="8b2f2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b2f2-111">EXAMPLES</span></span>

### <span data-ttu-id="8b2f2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b2f2-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="8b2f2-113">In diesem Beispiel werden die Details des Anwendungstyps mit den angegebenen Parametern angezeigt. Wenn die Ressource nicht angezeigt wird, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="8b2f2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8b2f2-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="8b2f2-115">In diesem Beispiel wird eine Liste der Anwendungstypen angezeigt, die unter dem angegebenen Cluster definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="8b2f2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b2f2-116">PARAMETERS</span></span>

### <span data-ttu-id="8b2f2-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8b2f2-117">-ClusterName</span></span>
<span data-ttu-id="8b2f2-118">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8b2f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2f2-119">-DefaultProfile</span></span>
<span data-ttu-id="8b2f2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b2f2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b2f2-121">-Name</span></span>
<span data-ttu-id="8b2f2-122">Angeben des Namens des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="8b2f2-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b2f2-124">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8b2f2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b2f2-125">-ResourceId</span></span>
<span data-ttu-id="8b2f2-126">Arm ResourceId des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="8b2f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2f2-127">CommonParameters</span></span>
<span data-ttu-id="8b2f2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2f2-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b2f2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2f2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b2f2-130">INPUTS</span></span>

### <span data-ttu-id="8b2f2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8b2f2-131">System.String</span></span>

## <span data-ttu-id="8b2f2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b2f2-132">OUTPUTS</span></span>

### <span data-ttu-id="8b2f2-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b2f2-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="8b2f2-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b2f2-134">NOTES</span></span>

## <span data-ttu-id="8b2f2-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b2f2-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: a0625a974da7d6544345419573fa4e96f0bbcae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010489"
---
# <span data-ttu-id="0ec09-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0ec09-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="0ec09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ec09-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec09-103">Informationen zu den Details des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="0ec09-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="0ec09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ec09-104">SYNTAX</span></span>

### <span data-ttu-id="0ec09-105">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ec09-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ec09-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0ec09-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ec09-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ec09-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ec09-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ec09-108">DESCRIPTION</span></span>
<span data-ttu-id="0ec09-109">Verwenden Sie dieses Cmdlet, um die Details des Anwendungstyps in der angegebenen Ressourcengruppe und dem angegebenen Cluster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ec09-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="0ec09-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ec09-110">EXAMPLES</span></span>

### <span data-ttu-id="0ec09-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ec09-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="0ec09-112">In diesem Beispiel werden die Details des Anwendungstyps mit den angegebenen Parametern abgerufen, wenn die Ressource nicht gefunden wird, die eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="0ec09-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="0ec09-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ec09-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="0ec09-114">In diesem Beispiel wird eine Liste der Anwendungstypen abgerufen, die unter dem angegebenen Cluster definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0ec09-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="0ec09-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ec09-115">PARAMETERS</span></span>

### <span data-ttu-id="0ec09-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0ec09-116">-ClusterName</span></span>
<span data-ttu-id="0ec09-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0ec09-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0ec09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec09-118">-DefaultProfile</span></span>
<span data-ttu-id="0ec09-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ec09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ec09-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ec09-120">-Name</span></span>
<span data-ttu-id="0ec09-121">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="0ec09-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="0ec09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec09-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ec09-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0ec09-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0ec09-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0ec09-124">-ResourceId</span></span>
<span data-ttu-id="0ec09-125">Arm-Ressourcentyp des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="0ec09-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="0ec09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec09-126">CommonParameters</span></span>
<span data-ttu-id="0ec09-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec09-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ec09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec09-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ec09-129">INPUTS</span></span>

### <span data-ttu-id="0ec09-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0ec09-130">System.String</span></span>

## <span data-ttu-id="0ec09-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ec09-131">OUTPUTS</span></span>

### <span data-ttu-id="0ec09-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="0ec09-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="0ec09-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ec09-133">NOTES</span></span>

## <span data-ttu-id="0ec09-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ec09-134">RELATED LINKS</span></span>

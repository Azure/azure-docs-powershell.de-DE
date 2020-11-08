---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7a47f6b7ee5200b8e4409d7fa25ba63244fb2ae6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003278"
---
# <span data-ttu-id="57427-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="57427-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="57427-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57427-102">SYNOPSIS</span></span>
<span data-ttu-id="57427-103">Abrufen von Details zur Version des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="57427-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="57427-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57427-104">SYNTAX</span></span>

### <span data-ttu-id="57427-105">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="57427-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57427-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="57427-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57427-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="57427-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57427-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57427-108">DESCRIPTION</span></span>
<span data-ttu-id="57427-109">Verwenden Sie dieses Cmdlet, um die Details der Anwendungstypen Version in der angegebenen Ressourcengruppe und dem angegebenen Cluster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="57427-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="57427-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57427-110">EXAMPLES</span></span>

### <span data-ttu-id="57427-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57427-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="57427-112">In diesem Beispiel wird der Anwendungstyp "testAppType" mit der Version "V1" abgerufen, wenn die Ressource, die eine Ausnahme auslöst, nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="57427-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="57427-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="57427-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="57427-114">In diesem Beispiel wird eine Liste der Anwendungs Typversionen abgerufen, die unter dem angegebenen Cluster und Typ definiert sind.</span><span class="sxs-lookup"><span data-stu-id="57427-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="57427-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="57427-115">PARAMETERS</span></span>

### <span data-ttu-id="57427-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="57427-116">-ClusterName</span></span>
<span data-ttu-id="57427-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="57427-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="57427-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57427-118">-DefaultProfile</span></span>
<span data-ttu-id="57427-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57427-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57427-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57427-120">-Name</span></span>
<span data-ttu-id="57427-121">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="57427-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="57427-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57427-122">-ResourceGroupName</span></span>
<span data-ttu-id="57427-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="57427-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="57427-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="57427-124">-ResourceId</span></span>
<span data-ttu-id="57427-125">Arm-Ressourcen-Nr. des Anwendungstyps Version.</span><span class="sxs-lookup"><span data-stu-id="57427-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="57427-126">-Version</span><span class="sxs-lookup"><span data-stu-id="57427-126">-Version</span></span>
<span data-ttu-id="57427-127">Geben Sie die Version des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="57427-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="57427-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57427-128">CommonParameters</span></span>
<span data-ttu-id="57427-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57427-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57427-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57427-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57427-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57427-131">INPUTS</span></span>

### <span data-ttu-id="57427-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57427-132">System.String</span></span>

## <span data-ttu-id="57427-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57427-133">OUTPUTS</span></span>

### <span data-ttu-id="57427-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="57427-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="57427-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="57427-135">NOTES</span></span>

## <span data-ttu-id="57427-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57427-136">RELATED LINKS</span></span>

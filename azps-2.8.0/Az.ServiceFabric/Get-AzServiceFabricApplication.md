---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 590f2470cacd349eb8f0467ce37e7c15ab5a9321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823196"
---
# <span data-ttu-id="c8499-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c8499-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c8499-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8499-102">SYNOPSIS</span></span>
<span data-ttu-id="c8499-103">Abrufen von Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8499-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="c8499-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8499-104">SYNTAX</span></span>

### <span data-ttu-id="c8499-105">ByResourceGroupAndCluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8499-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8499-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c8499-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8499-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8499-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8499-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8499-108">DESCRIPTION</span></span>
<span data-ttu-id="c8499-109">Dieses Cmdlet ruft die Anwendungsdetails in der angegebenen Ressourcengruppe und dem angegebenen Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="c8499-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="c8499-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8499-110">EXAMPLES</span></span>

### <span data-ttu-id="c8499-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8499-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c8499-112">In diesem Beispiel werden die Details der Anwendungsressource für die Anwendung "testApp" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8499-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="c8499-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c8499-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="c8499-114">In diesem Beispiel wird eine Liste der Anwendungen unter dem Cluster "testCluster" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8499-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="c8499-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8499-115">PARAMETERS</span></span>

### <span data-ttu-id="c8499-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c8499-116">-ClusterName</span></span>
<span data-ttu-id="c8499-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c8499-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c8499-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8499-118">-DefaultProfile</span></span>
<span data-ttu-id="c8499-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8499-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8499-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c8499-120">-Name</span></span>
<span data-ttu-id="c8499-121">Geben Sie den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c8499-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c8499-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8499-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8499-123">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c8499-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c8499-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c8499-124">-ResourceId</span></span>
<span data-ttu-id="c8499-125">Arm-Quell Code der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c8499-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c8499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8499-126">CommonParameters</span></span>
<span data-ttu-id="c8499-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8499-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8499-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8499-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8499-129">INPUTS</span></span>

### <span data-ttu-id="c8499-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c8499-130">System.String</span></span>

## <span data-ttu-id="c8499-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8499-131">OUTPUTS</span></span>

### <span data-ttu-id="c8499-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c8499-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c8499-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8499-133">NOTES</span></span>

## <span data-ttu-id="c8499-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8499-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300136"
---
# <span data-ttu-id="ed316-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ed316-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="ed316-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed316-102">SYNOPSIS</span></span>
<span data-ttu-id="ed316-103">Abrufen der Ressourcendetails des verwalteten Knotentyps</span><span class="sxs-lookup"><span data-stu-id="ed316-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="ed316-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed316-104">SYNTAX</span></span>

### <span data-ttu-id="ed316-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed316-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed316-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed316-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed316-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed316-107">DESCRIPTION</span></span>
<span data-ttu-id="ed316-108">Abrufen der Ressourcendetails des verwalteten Knotentyps</span><span class="sxs-lookup"><span data-stu-id="ed316-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="ed316-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed316-109">EXAMPLES</span></span>

### <span data-ttu-id="ed316-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed316-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="ed316-111">Abrufen von Knotentypen Details</span><span class="sxs-lookup"><span data-stu-id="ed316-111">Get node type details.</span></span>

### <span data-ttu-id="ed316-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed316-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="ed316-113">Abrufen einer Liste der Knotentypen unter dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ed316-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="ed316-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed316-114">PARAMETERS</span></span>

### <span data-ttu-id="ed316-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ed316-115">-ClusterName</span></span>
<span data-ttu-id="ed316-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ed316-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed316-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed316-117">-DefaultProfile</span></span>
<span data-ttu-id="ed316-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed316-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed316-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ed316-119">-Name</span></span>
<span data-ttu-id="ed316-120">Geben Sie den Namen des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="ed316-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed316-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed316-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed316-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed316-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed316-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed316-123">CommonParameters</span></span>
<span data-ttu-id="ed316-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed316-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed316-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed316-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed316-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed316-126">INPUTS</span></span>

### <span data-ttu-id="ed316-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ed316-127">System.String</span></span>

## <span data-ttu-id="ed316-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed316-128">OUTPUTS</span></span>

### <span data-ttu-id="ed316-129">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ed316-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ed316-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed316-130">NOTES</span></span>

## <span data-ttu-id="ed316-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed316-131">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: b954c1b6c5085dd285b925d57fe0b4649830bffd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659323"
---
# <span data-ttu-id="a2154-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a2154-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="a2154-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2154-102">SYNOPSIS</span></span>
<span data-ttu-id="a2154-103">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="a2154-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="a2154-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2154-104">SYNTAX</span></span>

### <span data-ttu-id="a2154-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2154-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2154-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a2154-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2154-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a2154-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2154-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2154-108">DESCRIPTION</span></span>
<span data-ttu-id="a2154-109">Der **Get-AzServiceFabricCluster** erhält die Clusterressourcen Details.</span><span class="sxs-lookup"><span data-stu-id="a2154-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="a2154-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2154-110">EXAMPLES</span></span>

### <span data-ttu-id="a2154-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2154-111">Example 1</span></span>
```
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="a2154-112">Dieser Befehl erhält die Clusterressourcen Details für Cluster "mycluster".</span><span class="sxs-lookup"><span data-stu-id="a2154-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="a2154-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2154-113">PARAMETERS</span></span>

### <span data-ttu-id="a2154-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2154-114">-DefaultProfile</span></span>
<span data-ttu-id="a2154-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2154-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2154-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a2154-116">-Name</span></span>
<span data-ttu-id="a2154-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="a2154-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2154-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2154-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2154-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a2154-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2154-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2154-120">CommonParameters</span></span>
<span data-ttu-id="a2154-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2154-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2154-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2154-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2154-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2154-123">INPUTS</span></span>

### <span data-ttu-id="a2154-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a2154-124">System.String</span></span>

## <span data-ttu-id="a2154-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2154-125">OUTPUTS</span></span>

### <span data-ttu-id="a2154-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a2154-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a2154-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2154-127">NOTES</span></span>

## <span data-ttu-id="a2154-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2154-128">RELATED LINKS</span></span>

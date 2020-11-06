---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478242"
---
# <span data-ttu-id="2b9e8-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2b9e8-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="2b9e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9e8-103">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b9e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b9e8-104">SYNTAX</span></span>

### <span data-ttu-id="2b9e8-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b9e8-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b9e8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b9e8-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b9e8-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2b9e8-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b9e8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b9e8-108">DESCRIPTION</span></span>
<span data-ttu-id="2b9e8-109">Das **Add-AzureRmServiceFabricCluster** erhält die Clusterressourcen Details.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="2b9e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b9e8-110">EXAMPLES</span></span>

### <span data-ttu-id="2b9e8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b9e8-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="2b9e8-112">Dieser Befehl erhält die Clusterressourcen Details für Cluster "mycluster".</span><span class="sxs-lookup"><span data-stu-id="2b9e8-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="2b9e8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b9e8-113">PARAMETERS</span></span>

### <span data-ttu-id="2b9e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9e8-114">-DefaultProfile</span></span>
<span data-ttu-id="2b9e8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2b9e8-116">-Name</span></span>
<span data-ttu-id="2b9e8-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b9e8-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9e8-120">CommonParameters</span></span>
<span data-ttu-id="2b9e8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9e8-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9e8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b9e8-123">INPUTS</span></span>

### <span data-ttu-id="2b9e8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9e8-124">System.String</span></span>

## <span data-ttu-id="2b9e8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b9e8-125">OUTPUTS</span></span>

### <span data-ttu-id="2b9e8-126">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. Commands. ServiceFabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b9e8-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b9e8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b9e8-127">NOTES</span></span>

## <span data-ttu-id="2b9e8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b9e8-128">RELATED LINKS</span></span>


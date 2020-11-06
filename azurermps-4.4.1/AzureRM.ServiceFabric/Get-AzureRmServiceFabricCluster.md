---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504729"
---
# <span data-ttu-id="096bb-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="096bb-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="096bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="096bb-102">SYNOPSIS</span></span>
<span data-ttu-id="096bb-103">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="096bb-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="096bb-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="096bb-105">DESCRIPTION</span></span>
<span data-ttu-id="096bb-106">Das **Add-AzureRmServiceFabricCluster** erhält die Clusterressourcen Details.</span><span class="sxs-lookup"><span data-stu-id="096bb-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="096bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="096bb-107">EXAMPLES</span></span>

### <span data-ttu-id="096bb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="096bb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="096bb-109">Dieser Befehl erhält die Clusterressourcen Details für Cluster "mycluster".</span><span class="sxs-lookup"><span data-stu-id="096bb-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="096bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="096bb-110">PARAMETERS</span></span>

### <span data-ttu-id="096bb-111">-Name</span><span class="sxs-lookup"><span data-stu-id="096bb-111">-Name</span></span>
<span data-ttu-id="096bb-112">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="096bb-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096bb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096bb-113">-ResourceGroupName</span></span>
<span data-ttu-id="096bb-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="096bb-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096bb-115">-DefaultProfile</span></span>
<span data-ttu-id="096bb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="096bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="096bb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096bb-117">CommonParameters</span></span>
<span data-ttu-id="096bb-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096bb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096bb-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096bb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096bb-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="096bb-120">INPUTS</span></span>

### <span data-ttu-id="096bb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="096bb-121">System.String</span></span>

## <span data-ttu-id="096bb-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="096bb-122">OUTPUTS</span></span>

### <span data-ttu-id="096bb-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster, Microsoft. Azure. Commands. ServiceFabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="096bb-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="096bb-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="096bb-124">NOTES</span></span>

## <span data-ttu-id="096bb-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="096bb-125">RELATED LINKS</span></span>


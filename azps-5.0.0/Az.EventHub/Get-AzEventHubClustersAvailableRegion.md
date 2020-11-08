---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178901"
---
# <span data-ttu-id="0a55d-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="0a55d-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="0a55d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a55d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a55d-103">Ruft die Details eines einzelnen Eventhub-Clusters oder der Liste der Cluster in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0a55d-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="0a55d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a55d-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a55d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a55d-105">DESCRIPTION</span></span>
<span data-ttu-id="0a55d-106">Die Get-AzEventHubClustersAvailableRegion-Cmdlet-Liste der Regionen, in denen dedizierte zum Erstellen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0a55d-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="0a55d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a55d-107">EXAMPLES</span></span>

### <span data-ttu-id="0a55d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a55d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="0a55d-109">Die Liste der Regionen wird zurückgegeben, wobei</span><span class="sxs-lookup"><span data-stu-id="0a55d-109">List of regions is returned where</span></span>

## <span data-ttu-id="0a55d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a55d-110">PARAMETERS</span></span>

### <span data-ttu-id="0a55d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a55d-111">-DefaultProfile</span></span>
<span data-ttu-id="0a55d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a55d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a55d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a55d-113">CommonParameters</span></span>
<span data-ttu-id="0a55d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a55d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a55d-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a55d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a55d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a55d-116">INPUTS</span></span>

### <span data-ttu-id="0a55d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="0a55d-117">None</span></span>

## <span data-ttu-id="0a55d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a55d-118">OUTPUTS</span></span>

### <span data-ttu-id="0a55d-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0a55d-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0a55d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a55d-120">NOTES</span></span>

## <span data-ttu-id="0a55d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a55d-121">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: 219afc3021a0826402672c41e2c13e44bd6d390c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505462"
---
# <span data-ttu-id="33698-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="33698-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="33698-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33698-102">SYNOPSIS</span></span>
<span data-ttu-id="33698-103">Listet Netzwerk Verwendungen für ein Abonnement auf</span><span class="sxs-lookup"><span data-stu-id="33698-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33698-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33698-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33698-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33698-105">DESCRIPTION</span></span>
<span data-ttu-id="33698-106">Das Get-AzureRmNetworkUsage-Cmdlet ruft Grenzwerte und die aktuelle Verwendung für Netzwerkressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="33698-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="33698-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33698-107">EXAMPLES</span></span>

### <span data-ttu-id="33698-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33698-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="33698-109">Ruft Ressourcen Nutzungsdaten in westcentralus Region ab.</span><span class="sxs-lookup"><span data-stu-id="33698-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="33698-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33698-110">PARAMETERS</span></span>

### <span data-ttu-id="33698-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33698-111">-DefaultProfile</span></span>
<span data-ttu-id="33698-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33698-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33698-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="33698-113">-Location</span></span>
<span data-ttu-id="33698-114">Der Speicherort, an dem die Ressourcenverwendung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="33698-114">The location where resource usage is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33698-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33698-115">CommonParameters</span></span>
<span data-ttu-id="33698-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33698-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33698-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33698-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33698-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33698-118">INPUTS</span></span>

### <span data-ttu-id="33698-119">System. String</span><span class="sxs-lookup"><span data-stu-id="33698-119">System.String</span></span>

## <span data-ttu-id="33698-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33698-120">OUTPUTS</span></span>

### <span data-ttu-id="33698-121">Microsoft. Azure. Commands. Network. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="33698-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="33698-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="33698-122">NOTES</span></span>

## <span data-ttu-id="33698-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33698-123">RELATED LINKS</span></span>


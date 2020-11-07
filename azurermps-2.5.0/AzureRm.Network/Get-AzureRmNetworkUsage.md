---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkusage
schema: 2.0.0
ms.openlocfilehash: 24ffdb99efddf22a5e632ac576a4aa8e7db42af6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848787"
---
# <span data-ttu-id="997a5-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="997a5-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="997a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="997a5-102">SYNOPSIS</span></span>
<span data-ttu-id="997a5-103">Listet Netzwerk Verwendungen für ein Abonnement auf</span><span class="sxs-lookup"><span data-stu-id="997a5-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="997a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="997a5-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="997a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="997a5-105">DESCRIPTION</span></span>
<span data-ttu-id="997a5-106">Das Get-AzureRmNetworkUsage-Cmdlet ruft Grenzwerte und die aktuelle Verwendung für Netzwerkressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="997a5-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="997a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="997a5-107">EXAMPLES</span></span>

### <span data-ttu-id="997a5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="997a5-108">Example 1</span></span>
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

<span data-ttu-id="997a5-109">Ruft Ressourcen Nutzungsdaten in westcentralus Region ab.</span><span class="sxs-lookup"><span data-stu-id="997a5-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="997a5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="997a5-110">PARAMETERS</span></span>

### <span data-ttu-id="997a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="997a5-111">-DefaultProfile</span></span>
<span data-ttu-id="997a5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="997a5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="997a5-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="997a5-113">-Location</span></span>
<span data-ttu-id="997a5-114">Der Speicherort, an dem die Ressourcenverwendung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="997a5-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="997a5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997a5-115">CommonParameters</span></span>
<span data-ttu-id="997a5-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="997a5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997a5-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="997a5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997a5-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="997a5-118">INPUTS</span></span>

### <span data-ttu-id="997a5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="997a5-119">System.String</span></span>

## <span data-ttu-id="997a5-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="997a5-120">OUTPUTS</span></span>

### <span data-ttu-id="997a5-121">Microsoft. Azure. Commands. Network. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="997a5-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="997a5-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="997a5-122">NOTES</span></span>

## <span data-ttu-id="997a5-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="997a5-123">RELATED LINKS</span></span>


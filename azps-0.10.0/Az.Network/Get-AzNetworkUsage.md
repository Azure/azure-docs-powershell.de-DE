---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 8429b007328fcc3358ecbb165fea55bb3c5eb232
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841599"
---
# <span data-ttu-id="114b2-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="114b2-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="114b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="114b2-102">SYNOPSIS</span></span>
<span data-ttu-id="114b2-103">Listet Netzwerk Verwendungen für ein Abonnement auf</span><span class="sxs-lookup"><span data-stu-id="114b2-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="114b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="114b2-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="114b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="114b2-105">DESCRIPTION</span></span>
<span data-ttu-id="114b2-106">Das Get-AzNetworkUsage-Cmdlet ruft Grenzwerte und die aktuelle Verwendung für Netzwerkressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="114b2-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="114b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="114b2-107">EXAMPLES</span></span>

### <span data-ttu-id="114b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="114b2-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

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

<span data-ttu-id="114b2-109">Ruft Ressourcen Nutzungsdaten in westcentralus Region ab.</span><span class="sxs-lookup"><span data-stu-id="114b2-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="114b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="114b2-110">PARAMETERS</span></span>

### <span data-ttu-id="114b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114b2-111">-DefaultProfile</span></span>
<span data-ttu-id="114b2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="114b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="114b2-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="114b2-113">-Location</span></span>
<span data-ttu-id="114b2-114">Der Speicherort, an dem die Ressourcenverwendung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="114b2-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="114b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114b2-115">CommonParameters</span></span>
<span data-ttu-id="114b2-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114b2-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114b2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114b2-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="114b2-118">INPUTS</span></span>

### <span data-ttu-id="114b2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="114b2-119">System.String</span></span>

## <span data-ttu-id="114b2-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="114b2-120">OUTPUTS</span></span>

### <span data-ttu-id="114b2-121">Microsoft. Azure. Commands. Network. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="114b2-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="114b2-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="114b2-122">NOTES</span></span>

## <span data-ttu-id="114b2-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="114b2-123">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 74da4bba721f415b48ee8ff626a1bfcf1d313b64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660737"
---
# <span data-ttu-id="9d823-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="9d823-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="9d823-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d823-102">SYNOPSIS</span></span>
<span data-ttu-id="9d823-103">Listet Netzwerk Verwendungen für ein Abonnement auf</span><span class="sxs-lookup"><span data-stu-id="9d823-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="9d823-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d823-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d823-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d823-105">DESCRIPTION</span></span>
<span data-ttu-id="9d823-106">Das Get-AzNetworkUsage-Cmdlet ruft Grenzwerte und die aktuelle Verwendung für Netzwerkressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="9d823-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="9d823-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d823-107">EXAMPLES</span></span>

### <span data-ttu-id="9d823-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d823-108">Example 1</span></span>
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

<span data-ttu-id="9d823-109">Ruft Ressourcen Nutzungsdaten in westcentralus Region ab.</span><span class="sxs-lookup"><span data-stu-id="9d823-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="9d823-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d823-110">PARAMETERS</span></span>

### <span data-ttu-id="9d823-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d823-111">-DefaultProfile</span></span>
<span data-ttu-id="9d823-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d823-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d823-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="9d823-113">-Location</span></span>
<span data-ttu-id="9d823-114">Der Speicherort, an dem die Ressourcenverwendung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="9d823-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d823-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d823-115">CommonParameters</span></span>
<span data-ttu-id="9d823-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d823-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d823-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d823-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d823-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d823-118">INPUTS</span></span>

### <span data-ttu-id="9d823-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9d823-119">System.String</span></span>

## <span data-ttu-id="9d823-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d823-120">OUTPUTS</span></span>

### <span data-ttu-id="9d823-121">Microsoft. Azure. Commands. Network. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="9d823-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="9d823-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d823-122">NOTES</span></span>

## <span data-ttu-id="9d823-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d823-123">RELATED LINKS</span></span>

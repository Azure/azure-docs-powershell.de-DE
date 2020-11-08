---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174326"
---
# <span data-ttu-id="14778-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="14778-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="14778-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14778-102">SYNOPSIS</span></span>
<span data-ttu-id="14778-103">Erstellen einer neuen Whitelist für Threat Intelligence für Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="14778-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="14778-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14778-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14778-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14778-105">DESCRIPTION</span></span>
<span data-ttu-id="14778-106">Mit dem Cmdlet " **New-AzFirewallPolicyThreatIntelWhitelist** " wird ein Intel Whitelist-Bedrohungs Objekt erstellt, das beim Erstellen oder Festlegen einer Azure Firewall-Richtlinie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="14778-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="14778-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14778-107">EXAMPLES</span></span>

### <span data-ttu-id="14778-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14778-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="14778-109">In diesem Beispiel wird eine Intel Whitelist mit einer FQDN-Whitelist mit einem Eintrag und einer IP-Adressen-Whitelist mit zwei Einträgen erstellt.</span><span class="sxs-lookup"><span data-stu-id="14778-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="14778-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14778-110">PARAMETERS</span></span>

### <span data-ttu-id="14778-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14778-111">-DefaultProfile</span></span>
<span data-ttu-id="14778-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14778-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14778-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="14778-113">-FQDN</span></span>
<span data-ttu-id="14778-114">Die FQDNs der Bedrohungs-Intel-Whitelist</span><span class="sxs-lookup"><span data-stu-id="14778-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14778-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="14778-115">-IpAddress</span></span>
<span data-ttu-id="14778-116">Die IP-Adressen der Bedrohungs-Intel-Whitelist</span><span class="sxs-lookup"><span data-stu-id="14778-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14778-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14778-117">CommonParameters</span></span>
<span data-ttu-id="14778-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14778-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14778-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14778-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14778-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14778-120">INPUTS</span></span>

### <span data-ttu-id="14778-121">Keine</span><span class="sxs-lookup"><span data-stu-id="14778-121">None</span></span>

## <span data-ttu-id="14778-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14778-122">OUTPUTS</span></span>

### <span data-ttu-id="14778-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="14778-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="14778-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="14778-124">NOTES</span></span>

## <span data-ttu-id="14778-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14778-125">RELATED LINKS</span></span>

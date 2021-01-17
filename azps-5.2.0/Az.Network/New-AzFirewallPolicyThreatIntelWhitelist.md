---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302880"
---
# <span data-ttu-id="dc1c5-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="dc1c5-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="dc1c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1c5-103">Erstellen einer neuen Threat Intelligence-Whitelist für die Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="dc1c5-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="dc1c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc1c5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc1c5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1c5-106">Das **Cmdlet "New-AzFirewallPolicyThreatIntelWhitelist"** erstellt ein intel whitelist-Threat-Objekt, das beim Erstellen oder Festlegen einer Azure-Firewallrichtlinie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="dc1c5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc1c5-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1c5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc1c5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="dc1c5-109">In diesem Beispiel wird eine Intel Whitelist für Bedrohungen erstellt, die eine FQDN-Whitelist eines Eintrags und eine Ip-Adress-Whitelist mit zwei Einträgen enthält.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="dc1c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc1c5-110">PARAMETERS</span></span>

### <span data-ttu-id="dc1c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1c5-111">-DefaultProfile</span></span>
<span data-ttu-id="dc1c5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1c5-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="dc1c5-113">-FQDN</span></span>
<span data-ttu-id="dc1c5-114">FQDNs der Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="dc1c5-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="dc1c5-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="dc1c5-115">-IpAddress</span></span>
<span data-ttu-id="dc1c5-116">Die IP-Adressen der Intel Whitelist für Threat</span><span class="sxs-lookup"><span data-stu-id="dc1c5-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="dc1c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1c5-117">CommonParameters</span></span>
<span data-ttu-id="dc1c5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1c5-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1c5-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc1c5-120">INPUTS</span></span>

### <span data-ttu-id="dc1c5-121">Keine</span><span class="sxs-lookup"><span data-stu-id="dc1c5-121">None</span></span>

## <span data-ttu-id="dc1c5-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc1c5-122">OUTPUTS</span></span>

### <span data-ttu-id="dc1c5-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="dc1c5-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="dc1c5-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc1c5-124">NOTES</span></span>

## <span data-ttu-id="dc1c5-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc1c5-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922811"
---
# <span data-ttu-id="05984-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="05984-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="05984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05984-102">SYNOPSIS</span></span>
<span data-ttu-id="05984-103">Erstellen einer neuen Whitelist für threat intelligence für Azure Firewall Policy</span><span class="sxs-lookup"><span data-stu-id="05984-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="05984-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05984-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05984-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05984-105">DESCRIPTION</span></span>
<span data-ttu-id="05984-106">Das **Cmdlet New-AzFirewallPolicyThreatIntelWhitelist** erstellt ein Intel Whitelist-Objekt für Bedrohungen, das beim Erstellen oder Festlegen einer Azure-Firewallrichtlinie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="05984-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="05984-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05984-107">EXAMPLES</span></span>

### <span data-ttu-id="05984-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05984-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="05984-109">In diesem Beispiel wird eine Intel-Whitelist für Bedrohungen erstellt, die eine FQDN-Whitelist mit einem Eintrag und eine Ip-Adress-Whitelist mit zwei Einträgen enthält.</span><span class="sxs-lookup"><span data-stu-id="05984-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="05984-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05984-110">PARAMETERS</span></span>

### <span data-ttu-id="05984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05984-111">-DefaultProfile</span></span>
<span data-ttu-id="05984-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05984-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05984-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="05984-113">-FQDN</span></span>
<span data-ttu-id="05984-114">Die FQDNs der Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="05984-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="05984-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="05984-115">-IpAddress</span></span>
<span data-ttu-id="05984-116">Die IP-Adressen der Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="05984-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="05984-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05984-117">CommonParameters</span></span>
<span data-ttu-id="05984-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05984-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05984-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05984-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05984-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05984-120">INPUTS</span></span>

### <span data-ttu-id="05984-121">Keine</span><span class="sxs-lookup"><span data-stu-id="05984-121">None</span></span>

## <span data-ttu-id="05984-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05984-122">OUTPUTS</span></span>

### <span data-ttu-id="05984-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="05984-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="05984-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05984-124">NOTES</span></span>

## <span data-ttu-id="05984-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05984-125">RELATED LINKS</span></span>

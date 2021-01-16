---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470232"
---
# <span data-ttu-id="2682d-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2682d-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="2682d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2682d-102">SYNOPSIS</span></span>
<span data-ttu-id="2682d-103">Erstellen einer neuen Threat Intelligence-Whitelist für die Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="2682d-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="2682d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2682d-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2682d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2682d-105">DESCRIPTION</span></span>
<span data-ttu-id="2682d-106">Das **Cmdlet "New-AzFirewallThreatIntelWhitelist"** erstellt ein intel whitelist-Threat-Objekt, das beim Erstellen oder Festlegen einer Azure Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2682d-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="2682d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2682d-107">EXAMPLES</span></span>

### <span data-ttu-id="2682d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2682d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="2682d-109">In diesem Beispiel wird eine Intel Whitelist für Bedrohungen erstellt, die eine FQDN-Whitelist mit zwei Einträgen und eine Ip-Adress-Whitelist mit zwei Einträgen enthält.</span><span class="sxs-lookup"><span data-stu-id="2682d-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="2682d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2682d-110">PARAMETERS</span></span>

### <span data-ttu-id="2682d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2682d-111">-DefaultProfile</span></span>
<span data-ttu-id="2682d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2682d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2682d-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2682d-113">-FQDN</span></span>
<span data-ttu-id="2682d-114">FQDNs der Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="2682d-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2682d-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2682d-115">-IpAddress</span></span>
<span data-ttu-id="2682d-116">Die IP-Adressen der Intel Whitelist für Threat</span><span class="sxs-lookup"><span data-stu-id="2682d-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2682d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2682d-117">CommonParameters</span></span>
<span data-ttu-id="2682d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2682d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2682d-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2682d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2682d-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2682d-120">INPUTS</span></span>

### <span data-ttu-id="2682d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="2682d-121">None</span></span>

## <span data-ttu-id="2682d-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2682d-122">OUTPUTS</span></span>

### <span data-ttu-id="2682d-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2682d-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="2682d-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2682d-124">NOTES</span></span>

## <span data-ttu-id="2682d-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2682d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2682d-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2682d-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="2682d-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2682d-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="2682d-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2682d-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
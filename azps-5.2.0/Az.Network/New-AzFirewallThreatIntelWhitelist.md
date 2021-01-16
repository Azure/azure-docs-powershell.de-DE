---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299624"
---
# <span data-ttu-id="b0003-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="b0003-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="b0003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0003-102">SYNOPSIS</span></span>
<span data-ttu-id="b0003-103">Erstellen einer neuen Threat Intelligence-Whitelist für die Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="b0003-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="b0003-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0003-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0003-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0003-105">DESCRIPTION</span></span>
<span data-ttu-id="b0003-106">Das **Cmdlet "New-AzFirewallThreatIntelWhitelist"** erstellt ein intel whitelist-Threat-Objekt, das beim Erstellen oder Festlegen einer Azure Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0003-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="b0003-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0003-107">EXAMPLES</span></span>

### <span data-ttu-id="b0003-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0003-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="b0003-109">In diesem Beispiel wird eine Intel Whitelist für Bedrohungen erstellt, die eine FQDN-Whitelist mit zwei Einträgen und eine Ip-Adress-Whitelist mit zwei Einträgen enthält.</span><span class="sxs-lookup"><span data-stu-id="b0003-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="b0003-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0003-110">PARAMETERS</span></span>

### <span data-ttu-id="b0003-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0003-111">-DefaultProfile</span></span>
<span data-ttu-id="b0003-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0003-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0003-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="b0003-113">-FQDN</span></span>
<span data-ttu-id="b0003-114">FQDNs der Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="b0003-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="b0003-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b0003-115">-IpAddress</span></span>
<span data-ttu-id="b0003-116">Die IP-Adressen der Intel Whitelist für Threat</span><span class="sxs-lookup"><span data-stu-id="b0003-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="b0003-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0003-117">CommonParameters</span></span>
<span data-ttu-id="b0003-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0003-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0003-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0003-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0003-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0003-120">INPUTS</span></span>

### <span data-ttu-id="b0003-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b0003-121">None</span></span>

## <span data-ttu-id="b0003-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0003-122">OUTPUTS</span></span>

### <span data-ttu-id="b0003-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="b0003-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="b0003-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0003-124">NOTES</span></span>

## <span data-ttu-id="b0003-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0003-125">RELATED LINKS</span></span>

[<span data-ttu-id="b0003-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b0003-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b0003-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b0003-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b0003-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b0003-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996512"
---
# <span data-ttu-id="c5f57-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c5f57-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="c5f57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5f57-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f57-103">Erstellen einer neuen Whitelist für Threat Intelligence für Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="c5f57-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="c5f57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f57-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5f57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5f57-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f57-106">Mit dem Cmdlet " **New-AzFirewallThreatIntelWhitelist** " wird ein Intel Whitelist-Bedrohungs Objekt erstellt, das beim Erstellen oder Festlegen einer Azure-Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5f57-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="c5f57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5f57-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f57-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5f57-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="c5f57-109">In diesem Beispiel wird eine Intel-Whitelist für Bedrohungen erstellt, die eine FQDN-Whitelist mit zwei Einträgen und eine IP-Adressen-Whitelist mit zwei Einträgen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5f57-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="c5f57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5f57-110">PARAMETERS</span></span>

### <span data-ttu-id="c5f57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f57-111">-DefaultProfile</span></span>
<span data-ttu-id="c5f57-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5f57-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5f57-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="c5f57-113">-FQDN</span></span>
<span data-ttu-id="c5f57-114">Die FQDNs der Bedrohungs-Intel-Whitelist</span><span class="sxs-lookup"><span data-stu-id="c5f57-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="c5f57-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="c5f57-115">-IpAddress</span></span>
<span data-ttu-id="c5f57-116">Die IP-Adressen der Bedrohungs-Intel-Whitelist</span><span class="sxs-lookup"><span data-stu-id="c5f57-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="c5f57-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f57-117">CommonParameters</span></span>
<span data-ttu-id="c5f57-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f57-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f57-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5f57-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f57-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5f57-120">INPUTS</span></span>

### <span data-ttu-id="c5f57-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c5f57-121">None</span></span>

## <span data-ttu-id="c5f57-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5f57-122">OUTPUTS</span></span>

### <span data-ttu-id="c5f57-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c5f57-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="c5f57-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5f57-124">NOTES</span></span>

## <span data-ttu-id="c5f57-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5f57-125">RELATED LINKS</span></span>

[<span data-ttu-id="c5f57-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5f57-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="c5f57-127">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5f57-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="c5f57-128">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5f57-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
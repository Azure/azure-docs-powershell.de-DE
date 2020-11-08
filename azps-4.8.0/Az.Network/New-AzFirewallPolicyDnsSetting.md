---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175043"
---
# <span data-ttu-id="cffcf-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="cffcf-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="cffcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cffcf-102">SYNOPSIS</span></span>
<span data-ttu-id="cffcf-103">Erstellt eine neue DNS-Einstellung für Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="cffcf-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="cffcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cffcf-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cffcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cffcf-105">DESCRIPTION</span></span>
<span data-ttu-id="cffcf-106">Mit dem Cmdlet " **New-AzFirewallPolicyDnsSetting** " wird ein DNS-Einstellungsobjekt für die Azure Firewall-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="cffcf-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="cffcf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cffcf-107">EXAMPLES</span></span>

### <span data-ttu-id="cffcf-108">1. Erstellen einer leeren Richtlinie</span><span class="sxs-lookup"><span data-stu-id="cffcf-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="cffcf-109">In diesem Beispiel wird ein DNS-Einstellungsobjekt mit der Einstellung aktivieren des DNS-Proxys erstellt.</span><span class="sxs-lookup"><span data-stu-id="cffcf-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="cffcf-110">2. Erstellen einer leeren Richtlinie mit dem ThreatIntel-Modus</span><span class="sxs-lookup"><span data-stu-id="cffcf-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="cffcf-111">In diesem Beispiel wird ein DNS-Einstellungsobjekt mit der Einstellung aktivieren des DNS-Proxys und Festlegen von benutzerdefinierten DNS-Servern erstellt.</span><span class="sxs-lookup"><span data-stu-id="cffcf-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="cffcf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cffcf-112">PARAMETERS</span></span>

### <span data-ttu-id="cffcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffcf-113">-DefaultProfile</span></span>
<span data-ttu-id="cffcf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cffcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cffcf-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="cffcf-115">-EnableProxy</span></span>
<span data-ttu-id="cffcf-116">Aktivieren des DNS-Proxys</span><span class="sxs-lookup"><span data-stu-id="cffcf-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="cffcf-117">Standardmäßig ist es deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cffcf-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cffcf-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="cffcf-119">Erfordert DNS-Proxy Funktionen für FQDNs innerhalb von Netzwerkregeln.</span><span class="sxs-lookup"><span data-stu-id="cffcf-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="cffcf-120">Standardmäßig ist es wahr.</span><span class="sxs-lookup"><span data-stu-id="cffcf-120">By default it is true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-121">-Server</span><span class="sxs-lookup"><span data-stu-id="cffcf-121">-Server</span></span>
<span data-ttu-id="cffcf-122">Liste der DNS-Server</span><span class="sxs-lookup"><span data-stu-id="cffcf-122">The list of DNS Servers</span></span>

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

### <span data-ttu-id="cffcf-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cffcf-123">-Confirm</span></span>
<span data-ttu-id="cffcf-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cffcf-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffcf-125">-WhatIf</span></span>
<span data-ttu-id="cffcf-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cffcf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffcf-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cffcf-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffcf-128">CommonParameters</span></span>
<span data-ttu-id="cffcf-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cffcf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffcf-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cffcf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffcf-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cffcf-131">INPUTS</span></span>

### <span data-ttu-id="cffcf-132">Keine</span><span class="sxs-lookup"><span data-stu-id="cffcf-132">None</span></span>

## <span data-ttu-id="cffcf-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cffcf-133">OUTPUTS</span></span>

### <span data-ttu-id="cffcf-134">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="cffcf-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="cffcf-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="cffcf-135">NOTES</span></span>

## <span data-ttu-id="cffcf-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cffcf-136">RELATED LINKS</span></span>

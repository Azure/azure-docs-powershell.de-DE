---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469004"
---
# <span data-ttu-id="e10b8-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="e10b8-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="e10b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e10b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e10b8-103">Erstellt eine neue DNS-Einstellung für die Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e10b8-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="e10b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e10b8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e10b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e10b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e10b8-106">Das **Cmdlet "New-AzFirewallPolicyDnsSetting"** erstellt ein DNS-Einstellungsobjekt für die Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e10b8-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="e10b8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e10b8-107">EXAMPLES</span></span>

### <span data-ttu-id="e10b8-108">1. Erstellen einer leeren Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e10b8-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="e10b8-109">In diesem Beispiel wird ein dns-Einstellungsobjekt erstellt, bei dem die Aktivierung des Dnsproxys aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e10b8-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="e10b8-110">2. Erstellen einer leeren Richtlinie mit dem ThreatIntel-Modus</span><span class="sxs-lookup"><span data-stu-id="e10b8-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="e10b8-111">In diesem Beispiel wird ein dns-Einstellungsobjekt erstellt, bei dem die Aktivierung des DNS-Proxys und die Einstellung von benutzerdefinierten DNS-Servern aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e10b8-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="e10b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e10b8-112">PARAMETERS</span></span>

### <span data-ttu-id="e10b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10b8-113">-DefaultProfile</span></span>
<span data-ttu-id="e10b8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e10b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10b8-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="e10b8-115">-EnableProxy</span></span>
<span data-ttu-id="e10b8-116">Aktivieren Sie den DNS-Proxy.</span><span class="sxs-lookup"><span data-stu-id="e10b8-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="e10b8-117">Standardmäßig ist sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e10b8-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="e10b8-118">-Server</span><span class="sxs-lookup"><span data-stu-id="e10b8-118">-Server</span></span>
<span data-ttu-id="e10b8-119">Die Liste der DNS-Server</span><span class="sxs-lookup"><span data-stu-id="e10b8-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="e10b8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e10b8-120">-Confirm</span></span>
<span data-ttu-id="e10b8-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e10b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10b8-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e10b8-122">-WhatIf</span></span>
<span data-ttu-id="e10b8-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e10b8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10b8-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e10b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10b8-125">CommonParameters</span></span>
<span data-ttu-id="e10b8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10b8-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e10b8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10b8-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e10b8-128">INPUTS</span></span>

### <span data-ttu-id="e10b8-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e10b8-129">None</span></span>

## <span data-ttu-id="e10b8-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e10b8-130">OUTPUTS</span></span>

### <span data-ttu-id="e10b8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="e10b8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="e10b8-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e10b8-132">NOTES</span></span>

## <span data-ttu-id="e10b8-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e10b8-133">RELATED LINKS</span></span>

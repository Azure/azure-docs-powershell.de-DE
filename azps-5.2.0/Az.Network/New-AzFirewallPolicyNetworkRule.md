---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291473"
---
# <span data-ttu-id="0174b-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0174b-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="0174b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0174b-102">SYNOPSIS</span></span>
<span data-ttu-id="0174b-103">Erstellen einer neuen Netzwerkregel für die Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0174b-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="0174b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0174b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0174b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0174b-105">DESCRIPTION</span></span>
<span data-ttu-id="0174b-106">Das **Cmdlet "New-AzFirewallPolicyNetworkRule"** erstellt eine Netzwerkregel für eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0174b-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="0174b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0174b-107">EXAMPLES</span></span>

### <span data-ttu-id="0174b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0174b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="0174b-109">In diesem Beispiel wird eine Netzwerkregel mit Quelladresse, Protokoll, Zieladresse und Zielport erstellt.</span><span class="sxs-lookup"><span data-stu-id="0174b-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="0174b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0174b-110">PARAMETERS</span></span>

### <span data-ttu-id="0174b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-111">-DefaultProfile</span></span>
<span data-ttu-id="0174b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0174b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0174b-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0174b-113">-Description</span></span>
<span data-ttu-id="0174b-114">Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0174b-115">-DestinationAddress</span></span>
<span data-ttu-id="0174b-116">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="0174b-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="0174b-117">-DestinationFqdn</span></span>
<span data-ttu-id="0174b-118">Der Ziel-FQDN der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="0174b-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="0174b-119">-DestinationIpGroup</span></span>
<span data-ttu-id="0174b-120">Die Ziel-IP-Gruppen der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="0174b-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0174b-121">-DestinationPort</span></span>
<span data-ttu-id="0174b-122">Die Zielports der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0174b-123">-Name</span></span>
<span data-ttu-id="0174b-124">Der Name der Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="0174b-124">The name of the Network Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0174b-125">-Protocol</span></span>
<span data-ttu-id="0174b-126">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="0174b-127">-SourceAddress</span></span>
<span data-ttu-id="0174b-128">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="0174b-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="0174b-129">-SourceIpGroup</span></span>
<span data-ttu-id="0174b-130">Die Quell-IP-Gruppen der Regel</span><span class="sxs-lookup"><span data-stu-id="0174b-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="0174b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0174b-131">-Confirm</span></span>
<span data-ttu-id="0174b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0174b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0174b-133">-WhatIf</span></span>
<span data-ttu-id="0174b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0174b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0174b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0174b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0174b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0174b-136">CommonParameters</span></span>
<span data-ttu-id="0174b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0174b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0174b-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0174b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0174b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0174b-139">INPUTS</span></span>

### <span data-ttu-id="0174b-140">Keine</span><span class="sxs-lookup"><span data-stu-id="0174b-140">None</span></span>

## <span data-ttu-id="0174b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0174b-141">OUTPUTS</span></span>

### <span data-ttu-id="0174b-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0174b-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="0174b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0174b-143">NOTES</span></span>

## <span data-ttu-id="0174b-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0174b-144">RELATED LINKS</span></span>

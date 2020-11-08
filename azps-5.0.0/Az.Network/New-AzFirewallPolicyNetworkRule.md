---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178525"
---
# <span data-ttu-id="6488e-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6488e-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="6488e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6488e-102">SYNOPSIS</span></span>
<span data-ttu-id="6488e-103">Erstellen einer neuen Azure Firewall-Richtlinien Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="6488e-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="6488e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6488e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6488e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6488e-105">DESCRIPTION</span></span>
<span data-ttu-id="6488e-106">Das Cmdlet **New-AzFirewallPolicyNetworkRule** erstellt eine Netzwerkregel für eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6488e-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="6488e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6488e-107">EXAMPLES</span></span>

### <span data-ttu-id="6488e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6488e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="6488e-109">In diesem Beispiel wird eine Netzwerkregel mit der Quelladresse, dem Protokoll, der Zieladresse und dem Zielanschluss erstellt.</span><span class="sxs-lookup"><span data-stu-id="6488e-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="6488e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6488e-110">PARAMETERS</span></span>

### <span data-ttu-id="6488e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6488e-111">-DefaultProfile</span></span>
<span data-ttu-id="6488e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6488e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6488e-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6488e-113">-Description</span></span>
<span data-ttu-id="6488e-114">Die Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-114">The description of the rule</span></span>

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

### <span data-ttu-id="6488e-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6488e-115">-DestinationAddress</span></span>
<span data-ttu-id="6488e-116">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="6488e-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="6488e-117">-DestinationFqdn</span></span>
<span data-ttu-id="6488e-118">Der Ziel-FQDN der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="6488e-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="6488e-119">-DestinationIpGroup</span></span>
<span data-ttu-id="6488e-120">Das Ziel ipgroups der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="6488e-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6488e-121">-DestinationPort</span></span>
<span data-ttu-id="6488e-122">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="6488e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6488e-123">-Name</span></span>
<span data-ttu-id="6488e-124">Der Name der Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="6488e-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="6488e-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="6488e-125">-Protocol</span></span>
<span data-ttu-id="6488e-126">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="6488e-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6488e-127">-SourceAddress</span></span>
<span data-ttu-id="6488e-128">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="6488e-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="6488e-129">-SourceIpGroup</span></span>
<span data-ttu-id="6488e-130">Das Quell-ipgroups der Regel</span><span class="sxs-lookup"><span data-stu-id="6488e-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="6488e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6488e-131">-Confirm</span></span>
<span data-ttu-id="6488e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6488e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6488e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6488e-133">-WhatIf</span></span>
<span data-ttu-id="6488e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6488e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6488e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6488e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6488e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6488e-136">CommonParameters</span></span>
<span data-ttu-id="6488e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6488e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6488e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6488e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6488e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6488e-139">INPUTS</span></span>

### <span data-ttu-id="6488e-140">Keine</span><span class="sxs-lookup"><span data-stu-id="6488e-140">None</span></span>

## <span data-ttu-id="6488e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6488e-141">OUTPUTS</span></span>

### <span data-ttu-id="6488e-142">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6488e-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="6488e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6488e-143">NOTES</span></span>

## <span data-ttu-id="6488e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6488e-144">RELATED LINKS</span></span>

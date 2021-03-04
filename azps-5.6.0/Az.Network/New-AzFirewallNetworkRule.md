---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 7b2c78793f5a5e5ae6de8c67ffc214ed5c9b9076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934835"
---
# <span data-ttu-id="5eab1-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5eab1-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="5eab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eab1-102">SYNOPSIS</span></span>
<span data-ttu-id="5eab1-103">Erstellt eine Firewallnetzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="5eab1-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="5eab1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eab1-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eab1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5eab1-105">DESCRIPTION</span></span>
<span data-ttu-id="5eab1-106">Das **Cmdlet New-AzFirewallNetworkRule** erstellt eine Netzwerkregel für die Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="5eab1-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="5eab1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5eab1-107">EXAMPLES</span></span>

### <span data-ttu-id="5eab1-108">Beispiel 1: Erstellen einer Regel für den ganzen TCP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="5eab1-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="5eab1-109">In diesem Beispiel wird eine Regel für den ganzen TCP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="5eab1-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="5eab1-110">Der Benutzer erzwingt, ob Datenverkehr für eine Regel zulässig oder verweigert wird, basierend auf der Regelsammlung, der er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5eab1-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="5eab1-111">Beispiel 2: Erstellen einer Regel für den ganzen TCP-Datenverkehr von 10.0.0.0 bis 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="5eab1-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="5eab1-112">In diesem Beispiel wird eine Regel für den ganzen TCP-Datenverkehr von 10.0.0.0 bis 60.1.5.0:4040 erstellt.</span><span class="sxs-lookup"><span data-stu-id="5eab1-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="5eab1-113">Der Benutzer erzwingt, ob Datenverkehr für eine Regel zulässig oder verweigert wird, basierend auf der Regelsammlung, der er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5eab1-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="5eab1-114">Beispiel 3: Erstellen einer Regel für den ganzen TCP- und ICMP-Datenverkehr aus einer beliebigen Quelle bis 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="5eab1-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="5eab1-115">In diesem Beispiel wird eine Regel für den ganzen TCP-Datenverkehr aus einer beliebigen Quelle bis 10.0.0.0/16 erstellt.</span><span class="sxs-lookup"><span data-stu-id="5eab1-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="5eab1-116">Der Benutzer erzwingt, ob Datenverkehr für eine Regel zulässig oder verweigert wird, basierend auf der Regelsammlung, der er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5eab1-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="5eab1-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5eab1-117">PARAMETERS</span></span>

### <span data-ttu-id="5eab1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eab1-118">-DefaultProfile</span></span>
<span data-ttu-id="5eab1-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eab1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eab1-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5eab1-120">-Description</span></span>
<span data-ttu-id="5eab1-121">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="5eab1-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5eab1-122">-DestinationAddress</span></span>
<span data-ttu-id="5eab1-123">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="5eab1-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="5eab1-124">-DestinationFqdn</span></span>
<span data-ttu-id="5eab1-125">Das Ziel-FQDN der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="5eab1-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-126">-DestinationIpGroup</span></span>
<span data-ttu-id="5eab1-127">Die Ziel-IP-Gruppe der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="5eab1-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5eab1-128">-DestinationPort</span></span>
<span data-ttu-id="5eab1-129">Die Zielports der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5eab1-130">-Name</span></span>
<span data-ttu-id="5eab1-131">Gibt den Namen dieser Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="5eab1-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="5eab1-132">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5eab1-132">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5eab1-133">-Protocol</span></span>
<span data-ttu-id="5eab1-134">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eab1-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="5eab1-135">Mögliche Werte sind TCP, UDP, ICMP und Any.</span><span class="sxs-lookup"><span data-stu-id="5eab1-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5eab1-136">-SourceAddress</span></span>
<span data-ttu-id="5eab1-137">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="5eab1-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-138">-SourceIpGroup</span></span>
<span data-ttu-id="5eab1-139">Die Quell-IP-Gruppe der Regel</span><span class="sxs-lookup"><span data-stu-id="5eab1-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="5eab1-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5eab1-140">-Confirm</span></span>
<span data-ttu-id="5eab1-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5eab1-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eab1-142">-WhatIf</span></span>
<span data-ttu-id="5eab1-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5eab1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eab1-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5eab1-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eab1-145">CommonParameters</span></span>
<span data-ttu-id="5eab1-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eab1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eab1-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eab1-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eab1-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5eab1-148">INPUTS</span></span>

### <span data-ttu-id="5eab1-149">Keine</span><span class="sxs-lookup"><span data-stu-id="5eab1-149">None</span></span>

## <span data-ttu-id="5eab1-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5eab1-150">OUTPUTS</span></span>

### <span data-ttu-id="5eab1-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5eab1-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="5eab1-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5eab1-152">NOTES</span></span>

## <span data-ttu-id="5eab1-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5eab1-153">RELATED LINKS</span></span>

[<span data-ttu-id="5eab1-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5eab1-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="5eab1-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5eab1-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="5eab1-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5eab1-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

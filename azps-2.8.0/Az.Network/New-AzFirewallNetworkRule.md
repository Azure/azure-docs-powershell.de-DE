---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 06cac261d368dfafa19b96b42945ed9cda613122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821592"
---
# <span data-ttu-id="ad6c5-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad6c5-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="ad6c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6c5-103">Erstellt eine Firewall-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="ad6c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad6c5-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad6c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6c5-106">Das Cmdlet **New-AzFirewallNetworkRule** erstellt eine Netzwerkregel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="ad6c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ad6c5-108">1: Erstellen einer Regel für den gesamten TCP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="ad6c5-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="ad6c5-109">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="ad6c5-110">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ad6c5-111">2: Erstellen einer Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="ad6c5-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="ad6c5-112">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="ad6c5-113">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ad6c5-114">3: Erstellen einer Regel für den gesamten TCP-und ICMP-Datenverkehr von einer beliebigen Quelle zu 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="ad6c5-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="ad6c5-115">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040 erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="ad6c5-116">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="ad6c5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad6c5-117">PARAMETERS</span></span>

### <span data-ttu-id="ad6c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6c5-118">-DefaultProfile</span></span>
<span data-ttu-id="ad6c5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad6c5-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad6c5-120">-Description</span></span>
<span data-ttu-id="ad6c5-121">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ad6c5-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ad6c5-122">-DestinationAddress</span></span>
<span data-ttu-id="ad6c5-123">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="ad6c5-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ad6c5-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ad6c5-124">-DestinationPort</span></span>
<span data-ttu-id="ad6c5-125">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="ad6c5-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ad6c5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ad6c5-126">-Name</span></span>
<span data-ttu-id="ad6c5-127">Gibt den Namen dieser Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="ad6c5-128">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ad6c5-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ad6c5-129">-Protocol</span></span>
<span data-ttu-id="ad6c5-130">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="ad6c5-131">Mögliche Werte sind TCP, UDP, ICMP und any.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="ad6c5-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ad6c5-132">-SourceAddress</span></span>
<span data-ttu-id="ad6c5-133">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="ad6c5-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ad6c5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad6c5-134">-Confirm</span></span>
<span data-ttu-id="ad6c5-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad6c5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6c5-136">-WhatIf</span></span>
<span data-ttu-id="ad6c5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6c5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad6c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6c5-139">CommonParameters</span></span>
<span data-ttu-id="ad6c5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6c5-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6c5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6c5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad6c5-142">INPUTS</span></span>

### <span data-ttu-id="ad6c5-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ad6c5-143">None</span></span>

## <span data-ttu-id="ad6c5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad6c5-144">OUTPUTS</span></span>

### <span data-ttu-id="ad6c5-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad6c5-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ad6c5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad6c5-146">NOTES</span></span>

## <span data-ttu-id="ad6c5-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad6c5-147">RELATED LINKS</span></span>

[<span data-ttu-id="ad6c5-148">Neu – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad6c5-148">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="ad6c5-149">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ad6c5-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ad6c5-150">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ad6c5-150">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480302"
---
# <span data-ttu-id="1f337-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1f337-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="1f337-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f337-102">SYNOPSIS</span></span>
<span data-ttu-id="1f337-103">Erstellt eine Firewall-Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="1f337-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f337-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f337-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f337-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f337-105">DESCRIPTION</span></span>
<span data-ttu-id="1f337-106">Das Cmdlet **New-AzureRmFirewallNetworkRule** erstellt eine Netzwerkregel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="1f337-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="1f337-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f337-107">EXAMPLES</span></span>

### <span data-ttu-id="1f337-108">1: Erstellen einer Regel für den gesamten TCP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="1f337-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="1f337-109">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f337-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="1f337-110">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="1f337-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="1f337-111">2: Erstellen einer Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="1f337-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="1f337-112">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040 erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f337-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="1f337-113">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="1f337-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="1f337-114">3: Erstellen einer Regel für den gesamten TCP-und ICMP-Datenverkehr von einer beliebigen Quelle zu 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="1f337-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="1f337-115">In diesem Beispiel wird eine Regel für den gesamten TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040 erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f337-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="1f337-116">Der Benutzer erzwingt, ob Datenverkehr für eine Regel basierend auf der Regelsammlung, der Sie zugeordnet ist, zugelassen oder verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="1f337-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="1f337-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f337-117">PARAMETERS</span></span>

### <span data-ttu-id="1f337-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f337-118">-DefaultProfile</span></span>
<span data-ttu-id="1f337-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f337-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f337-120">-Description</span></span>
<span data-ttu-id="1f337-121">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="1f337-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="1f337-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1f337-122">-DestinationAddress</span></span>
<span data-ttu-id="1f337-123">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="1f337-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1f337-124">-DestinationPort</span></span>
<span data-ttu-id="1f337-125">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="1f337-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1f337-126">-Name</span></span>
<span data-ttu-id="1f337-127">Gibt den Namen dieser Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="1f337-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="1f337-128">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1f337-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="1f337-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1f337-129">-Protocol</span></span>
<span data-ttu-id="1f337-130">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f337-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="1f337-131">Mögliche Werte sind TCP, UDP, ICMP und any.</span><span class="sxs-lookup"><span data-stu-id="1f337-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="1f337-132">-SourceAddress</span></span>
<span data-ttu-id="1f337-133">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="1f337-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f337-134">-Confirm</span></span>
<span data-ttu-id="1f337-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f337-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f337-136">-WhatIf</span></span>
<span data-ttu-id="1f337-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f337-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f337-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f337-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f337-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f337-139">CommonParameters</span></span>
<span data-ttu-id="1f337-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f337-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f337-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f337-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f337-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f337-142">INPUTS</span></span>

### <span data-ttu-id="1f337-143">Keine</span><span class="sxs-lookup"><span data-stu-id="1f337-143">None</span></span>
<span data-ttu-id="1f337-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1f337-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f337-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f337-145">OUTPUTS</span></span>

### <span data-ttu-id="1f337-146">Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1f337-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="1f337-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f337-147">NOTES</span></span>

## <span data-ttu-id="1f337-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f337-148">RELATED LINKS</span></span>

[<span data-ttu-id="1f337-149">Neu – AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1f337-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="1f337-150">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1f337-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="1f337-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1f337-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

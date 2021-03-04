---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935616"
---
# <span data-ttu-id="8d396-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8d396-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="8d396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d396-102">SYNOPSIS</span></span>
<span data-ttu-id="8d396-103">Erstellt eine Firewall-NAT-Regel.</span><span class="sxs-lookup"><span data-stu-id="8d396-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="8d396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d396-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d396-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d396-105">DESCRIPTION</span></span>
<span data-ttu-id="8d396-106">Das **Cmdlet New-AzFirewallNatRule** erstellt eine NAT-Regel für die Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="8d396-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="8d396-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d396-107">EXAMPLES</span></span>

### <span data-ttu-id="8d396-108">Beispiel 1: Erstellen einer Regel zum DNST für den ganzen TCP-Datenverkehr von 10.0.0.0/24 mit Ziel 10.1.2.3:80 zum Ziel 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="8d396-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="8d396-109">In diesem Beispiel wird eine Regel erstellt, die den datenverkehr, der aus 10.0.0.0/24 stammt, mit ziel 10.1.2.3:80 bis 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="8d396-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="8d396-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d396-110">PARAMETERS</span></span>

### <span data-ttu-id="8d396-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d396-111">-DefaultProfile</span></span>
<span data-ttu-id="8d396-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d396-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d396-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d396-113">-Description</span></span>
<span data-ttu-id="8d396-114">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="8d396-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="8d396-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-115">-DestinationAddress</span></span>
<span data-ttu-id="8d396-116">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="8d396-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="8d396-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8d396-117">-DestinationPort</span></span>
<span data-ttu-id="8d396-118">Die Zielports der Regel</span><span class="sxs-lookup"><span data-stu-id="8d396-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="8d396-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d396-119">-Name</span></span>
<span data-ttu-id="8d396-120">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="8d396-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="8d396-121">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8d396-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="8d396-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8d396-122">-Protocol</span></span>
<span data-ttu-id="8d396-123">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d396-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="8d396-124">Die unterstützten Protokolle sind TCP und UDP.</span><span class="sxs-lookup"><span data-stu-id="8d396-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="8d396-125">Der Sonderwert "Any" ist zulässig, was bedeutet, dass er sowohl tcp als auch UDP, aber keine anderen Protokolle entsprechen wird.</span><span class="sxs-lookup"><span data-stu-id="8d396-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d396-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-126">-SourceAddress</span></span>
<span data-ttu-id="8d396-127">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="8d396-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="8d396-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d396-128">-SourceIpGroup</span></span>
<span data-ttu-id="8d396-129">Die Quell-IP-Gruppe der Regel</span><span class="sxs-lookup"><span data-stu-id="8d396-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="8d396-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="8d396-130">-TranslatedAddress</span></span>
<span data-ttu-id="8d396-131">Gibt das gewünschte Ergebnis der Adressübersetzung an.</span><span class="sxs-lookup"><span data-stu-id="8d396-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="8d396-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="8d396-132">-TranslatedFqdn</span></span>
<span data-ttu-id="8d396-133">Der übersetzte FQDN für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="8d396-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="8d396-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="8d396-134">-TranslatedPort</span></span>
<span data-ttu-id="8d396-135">Gibt das gewünschte Ergebnis der Portübersetzung an.</span><span class="sxs-lookup"><span data-stu-id="8d396-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="8d396-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d396-136">-Confirm</span></span>
<span data-ttu-id="8d396-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d396-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d396-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d396-138">-WhatIf</span></span>
<span data-ttu-id="8d396-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d396-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d396-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d396-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d396-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d396-141">CommonParameters</span></span>
<span data-ttu-id="8d396-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d396-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d396-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d396-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d396-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d396-144">INPUTS</span></span>

### <span data-ttu-id="8d396-145">Keine</span><span class="sxs-lookup"><span data-stu-id="8d396-145">None</span></span>

## <span data-ttu-id="8d396-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d396-146">OUTPUTS</span></span>

### <span data-ttu-id="8d396-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8d396-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="8d396-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d396-148">NOTES</span></span>

## <span data-ttu-id="8d396-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d396-149">RELATED LINKS</span></span>

[<span data-ttu-id="8d396-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8d396-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="8d396-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8d396-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="8d396-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8d396-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

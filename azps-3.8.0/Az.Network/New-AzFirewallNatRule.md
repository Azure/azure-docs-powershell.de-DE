---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c0c6a1b3d868bb3189dc040baac9618e60130033
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845123"
---
# <span data-ttu-id="ce996-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ce996-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="ce996-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce996-102">SYNOPSIS</span></span>
<span data-ttu-id="ce996-103">Erstellt eine Firewall-NAT-Regel.</span><span class="sxs-lookup"><span data-stu-id="ce996-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="ce996-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce996-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce996-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce996-105">DESCRIPTION</span></span>
<span data-ttu-id="ce996-106">Das Cmdlet **New-AzFirewallNatRule** erstellt eine NAT-Regel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="ce996-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="ce996-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce996-107">EXAMPLES</span></span>

### <span data-ttu-id="ce996-108">1: Erstellen einer Regel zum DNAT des gesamten TCP-Datenverkehrs von 10.0.0.0/24 mit Ziel 10.1.2.3:80 bis Ziel 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="ce996-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="ce996-109">In diesem Beispiel wird eine Regel erstellt, die den gesamten Datenverkehr in 10.0.0.0/24 mit dem Ziel 10.1.2.3:80 bis 10.4.5.6:8080 DNAT.</span><span class="sxs-lookup"><span data-stu-id="ce996-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="ce996-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce996-110">PARAMETERS</span></span>

### <span data-ttu-id="ce996-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce996-111">-DefaultProfile</span></span>
<span data-ttu-id="ce996-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce996-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce996-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce996-113">-Description</span></span>
<span data-ttu-id="ce996-114">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="ce996-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ce996-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ce996-115">-DestinationAddress</span></span>
<span data-ttu-id="ce996-116">Die Zieladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="ce996-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ce996-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ce996-117">-DestinationPort</span></span>
<span data-ttu-id="ce996-118">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="ce996-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ce996-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ce996-119">-Name</span></span>
<span data-ttu-id="ce996-120">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="ce996-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="ce996-121">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ce996-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ce996-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ce996-122">-Protocol</span></span>
<span data-ttu-id="ce996-123">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce996-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="ce996-124">Die unterstützten Protokolle sind TCP und UDP.</span><span class="sxs-lookup"><span data-stu-id="ce996-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="ce996-125">Ein spezieller Wert "Any" ist zulässig, was bedeutet, dass er mit TCP und UDP übereinstimmt, aber keine anderen Protokolle.</span><span class="sxs-lookup"><span data-stu-id="ce996-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="ce996-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ce996-126">-SourceAddress</span></span>
<span data-ttu-id="ce996-127">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="ce996-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ce996-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="ce996-128">-SourceIpGroup</span></span>
<span data-ttu-id="ce996-129">Das Quell-ipgroup der Regel</span><span class="sxs-lookup"><span data-stu-id="ce996-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="ce996-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="ce996-130">-TranslatedAddress</span></span>
<span data-ttu-id="ce996-131">Gibt das gewünschte Ergebnis der Adressübersetzung an</span><span class="sxs-lookup"><span data-stu-id="ce996-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="ce996-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="ce996-132">-TranslatedFqdn</span></span>
<span data-ttu-id="ce996-133">Der übersetzte FQDN für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="ce996-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="ce996-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="ce996-134">-TranslatedPort</span></span>
<span data-ttu-id="ce996-135">Gibt das gewünschte Ergebnis der Portübersetzung an</span><span class="sxs-lookup"><span data-stu-id="ce996-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="ce996-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce996-136">-Confirm</span></span>
<span data-ttu-id="ce996-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce996-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce996-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce996-138">-WhatIf</span></span>
<span data-ttu-id="ce996-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce996-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce996-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce996-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce996-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce996-141">CommonParameters</span></span>
<span data-ttu-id="ce996-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce996-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce996-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce996-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce996-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce996-144">INPUTS</span></span>

### <span data-ttu-id="ce996-145">Keine</span><span class="sxs-lookup"><span data-stu-id="ce996-145">None</span></span>

## <span data-ttu-id="ce996-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce996-146">OUTPUTS</span></span>

### <span data-ttu-id="ce996-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ce996-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="ce996-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce996-148">NOTES</span></span>

## <span data-ttu-id="ce996-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce996-149">RELATED LINKS</span></span>

[<span data-ttu-id="ce996-150">Neu – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce996-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="ce996-151">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce996-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ce996-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce996-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

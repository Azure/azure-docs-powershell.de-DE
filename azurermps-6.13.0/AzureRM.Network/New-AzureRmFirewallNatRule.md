---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498309"
---
# <span data-ttu-id="14c35-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="14c35-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="14c35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14c35-102">SYNOPSIS</span></span>
<span data-ttu-id="14c35-103">Erstellt eine Firewall-NAT-Regel.</span><span class="sxs-lookup"><span data-stu-id="14c35-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c35-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14c35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14c35-105">DESCRIPTION</span></span>
<span data-ttu-id="14c35-106">Das Cmdlet **New-AzureRmFirewallNatRule** erstellt eine NAT-Regel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="14c35-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="14c35-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14c35-107">EXAMPLES</span></span>

### <span data-ttu-id="14c35-108">1: Erstellen einer Regel zum DNAT des gesamten TCP-Datenverkehrs von 10.0.0.0/24 mit Ziel 10.1.2.3:80 bis Ziel 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="14c35-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="14c35-109">In diesem Beispiel wird eine Regel erstellt, die den gesamten Datenverkehr in 10.0.0.0/24 mit dem Ziel 10.1.2.3:80 bis 10.4.5.6:8080 DNAT.</span><span class="sxs-lookup"><span data-stu-id="14c35-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="14c35-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14c35-110">PARAMETERS</span></span>

### <span data-ttu-id="14c35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c35-111">-DefaultProfile</span></span>
<span data-ttu-id="14c35-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14c35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c35-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14c35-113">-Description</span></span>
<span data-ttu-id="14c35-114">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="14c35-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="14c35-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="14c35-115">-DestinationAddress</span></span>
<span data-ttu-id="14c35-116">Die Zieladressen der Regel.</span><span class="sxs-lookup"><span data-stu-id="14c35-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="14c35-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="14c35-117">-DestinationPort</span></span>
<span data-ttu-id="14c35-118">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="14c35-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="14c35-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14c35-119">-Name</span></span>
<span data-ttu-id="14c35-120">Gibt den Namen dieser NAT-Regel an.</span><span class="sxs-lookup"><span data-stu-id="14c35-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="14c35-121">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="14c35-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="14c35-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="14c35-122">-Protocol</span></span>
<span data-ttu-id="14c35-123">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14c35-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="14c35-124">Die unterstützten Protokolle sind TCP und UDP.</span><span class="sxs-lookup"><span data-stu-id="14c35-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="14c35-125">Ein spezieller Wert "Any" ist zulässig, was bedeutet, dass er mit TCP und UDP übereinstimmt, aber keine anderen Protokolle.</span><span class="sxs-lookup"><span data-stu-id="14c35-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c35-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="14c35-126">-SourceAddress</span></span>
<span data-ttu-id="14c35-127">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="14c35-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="14c35-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="14c35-128">-TranslatedAddress</span></span>
<span data-ttu-id="14c35-129">Gibt das gewünschte Ergebnis der Adressübersetzung an</span><span class="sxs-lookup"><span data-stu-id="14c35-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="14c35-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="14c35-130">-TranslatedPort</span></span>
<span data-ttu-id="14c35-131">Gibt das gewünschte Ergebnis der Portübersetzung an</span><span class="sxs-lookup"><span data-stu-id="14c35-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="14c35-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14c35-132">-Confirm</span></span>
<span data-ttu-id="14c35-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14c35-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14c35-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14c35-134">-WhatIf</span></span>
<span data-ttu-id="14c35-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14c35-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14c35-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14c35-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14c35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c35-137">CommonParameters</span></span>
<span data-ttu-id="14c35-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c35-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c35-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c35-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14c35-140">INPUTS</span></span>

### <span data-ttu-id="14c35-141">Keine</span><span class="sxs-lookup"><span data-stu-id="14c35-141">None</span></span>
<span data-ttu-id="14c35-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="14c35-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14c35-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14c35-143">OUTPUTS</span></span>

### <span data-ttu-id="14c35-144">Microsoft. Azure. Commands. Network. Models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="14c35-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="14c35-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="14c35-145">NOTES</span></span>

## <span data-ttu-id="14c35-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14c35-146">RELATED LINKS</span></span>

[<span data-ttu-id="14c35-147">Neu – AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="14c35-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="14c35-148">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="14c35-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="14c35-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="14c35-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

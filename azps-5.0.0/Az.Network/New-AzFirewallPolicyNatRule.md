---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302718"
---
# <span data-ttu-id="65676-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="65676-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="65676-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65676-102">SYNOPSIS</span></span>
<span data-ttu-id="65676-103">Erstellen einer neuen Azure Firewall-Richtlinien NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="65676-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="65676-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65676-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65676-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65676-105">DESCRIPTION</span></span>
<span data-ttu-id="65676-106">Das Cmdlet **New-AzFirewallPolicyNatRule** erstellt eine NAT-Regel für eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="65676-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="65676-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65676-107">EXAMPLES</span></span>

### <span data-ttu-id="65676-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65676-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="65676-109">In diesem Beispiel wird eine NAT-Regel mit der Quelladresse, dem Protokoll, der Zieladresse, dem Ziel-Port, der übersetzten Adresse und dem übersetzten Port erstellt.</span><span class="sxs-lookup"><span data-stu-id="65676-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="65676-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65676-110">PARAMETERS</span></span>

### <span data-ttu-id="65676-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65676-111">-DefaultProfile</span></span>
<span data-ttu-id="65676-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65676-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65676-113">-Name</span><span class="sxs-lookup"><span data-stu-id="65676-113">-Name</span></span>
<span data-ttu-id="65676-114">Der Name der NAT-Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="65676-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="65676-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65676-115">-Description</span></span>
<span data-ttu-id="65676-116">Die Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="65676-116">The description of the rule</span></span>

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

### <span data-ttu-id="65676-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="65676-117">-DestinationAddress</span></span>
<span data-ttu-id="65676-118">Die Zieladressen der Regel.</span><span class="sxs-lookup"><span data-stu-id="65676-118">The destination addresses of the rule.</span></span> <span data-ttu-id="65676-119">Dies muss eine öffentliche IP-Adresse der Firewall sein.</span><span class="sxs-lookup"><span data-stu-id="65676-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="65676-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="65676-120">-DestinationPort</span></span>
<span data-ttu-id="65676-121">Die Zielanschlüsse der Regel</span><span class="sxs-lookup"><span data-stu-id="65676-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="65676-122">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="65676-122">-Protocols</span></span>
<span data-ttu-id="65676-123">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="65676-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="65676-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="65676-124">-SourceAddress</span></span>
<span data-ttu-id="65676-125">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="65676-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="65676-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="65676-126">-SourceIpGroup</span></span>
<span data-ttu-id="65676-127">Das Quell-ipgroups der Regel</span><span class="sxs-lookup"><span data-stu-id="65676-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="65676-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="65676-128">-TranslatedAddress</span></span>
<span data-ttu-id="65676-129">Die übersetzte Adresse für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="65676-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="65676-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="65676-130">-TranslatedPort</span></span>
<span data-ttu-id="65676-131">Der übersetzte Port für diese NAT-Regel</span><span class="sxs-lookup"><span data-stu-id="65676-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="65676-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65676-132">-Confirm</span></span>
<span data-ttu-id="65676-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65676-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65676-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65676-134">-WhatIf</span></span>
<span data-ttu-id="65676-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65676-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65676-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65676-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65676-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65676-137">CommonParameters</span></span>
<span data-ttu-id="65676-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65676-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65676-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65676-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65676-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65676-140">INPUTS</span></span>

### <span data-ttu-id="65676-141">Keine</span><span class="sxs-lookup"><span data-stu-id="65676-141">None</span></span>

## <span data-ttu-id="65676-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65676-142">OUTPUTS</span></span>

### <span data-ttu-id="65676-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="65676-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="65676-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="65676-144">NOTES</span></span>

## <span data-ttu-id="65676-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65676-145">RELATED LINKS</span></span>

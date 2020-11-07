---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660550"
---
# <span data-ttu-id="d097c-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d097c-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="d097c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d097c-102">SYNOPSIS</span></span>
<span data-ttu-id="d097c-103">Erstellt eine Firewallregel für eine Firewall-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d097c-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="d097c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d097c-104">SYNTAX</span></span>

### <span data-ttu-id="d097c-105">TargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="d097c-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d097c-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d097c-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d097c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d097c-107">DESCRIPTION</span></span>
<span data-ttu-id="d097c-108">Das Cmdlet **New-AzFirewallApplicationRule** erstellt eine Anwendungsregel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="d097c-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="d097c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d097c-109">EXAMPLES</span></span>

### <span data-ttu-id="d097c-110">1: Erstellen einer Regel zum Zulassen des gesamten HTTPS-Datenverkehrs von 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="d097c-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="d097c-111">In diesem Beispiel wird eine Regel erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 von 10.0.0.0 aus ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d097c-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="d097c-112">2: Erstellen einer Regel zum Zulassen von Windows für 10.0.0.0/24-Subnetz</span><span class="sxs-lookup"><span data-stu-id="d097c-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="d097c-113">In diesem Beispiel wird eine Regel erstellt, mit der Datenverkehr für Windows-Updates für 10.0.0.0/24-Domäne zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="d097c-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="d097c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d097c-114">PARAMETERS</span></span>

### <span data-ttu-id="d097c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d097c-115">-DefaultProfile</span></span>
<span data-ttu-id="d097c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d097c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d097c-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d097c-117">-Description</span></span>
<span data-ttu-id="d097c-118">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="d097c-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d097c-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d097c-119">-FqdnTag</span></span>
<span data-ttu-id="d097c-120">Gibt eine Liste von FQDN-Tags für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="d097c-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="d097c-121">Die verfügbaren Tags können mit dem Cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d097c-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d097c-122">-Name</span></span>
<span data-ttu-id="d097c-123">Gibt den Namen dieser Anwendungsregel an.</span><span class="sxs-lookup"><span data-stu-id="d097c-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="d097c-124">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d097c-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d097c-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d097c-125">-Protocol</span></span>
<span data-ttu-id="d097c-126">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d097c-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="d097c-127">Das Format lautet <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="d097c-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="d097c-128">Beispielsweise "http: 80" oder "https: 443".</span><span class="sxs-lookup"><span data-stu-id="d097c-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="d097c-129">Das Protokoll ist bei Verwendung von TargetFqdn obligatorisch, kann jedoch nicht mit FqdnTag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d097c-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="d097c-130">Die unterstützten Protokolle sind http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d097c-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097c-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d097c-131">-SourceAddress</span></span>
<span data-ttu-id="d097c-132">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="d097c-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d097c-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="d097c-133">-TargetFqdn</span></span>
<span data-ttu-id="d097c-134">Gibt eine Liste der Domänennamen an, die nach dieser Regel gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="d097c-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="d097c-135">Das Asterik-Zeichen ' *' wird nur als erstes Zeichen eines FQDN in der Liste akzeptiert. Wenn Sie verwendet wird, entspricht die Asterik einer beliebigen Anzahl von Zeichen. (Beispiel: "* MSN.com" entspricht MSN.com und allen zugehörigen Unterdomänen)</span><span class="sxs-lookup"><span data-stu-id="d097c-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097c-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d097c-136">-Confirm</span></span>
<span data-ttu-id="d097c-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d097c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d097c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d097c-138">-WhatIf</span></span>
<span data-ttu-id="d097c-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d097c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d097c-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d097c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d097c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d097c-141">CommonParameters</span></span>
<span data-ttu-id="d097c-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d097c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d097c-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d097c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d097c-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d097c-144">INPUTS</span></span>

### <span data-ttu-id="d097c-145">Keine</span><span class="sxs-lookup"><span data-stu-id="d097c-145">None</span></span>

## <span data-ttu-id="d097c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d097c-146">OUTPUTS</span></span>

### <span data-ttu-id="d097c-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d097c-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="d097c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d097c-148">NOTES</span></span>

## <span data-ttu-id="d097c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d097c-149">RELATED LINKS</span></span>

[<span data-ttu-id="d097c-150">Neu – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d097c-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="d097c-151">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d097c-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d097c-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d097c-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d097c-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d097c-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)

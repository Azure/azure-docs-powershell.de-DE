---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175062"
---
# <span data-ttu-id="7538f-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="7538f-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="7538f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7538f-102">SYNOPSIS</span></span>
<span data-ttu-id="7538f-103">Erstellt eine Firewallregel für eine Firewall-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7538f-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="7538f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7538f-104">SYNTAX</span></span>

### <span data-ttu-id="7538f-105">TargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="7538f-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7538f-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="7538f-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7538f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7538f-107">DESCRIPTION</span></span>
<span data-ttu-id="7538f-108">Das Cmdlet **New-AzFirewallApplicationRule** erstellt eine Anwendungsregel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="7538f-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="7538f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7538f-109">EXAMPLES</span></span>

### <span data-ttu-id="7538f-110">Beispiel 1: Erstellen einer Regel zum Zulassen des gesamten HTTPS-Datenverkehrs von 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="7538f-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="7538f-111">In diesem Beispiel wird eine Regel erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 von 10.0.0.0 aus ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7538f-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="7538f-112">Beispiel 2: Erstellen einer Regel zum Zulassen von Windows für 10.0.0.0/24-Subnetz</span><span class="sxs-lookup"><span data-stu-id="7538f-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="7538f-113">In diesem Beispiel wird eine Regel erstellt, mit der Datenverkehr für Windows-Updates für 10.0.0.0/24-Domäne zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="7538f-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="7538f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7538f-114">PARAMETERS</span></span>

### <span data-ttu-id="7538f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7538f-115">-DefaultProfile</span></span>
<span data-ttu-id="7538f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7538f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7538f-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7538f-117">-Description</span></span>
<span data-ttu-id="7538f-118">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="7538f-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="7538f-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="7538f-119">-FqdnTag</span></span>
<span data-ttu-id="7538f-120">Gibt eine Liste von FQDN-Tags für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="7538f-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="7538f-121">Die verfügbaren Tags können mit dem Cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7538f-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="7538f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7538f-122">-Name</span></span>
<span data-ttu-id="7538f-123">Gibt den Namen dieser Anwendungsregel an.</span><span class="sxs-lookup"><span data-stu-id="7538f-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="7538f-124">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7538f-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="7538f-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7538f-125">-Protocol</span></span>
<span data-ttu-id="7538f-126">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7538f-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="7538f-127">Das Format lautet <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="7538f-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="7538f-128">Beispielsweise "http: 80" oder "https: 443".</span><span class="sxs-lookup"><span data-stu-id="7538f-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="7538f-129">Das Protokoll ist bei Verwendung von TargetFqdn obligatorisch, kann jedoch nicht mit FqdnTag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7538f-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="7538f-130">Die unterstützten Protokolle sind http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7538f-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="7538f-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7538f-131">-SourceAddress</span></span>
<span data-ttu-id="7538f-132">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="7538f-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="7538f-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7538f-133">-SourceIpGroup</span></span>
<span data-ttu-id="7538f-134">Das Quell-ipgroup der Regel</span><span class="sxs-lookup"><span data-stu-id="7538f-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="7538f-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="7538f-135">-TargetFqdn</span></span>
<span data-ttu-id="7538f-136">Gibt eine Liste der Domänennamen an, die nach dieser Regel gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="7538f-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="7538f-137">Das Sternchen " *'" wird nur als erstes Zeichen eines FQDN in der Liste akzeptiert. Bei Verwendung entspricht das Sternchen einer beliebigen Anzahl von Zeichen. (Beispiel: "* MSN.com" entspricht MSN.com und allen zugehörigen Unterdomänen)</span><span class="sxs-lookup"><span data-stu-id="7538f-137">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="7538f-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7538f-138">-Confirm</span></span>
<span data-ttu-id="7538f-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7538f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7538f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7538f-140">-WhatIf</span></span>
<span data-ttu-id="7538f-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7538f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7538f-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7538f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7538f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7538f-143">CommonParameters</span></span>
<span data-ttu-id="7538f-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7538f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7538f-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7538f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7538f-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7538f-146">INPUTS</span></span>

### <span data-ttu-id="7538f-147">Keine</span><span class="sxs-lookup"><span data-stu-id="7538f-147">None</span></span>

## <span data-ttu-id="7538f-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7538f-148">OUTPUTS</span></span>

### <span data-ttu-id="7538f-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="7538f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="7538f-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="7538f-150">NOTES</span></span>

## <span data-ttu-id="7538f-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7538f-151">RELATED LINKS</span></span>

[<span data-ttu-id="7538f-152">Neu – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7538f-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="7538f-153">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7538f-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7538f-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7538f-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7538f-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="7538f-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)

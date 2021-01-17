---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469044"
---
# <span data-ttu-id="e5c52-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e5c52-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="e5c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c52-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c52-103">Erstellt eine Firewallanwendungsregel.</span><span class="sxs-lookup"><span data-stu-id="e5c52-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="e5c52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5c52-104">SYNTAX</span></span>

### <span data-ttu-id="e5c52-105">TargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5c52-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c52-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e5c52-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5c52-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5c52-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c52-108">Das **Cmdlet "New-AzFirewallApplicationRule"** erstellt eine Anwendungsregel für die Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="e5c52-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="e5c52-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5c52-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c52-110">Beispiel 1: Erstellen einer Regel zum Zulassen des sämtlichen HTTPS-Datenverkehrs von 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="e5c52-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="e5c52-111">In diesem Beispiel wird eine Regel erstellt, die den ganzen HTTPS-Datenverkehr auf Port 443 von 10.0.0.0 zu lässt.</span><span class="sxs-lookup"><span data-stu-id="e5c52-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="e5c52-112">Beispiel 2: Erstellen einer Regel zum Zulassen von WindowsUpdate für 10.0.0.0/24-Subnetz</span><span class="sxs-lookup"><span data-stu-id="e5c52-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="e5c52-113">In diesem Beispiel wird eine Regel erstellt, die Datenverkehr für Windows Updates für die Domäne 10.0.0.0/24 zu erlaubt.</span><span class="sxs-lookup"><span data-stu-id="e5c52-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="e5c52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c52-114">PARAMETERS</span></span>

### <span data-ttu-id="e5c52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c52-115">-DefaultProfile</span></span>
<span data-ttu-id="e5c52-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5c52-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c52-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5c52-117">-Description</span></span>
<span data-ttu-id="e5c52-118">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="e5c52-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="e5c52-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e5c52-119">-FqdnTag</span></span>
<span data-ttu-id="e5c52-120">Gibt eine Liste der FQDN-Tags für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="e5c52-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="e5c52-121">Die verfügbaren Tags können mit dem [Cmdlet "Get-AzFirewallFqdnTag"](./Get-AzFirewallFqdnTag.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e5c52-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="e5c52-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e5c52-122">-Name</span></span>
<span data-ttu-id="e5c52-123">Gibt den Namen dieser Anwendungsregel an.</span><span class="sxs-lookup"><span data-stu-id="e5c52-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="e5c52-124">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="e5c52-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="e5c52-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e5c52-125">-Protocol</span></span>
<span data-ttu-id="e5c52-126">Gibt den Typ des Datenverkehrs an, der von dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5c52-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="e5c52-127">Das Format <protocol type> ist: <port></span><span class="sxs-lookup"><span data-stu-id="e5c52-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="e5c52-128">Beispiel: "http:80" oder "https:443".</span><span class="sxs-lookup"><span data-stu-id="e5c52-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="e5c52-129">Das Protokoll ist bei Verwendung von TargetFqdn obligatorisch, kann aber nicht mit FqdnTag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5c52-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="e5c52-130">Die unterstützten Protokolle sind HTTP und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5c52-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="e5c52-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e5c52-131">-SourceAddress</span></span>
<span data-ttu-id="e5c52-132">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="e5c52-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="e5c52-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e5c52-133">-SourceIpGroup</span></span>
<span data-ttu-id="e5c52-134">Die Quell-IP-Gruppe der Regel</span><span class="sxs-lookup"><span data-stu-id="e5c52-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="e5c52-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e5c52-135">-TargetFqdn</span></span>
<span data-ttu-id="e5c52-136">Gibt eine Liste von Domänennamen an, die nach dieser Regel gefiltert sind.</span><span class="sxs-lookup"><span data-stu-id="e5c52-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="e5c52-137">Das Sternchen ' ' wird nur als erstes Zeichen eines *FQDNs in der Liste akzeptiert. Bei Verwendung ersetzt das Sternchen eine beliebige Anzahl von Zeichen. (z. B. "msn.com"* entspricht msn.com und allen unterdomänen Domänen.)</span><span class="sxs-lookup"><span data-stu-id="e5c52-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="e5c52-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5c52-138">-Confirm</span></span>
<span data-ttu-id="e5c52-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5c52-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c52-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e5c52-140">-WhatIf</span></span>
<span data-ttu-id="e5c52-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5c52-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c52-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5c52-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c52-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c52-143">CommonParameters</span></span>
<span data-ttu-id="e5c52-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c52-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c52-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c52-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c52-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5c52-146">INPUTS</span></span>

### <span data-ttu-id="e5c52-147">Keine</span><span class="sxs-lookup"><span data-stu-id="e5c52-147">None</span></span>

## <span data-ttu-id="e5c52-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5c52-148">OUTPUTS</span></span>

### <span data-ttu-id="e5c52-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e5c52-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="e5c52-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5c52-150">NOTES</span></span>

## <span data-ttu-id="e5c52-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5c52-151">RELATED LINKS</span></span>

[<span data-ttu-id="e5c52-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e5c52-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="e5c52-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e5c52-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e5c52-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e5c52-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="e5c52-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e5c52-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664822"
---
# <span data-ttu-id="439a6-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="439a6-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="439a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="439a6-102">SYNOPSIS</span></span>
<span data-ttu-id="439a6-103">Erstellt eine Firewallregel für eine Firewall-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="439a6-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="439a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="439a6-104">SYNTAX</span></span>

### <span data-ttu-id="439a6-105">TargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="439a6-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="439a6-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="439a6-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="439a6-107">DESCRIPTION</span></span>
<span data-ttu-id="439a6-108">Das Cmdlet **New-AzureRmFirewallApplicationRule** erstellt eine Anwendungsregel für Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="439a6-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="439a6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="439a6-109">EXAMPLES</span></span>

### <span data-ttu-id="439a6-110">1: Erstellen einer Regel zum Zulassen des gesamten HTTPS-Datenverkehrs von 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="439a6-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="439a6-111">In diesem Beispiel wird eine Regel erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 von 10.0.0.0 aus ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="439a6-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="439a6-112">2: Erstellen einer Regel zum Zulassen von Windows für 10.0.0.0/24-Subnetz</span><span class="sxs-lookup"><span data-stu-id="439a6-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="439a6-113">In diesem Beispiel wird eine Regel erstellt, mit der Datenverkehr für Windows-Updates für 10.0.0.0/24-Domäne zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="439a6-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="439a6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="439a6-114">PARAMETERS</span></span>

### <span data-ttu-id="439a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439a6-115">-DefaultProfile</span></span>
<span data-ttu-id="439a6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="439a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="439a6-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="439a6-117">-Description</span></span>
<span data-ttu-id="439a6-118">Gibt eine optionale Beschreibung dieser Regel an.</span><span class="sxs-lookup"><span data-stu-id="439a6-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="439a6-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="439a6-119">-FqdnTag</span></span>
<span data-ttu-id="439a6-120">Gibt eine Liste von FQDN-Tags für diese Regel an.</span><span class="sxs-lookup"><span data-stu-id="439a6-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="439a6-121">Die verfügbaren Tags können mit dem Cmdlet [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="439a6-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="439a6-122">-Name</span></span>
<span data-ttu-id="439a6-123">Gibt den Namen dieser Anwendungsregel an.</span><span class="sxs-lookup"><span data-stu-id="439a6-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="439a6-124">Der Name muss innerhalb einer Regelsammlung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="439a6-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="439a6-125">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="439a6-125">-Protocol</span></span>
<span data-ttu-id="439a6-126">Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="439a6-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="439a6-127">Das Format lautet <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="439a6-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="439a6-128">Beispielsweise "http: 80" oder "https: 443".</span><span class="sxs-lookup"><span data-stu-id="439a6-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="439a6-129">Das Protokoll ist bei Verwendung von TargetFqdn obligatorisch, kann jedoch nicht mit FqdnTag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="439a6-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="439a6-130">Die unterstützten Protokolle sind http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="439a6-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="439a6-131">-SourceAddress</span></span>
<span data-ttu-id="439a6-132">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="439a6-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="439a6-133">-TargetFqdn</span></span>
<span data-ttu-id="439a6-134">Gibt eine Liste der Domänennamen an, die nach dieser Regel gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="439a6-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="439a6-135">Das Asterik-Zeichen ' *' wird nur als erstes Zeichen eines FQDN in der Liste akzeptiert. Wenn Sie verwendet wird, entspricht die Asterik einer beliebigen Anzahl von Zeichen. (Beispiel: "* MSN.com" entspricht MSN.com und allen zugehörigen Unterdomänen)</span><span class="sxs-lookup"><span data-stu-id="439a6-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="439a6-136">-Confirm</span></span>
<span data-ttu-id="439a6-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="439a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="439a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439a6-138">-WhatIf</span></span>
<span data-ttu-id="439a6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="439a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439a6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="439a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="439a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439a6-141">CommonParameters</span></span>
<span data-ttu-id="439a6-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439a6-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439a6-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="439a6-144">INPUTS</span></span>

### <span data-ttu-id="439a6-145">Keine</span><span class="sxs-lookup"><span data-stu-id="439a6-145">None</span></span>
<span data-ttu-id="439a6-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="439a6-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="439a6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="439a6-147">OUTPUTS</span></span>

### <span data-ttu-id="439a6-148">Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="439a6-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="439a6-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="439a6-149">NOTES</span></span>

## <span data-ttu-id="439a6-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="439a6-150">RELATED LINKS</span></span>

[<span data-ttu-id="439a6-151">Neu – AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="439a6-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="439a6-152">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="439a6-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="439a6-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="439a6-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="439a6-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="439a6-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)

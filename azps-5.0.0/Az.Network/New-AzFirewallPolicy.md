---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301978"
---
# <span data-ttu-id="8235b-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8235b-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="8235b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8235b-102">SYNOPSIS</span></span>
<span data-ttu-id="8235b-103">Erstellt eine neue Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8235b-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="8235b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8235b-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8235b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8235b-105">DESCRIPTION</span></span>
<span data-ttu-id="8235b-106">Das Cmdlet **New-AzFirewallPolicy** erstellt eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8235b-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="8235b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8235b-107">EXAMPLES</span></span>

### <span data-ttu-id="8235b-108">Beispiel 1:1.</span><span class="sxs-lookup"><span data-stu-id="8235b-108">Example 1: 1.</span></span> <span data-ttu-id="8235b-109">Erstellen einer leeren Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8235b-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="8235b-110">In diesem Beispiel wird eine Azure Firewall-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="8235b-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="8235b-111">Beispiel 2:2.</span><span class="sxs-lookup"><span data-stu-id="8235b-111">Example 2: 2.</span></span> <span data-ttu-id="8235b-112">Erstellen einer leeren Richtlinie mit dem ThreatIntel-Modus</span><span class="sxs-lookup"><span data-stu-id="8235b-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="8235b-113">In diesem Beispiel wird eine Azure-Firewall-Richtlinie mit dem Intel-Modus "Bedrohung" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8235b-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="8235b-114">Beispiel 3:3.</span><span class="sxs-lookup"><span data-stu-id="8235b-114">Example 3: 3.</span></span> <span data-ttu-id="8235b-115">Erstellen einer leeren Richtlinie mit der ThreatIntel-Whitelist</span><span class="sxs-lookup"><span data-stu-id="8235b-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="8235b-116">In diesem Beispiel wird eine Azure-Firewall-Richtlinie mit einer Bedrohung für Intel-Whitelist erstellt</span><span class="sxs-lookup"><span data-stu-id="8235b-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="8235b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8235b-117">PARAMETERS</span></span>

### <span data-ttu-id="8235b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8235b-118">-AsJob</span></span>
<span data-ttu-id="8235b-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8235b-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="8235b-120">-BasePolicy</span></span>
<span data-ttu-id="8235b-121">Die Basisrichtlinie, von der geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="8235b-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8235b-122">-DefaultProfile</span></span>
<span data-ttu-id="8235b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8235b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8235b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8235b-124">-Force</span></span>
<span data-ttu-id="8235b-125">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="8235b-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="8235b-126">-Location</span></span>
<span data-ttu-id="8235b-127">Lage.</span><span class="sxs-lookup"><span data-stu-id="8235b-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8235b-128">-Name</span></span>
<span data-ttu-id="8235b-129">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8235b-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8235b-130">-ResourceGroupName</span></span>
<span data-ttu-id="8235b-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8235b-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="8235b-132">-Tag</span></span>
<span data-ttu-id="8235b-133">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8235b-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="8235b-134">-ThreatIntelMode</span></span>
<span data-ttu-id="8235b-135">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="8235b-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="8235b-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="8235b-137">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="8235b-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="8235b-138">-DnsSetting</span></span>
<span data-ttu-id="8235b-139">Die DNS-Einstellung</span><span class="sxs-lookup"><span data-stu-id="8235b-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8235b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8235b-140">-Confirm</span></span>
<span data-ttu-id="8235b-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8235b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8235b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8235b-142">-WhatIf</span></span>
<span data-ttu-id="8235b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8235b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8235b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8235b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8235b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8235b-145">CommonParameters</span></span>
<span data-ttu-id="8235b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8235b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8235b-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8235b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8235b-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8235b-148">INPUTS</span></span>

### <span data-ttu-id="8235b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8235b-149">System.String</span></span>

### <span data-ttu-id="8235b-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8235b-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8235b-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8235b-151">OUTPUTS</span></span>

### <span data-ttu-id="8235b-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8235b-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="8235b-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="8235b-153">NOTES</span></span>

## <span data-ttu-id="8235b-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8235b-154">RELATED LINKS</span></span>

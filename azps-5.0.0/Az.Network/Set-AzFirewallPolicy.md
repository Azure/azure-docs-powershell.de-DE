---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179824"
---
# <span data-ttu-id="32ed0-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="32ed0-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="32ed0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="32ed0-103">Speichert eine modifizierte Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="32ed0-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="32ed0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32ed0-104">SYNTAX</span></span>

### <span data-ttu-id="32ed0-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="32ed0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ed0-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32ed0-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ed0-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32ed0-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ed0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32ed0-108">DESCRIPTION</span></span>
<span data-ttu-id="32ed0-109">Das Cmdlet " **Satz-AzFirewallPolicy** " aktualisiert eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="32ed0-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="32ed0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32ed0-110">EXAMPLES</span></span>

### <span data-ttu-id="32ed0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32ed0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="32ed0-112">In diesem Beispiel wird die Firewall-Richtlinie mit dem neuen Firewallrichtlinie-Richtlinienwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32ed0-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="32ed0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32ed0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="32ed0-114">In diesem Beispiel wird die Firewall-Richtlinie mit dem neuen Intel-Modus "Bedrohung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32ed0-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="32ed0-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="32ed0-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="32ed0-116">In diesem Beispiel wird die Firewall-Richtlinie mit der neuen Bedrohungs-Intel-Whitelist festgelegt</span><span class="sxs-lookup"><span data-stu-id="32ed0-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="32ed0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="32ed0-117">PARAMETERS</span></span>

### <span data-ttu-id="32ed0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32ed0-118">-AsJob</span></span>
<span data-ttu-id="32ed0-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32ed0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32ed0-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="32ed0-120">-BasePolicy</span></span>
<span data-ttu-id="32ed0-121">Die Basisrichtlinie, von der geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="32ed0-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="32ed0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ed0-122">-DefaultProfile</span></span>
<span data-ttu-id="32ed0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32ed0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32ed0-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="32ed0-124">-DnsSetting</span></span>
<span data-ttu-id="32ed0-125">Die DNS-Einstellung</span><span class="sxs-lookup"><span data-stu-id="32ed0-125">The DNS Setting</span></span>

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

### <span data-ttu-id="32ed0-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32ed0-126">-InputObject</span></span>
<span data-ttu-id="32ed0-127">Die AzureFirewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="32ed0-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32ed0-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="32ed0-128">-Location</span></span>
<span data-ttu-id="32ed0-129">Lage.</span><span class="sxs-lookup"><span data-stu-id="32ed0-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ed0-130">-Name</span><span class="sxs-lookup"><span data-stu-id="32ed0-130">-Name</span></span>
<span data-ttu-id="32ed0-131">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="32ed0-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ed0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32ed0-132">-ResourceGroupName</span></span>
<span data-ttu-id="32ed0-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32ed0-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ed0-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="32ed0-134">-ResourceId</span></span>
<span data-ttu-id="32ed0-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="32ed0-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ed0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="32ed0-136">-Tag</span></span>
<span data-ttu-id="32ed0-137">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="32ed0-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="32ed0-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="32ed0-138">-ThreatIntelMode</span></span>
<span data-ttu-id="32ed0-139">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="32ed0-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="32ed0-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="32ed0-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="32ed0-141">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="32ed0-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="32ed0-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32ed0-142">-Confirm</span></span>
<span data-ttu-id="32ed0-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32ed0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ed0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ed0-144">-WhatIf</span></span>
<span data-ttu-id="32ed0-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32ed0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ed0-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32ed0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ed0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ed0-147">CommonParameters</span></span>
<span data-ttu-id="32ed0-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ed0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ed0-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32ed0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ed0-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32ed0-150">INPUTS</span></span>

### <span data-ttu-id="32ed0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="32ed0-151">System.String</span></span>

### <span data-ttu-id="32ed0-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="32ed0-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="32ed0-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="32ed0-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32ed0-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32ed0-154">OUTPUTS</span></span>

### <span data-ttu-id="32ed0-155">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="32ed0-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="32ed0-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="32ed0-156">NOTES</span></span>

## <span data-ttu-id="32ed0-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32ed0-157">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156740"
---
# <span data-ttu-id="c6e14-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c6e14-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="c6e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6e14-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e14-103">Speichert eine geänderte Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c6e14-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="c6e14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6e14-104">SYNTAX</span></span>

### <span data-ttu-id="c6e14-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6e14-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e14-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6e14-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e14-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6e14-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e14-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6e14-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e14-109">Das **Cmdlet Set-AzFirewallPolicy** aktualisiert eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c6e14-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="c6e14-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6e14-110">EXAMPLES</span></span>

### <span data-ttu-id="c6e14-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6e14-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="c6e14-112">In diesem Beispiel wird die Firewallrichtlinie mit dem neuen Wert der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="c6e14-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="c6e14-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6e14-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="c6e14-114">In diesem Beispiel wird die Firewallrichtlinie auf den neuen Intel-Modus für Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="c6e14-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="c6e14-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c6e14-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="c6e14-116">In diesem Beispiel wird die Firewallrichtlinie mit der neuen Intel Whitelist für Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="c6e14-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="c6e14-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6e14-117">PARAMETERS</span></span>

### <span data-ttu-id="c6e14-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6e14-118">-AsJob</span></span>
<span data-ttu-id="c6e14-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c6e14-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6e14-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="c6e14-120">-BasePolicy</span></span>
<span data-ttu-id="c6e14-121">Die Basisrichtlinie, von der geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="c6e14-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="c6e14-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e14-122">-DefaultProfile</span></span>
<span data-ttu-id="c6e14-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6e14-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e14-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="c6e14-124">-DnsSetting</span></span>
<span data-ttu-id="c6e14-125">Die Einstellung 'DNS'</span><span class="sxs-lookup"><span data-stu-id="c6e14-125">The DNS Setting</span></span>

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

### <span data-ttu-id="c6e14-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e14-126">-InputObject</span></span>
<span data-ttu-id="c6e14-127">Die AzureFirewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c6e14-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="c6e14-128">-Location</span><span class="sxs-lookup"><span data-stu-id="c6e14-128">-Location</span></span>
<span data-ttu-id="c6e14-129">aus.</span><span class="sxs-lookup"><span data-stu-id="c6e14-129">location.</span></span>

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

### <span data-ttu-id="c6e14-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c6e14-130">-Name</span></span>
<span data-ttu-id="c6e14-131">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c6e14-131">The resource name.</span></span>

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

### <span data-ttu-id="c6e14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e14-132">-ResourceGroupName</span></span>
<span data-ttu-id="c6e14-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6e14-133">The resource group name.</span></span>

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

### <span data-ttu-id="c6e14-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e14-134">-ResourceId</span></span>
<span data-ttu-id="c6e14-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c6e14-135">The resource Id.</span></span>

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

### <span data-ttu-id="c6e14-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6e14-136">-Tag</span></span>
<span data-ttu-id="c6e14-137">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6e14-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c6e14-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="c6e14-138">-ThreatIntelMode</span></span>
<span data-ttu-id="c6e14-139">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="c6e14-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="c6e14-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c6e14-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="c6e14-141">Die Whitelist für Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c6e14-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="c6e14-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6e14-142">-Confirm</span></span>
<span data-ttu-id="c6e14-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6e14-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e14-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c6e14-144">-WhatIf</span></span>
<span data-ttu-id="c6e14-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6e14-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e14-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e14-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e14-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e14-147">CommonParameters</span></span>
<span data-ttu-id="c6e14-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e14-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e14-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6e14-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e14-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6e14-150">INPUTS</span></span>

### <span data-ttu-id="c6e14-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c6e14-151">System.String</span></span>

### <span data-ttu-id="c6e14-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c6e14-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="c6e14-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c6e14-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c6e14-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6e14-154">OUTPUTS</span></span>

### <span data-ttu-id="c6e14-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c6e14-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c6e14-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6e14-156">NOTES</span></span>

## <span data-ttu-id="c6e14-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6e14-157">RELATED LINKS</span></span>

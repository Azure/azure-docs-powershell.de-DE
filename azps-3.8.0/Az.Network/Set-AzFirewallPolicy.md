---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997212"
---
# <span data-ttu-id="999c8-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="999c8-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="999c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="999c8-102">SYNOPSIS</span></span>
<span data-ttu-id="999c8-103">Speichert eine modifizierte Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="999c8-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="999c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="999c8-104">SYNTAX</span></span>

### <span data-ttu-id="999c8-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="999c8-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="999c8-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="999c8-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="999c8-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="999c8-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="999c8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="999c8-108">DESCRIPTION</span></span>
<span data-ttu-id="999c8-109">Das Cmdlet " **Satz-AzFirewallPolicy** " aktualisiert eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="999c8-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="999c8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="999c8-110">EXAMPLES</span></span>

### <span data-ttu-id="999c8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="999c8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="999c8-112">In diesem Beispiel wird die Firewall-Richtlinie mit dem neuen Firewallrichtlinie-Richtlinienwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="999c8-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="999c8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="999c8-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="999c8-114">In diesem Beispiel wird die Firewall-Richtlinie mit dem neuen Intel-Modus "Bedrohung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="999c8-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="999c8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="999c8-115">PARAMETERS</span></span>

### <span data-ttu-id="999c8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="999c8-116">-AsJob</span></span>
<span data-ttu-id="999c8-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="999c8-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="999c8-118">-BasePolicy</span></span>
<span data-ttu-id="999c8-119">Die Basisrichtlinie, von der geerbt werden soll</span><span class="sxs-lookup"><span data-stu-id="999c8-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999c8-120">-DefaultProfile</span></span>
<span data-ttu-id="999c8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="999c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="999c8-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="999c8-122">-InputObject</span></span>
<span data-ttu-id="999c8-123">Die AzureFirewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="999c8-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="999c8-124">-Location</span></span>
<span data-ttu-id="999c8-125">Lage.</span><span class="sxs-lookup"><span data-stu-id="999c8-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="999c8-126">-Name</span></span>
<span data-ttu-id="999c8-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="999c8-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="999c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="999c8-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="999c8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="999c8-130">-ResourceId</span></span>
<span data-ttu-id="999c8-131">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="999c8-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="999c8-132">-Tag</span></span>
<span data-ttu-id="999c8-133">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="999c8-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="999c8-134">-ThreatIntelMode</span></span>
<span data-ttu-id="999c8-135">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="999c8-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="999c8-136">-Confirm</span></span>
<span data-ttu-id="999c8-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="999c8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999c8-138">-WhatIf</span></span>
<span data-ttu-id="999c8-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="999c8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="999c8-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="999c8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999c8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999c8-141">CommonParameters</span></span>
<span data-ttu-id="999c8-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="999c8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999c8-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="999c8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999c8-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="999c8-144">INPUTS</span></span>

### <span data-ttu-id="999c8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="999c8-145">System.String</span></span>

### <span data-ttu-id="999c8-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="999c8-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="999c8-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="999c8-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="999c8-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="999c8-148">OUTPUTS</span></span>

### <span data-ttu-id="999c8-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="999c8-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="999c8-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="999c8-150">NOTES</span></span>

## <span data-ttu-id="999c8-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="999c8-151">RELATED LINKS</span></span>

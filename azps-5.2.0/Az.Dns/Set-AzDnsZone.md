---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302315"
---
# <span data-ttu-id="9bb3b-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="9bb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb3b-103">Aktualisiert die Eigenschaften einer DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="9bb3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bb3b-104">SYNTAX</span></span>

### <span data-ttu-id="9bb3b-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="9bb3b-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb3b-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="9bb3b-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb3b-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="9bb3b-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb3b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bb3b-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb3b-109">Das **Set-AzDnsZone-Cmdlet** aktualisiert die angegebene DNS-Zone im Azure-DNS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="9bb3b-110">Mit diesem Cmdlet werden die Datensatzsätze in der Zone nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="9bb3b-111">Sie können ein **DnsZone-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können die *Parameter "ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9bb3b-112">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9bb3b-113">Wenn eine DNS-Zone als Objekt übergeben wird (mithilfe des Zonenobjekts oder über die Pipeline), wird sie nicht aktualisiert, wenn sie in Azure DNS geändert wurde, seit das lokale "DnsZone"-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9bb3b-114">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9bb3b-115">Sie können dieses Verhalten mit dem Parameter *"Overwrite"* unterdrücken, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="9bb3b-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9bb3b-116">EXAMPLES</span></span>

### <span data-ttu-id="9bb3b-117">Beispiel 1: Aktualisieren einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="9bb3b-118">Der erste Befehl ruft die Zone namens "myzone.com" aus der angegebenen Ressourcengruppe ab und speichert sie dann in $Zone Variable.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="9bb3b-119">Der zweite Befehl aktualisiert die Tags für $Zone.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="9bb3b-120">Der letzte Befehl über committ die Änderung.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-120">The final command commits the change.</span></span>

### <span data-ttu-id="9bb3b-121">Beispiel 2: Aktualisieren von Tags für eine Zone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="9bb3b-122">Mit diesem Befehl werden die Tags für die Zone namens "myzone.com aktualisiert, ohne zuerst die Zone explizit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="9bb3b-123">Beispiel 3: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angeben der ID</span><span class="sxs-lookup"><span data-stu-id="9bb3b-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="9bb3b-124">Mit diesem Befehl wird die private DNS-Zone myprivatezone.com A0 dem virtuellen Netzwerk myvnet als Registrierungsnetzwerk zugeordnet, indem seine ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="9bb3b-125">Beispiel 4: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angeben des Netzwerkobjekts.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="9bb3b-126">Dieser Befehl ordnet die Private -DNS-Zone myprivatezone.com dem virtuellen Netzwerk myvnet als Registrierungsnetzwerk zu, indem das virtuelle Netzwerkobjekt, das durch die Variable $vnet dargestellt wird, an das cmdlet Set-AzDnsZone übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="9bb3b-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bb3b-127">PARAMETERS</span></span>

### <span data-ttu-id="9bb3b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb3b-128">-DefaultProfile</span></span>
<span data-ttu-id="9bb3b-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9bb3b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bb3b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9bb3b-130">-Name</span></span>
<span data-ttu-id="9bb3b-131">Gibt den Namen der zu aktualisierenden DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9bb3b-132">-Overwrite</span></span>
<span data-ttu-id="9bb3b-133">Wenn eine DNS-Zone als Objekt übergeben wird (mithilfe des Zonenobjekts oder über die Pipeline), wird sie nicht aktualisiert, wenn sie in Azure DNS geändert wurde, seit das lokale "DnsZone"-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9bb3b-134">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9bb3b-135">Sie können dieses Verhalten mit dem Parameter *"Overwrite"* unterdrücken, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bb3b-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="9bb3b-137">Die Liste der virtuellen Netzwerke, die Hostnameneinträge für virtuelle Computer in dieser DNS-Zone registrieren, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9bb3b-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="9bb3b-139">Die Liste der virtuellen Netzwerk-IDs, die Hostnameneinträge für virtuelle Computer in dieser DNS-Zone registrieren, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9bb3b-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="9bb3b-141">Die Liste der virtuellen Netzwerke, die Einträge in dieser DNS-Zone auflösen können, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9bb3b-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="9bb3b-143">Die Liste der virtuellen Netzwerk-IDs, die Einträge in dieser DNS-Zone auflösen können, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb3b-144">-ResourceGroupName</span></span>
<span data-ttu-id="9bb3b-145">Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="9bb3b-146">Sie müssen auch den Parameter "ZoneName" angeben.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="9bb3b-147">Alternativ können Sie die Zone mit einem "DnsZone"-Objekt mit dem *Parameter "Zone"* oder der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bb3b-148">-Tag</span></span>
<span data-ttu-id="9bb3b-149">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9bb3b-150">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9bb3b-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-151">-Zone</span></span>
<span data-ttu-id="9bb3b-152">Gibt die zu aktualisierende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="9bb3b-153">Alternativ können Sie die Zone mit den Parametern *"ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb3b-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bb3b-154">-Confirm</span></span>
<span data-ttu-id="9bb3b-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb3b-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9bb3b-156">-WhatIf</span></span>
<span data-ttu-id="9bb3b-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bb3b-158">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bb3b-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb3b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb3b-160">CommonParameters</span></span>
<span data-ttu-id="9bb3b-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb3b-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb3b-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb3b-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9bb3b-163">INPUTS</span></span>

### <span data-ttu-id="9bb3b-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9bb3b-164">System.String</span></span>

### <span data-ttu-id="9bb3b-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9bb3b-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9bb3b-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9bb3b-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9bb3b-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9bb3b-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9bb3b-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="9bb3b-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9bb3b-169">OUTPUTS</span></span>

### <span data-ttu-id="9bb3b-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="9bb3b-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9bb3b-171">NOTES</span></span>
<span data-ttu-id="9bb3b-172">Mit dem Parameter *"Bestätigen"* können Sie steuern, ob sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9bb3b-173">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn $ConfirmPreference Windows PowerShell Variable den Wert "Mittel" oder "Niedriger" hat.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="9bb3b-174">Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True" angeben,* fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="9bb3b-175">Wenn Sie *"Confirm:$False"* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9bb3b-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9bb3b-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9bb3b-176">RELATED LINKS</span></span>

[<span data-ttu-id="9bb3b-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="9bb3b-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="9bb3b-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9bb3b-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 67997145a327d7f9e47f4cf346cbfd5e3a6bf0f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663149"
---
# <span data-ttu-id="b494e-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="b494e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b494e-102">SYNOPSIS</span></span>
<span data-ttu-id="b494e-103">Aktualisiert die Eigenschaften einer DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="b494e-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b494e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b494e-104">SYNTAX</span></span>

### <span data-ttu-id="b494e-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="b494e-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b494e-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="b494e-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b494e-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="b494e-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b494e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b494e-108">DESCRIPTION</span></span>
<span data-ttu-id="b494e-109">Das Cmdlet " **Satz-AzureRmDnsZone** " aktualisiert die angegebene DNS-Zone im Azure DNS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b494e-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="b494e-110">Mit diesem Cmdlet werden die Daten Satz Sätze in der Zone nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b494e-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="b494e-111">Sie können ein **dnsZone** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="b494e-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b494e-112">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="b494e-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b494e-113">Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b494e-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b494e-114">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b494e-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b494e-115">Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b494e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b494e-116">EXAMPLES</span></span>

### <span data-ttu-id="b494e-117">Beispiel 1: Aktualisieren einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="b494e-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="b494e-118">Der erste Befehl ruft die Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe ab und speichert Sie dann in der $Zone Variablen.</span><span class="sxs-lookup"><span data-stu-id="b494e-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="b494e-119">Mit dem zweiten Befehl werden die Tags für $Zone aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b494e-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="b494e-120">Der endgültige Befehl übernimmt die Änderung.</span><span class="sxs-lookup"><span data-stu-id="b494e-120">The final command commits the change.</span></span>

### <span data-ttu-id="b494e-121">Beispiel 2: Aktualisieren von Tags für eine Zone</span><span class="sxs-lookup"><span data-stu-id="b494e-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="b494e-122">Dieser Befehl aktualisiert die Tags für die Zone mit dem Namen MyZone.com, ohne die Zone zuvor explizit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b494e-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="b494e-123">Beispiel 3: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angabe der ID</span><span class="sxs-lookup"><span data-stu-id="b494e-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="b494e-124">Dieser Befehl ordnet die private DNS Zone myprivatezone.com dem virtuellen Netzwerk myvnet als Registrierungs Netzwerk zu, indem die ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="b494e-125">Beispiel 4: Zuordnen einer privaten Zone zu einem virtuellen Netzwerk durch Angabe des Netzwerkobjekts.</span><span class="sxs-lookup"><span data-stu-id="b494e-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="b494e-126">Dieser Befehl ordnet die private DNS Zone myprivatezone.com dem virtuellen Netzwerk myvnet als Registrierungs Netzwerk zu, indem das durch $vnet Variable dargestellte virtuelle Netzwerkobjekt an das Set-AzureRmDnsZone-Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="b494e-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="b494e-127">PARAMETERS</span></span>

### <span data-ttu-id="b494e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b494e-128">-DefaultProfile</span></span>
<span data-ttu-id="b494e-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b494e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b494e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b494e-130">-Name</span></span>
<span data-ttu-id="b494e-131">Gibt den Namen der zu aktualisierende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="b494e-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="b494e-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b494e-132">-Overwrite</span></span>
<span data-ttu-id="b494e-133">Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b494e-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b494e-134">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b494e-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b494e-135">Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b494e-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b494e-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="b494e-137">In der Liste der virtuellen Netzwerke, die die Hostnamen für virtuelle Maschinen registrieren, werden die Datensätze in dieser DNS-Zone nur für private Zonen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="b494e-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b494e-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b494e-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="b494e-139">Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Maschinen in dieser DNS-Zone registrieren, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b494e-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b494e-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b494e-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="b494e-141">Die Liste der virtuellen Netzwerke, in denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b494e-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b494e-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b494e-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="b494e-143">Die Liste der virtuellen Netzwerk-IDs, mit denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b494e-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="b494e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b494e-144">-ResourceGroupName</span></span>
<span data-ttu-id="b494e-145">Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="b494e-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="b494e-146">Außerdem müssen Sie den Parameter zonename angeben.</span><span class="sxs-lookup"><span data-stu-id="b494e-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="b494e-147">Alternativ können Sie die Zone mithilfe eines dnsZone-Objekts mit dem *Zone* -Parameter oder der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="b494e-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="b494e-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b494e-148">-Tag</span></span>
<span data-ttu-id="b494e-149">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b494e-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b494e-150">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b494e-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b494e-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="b494e-151">-Zone</span></span>
<span data-ttu-id="b494e-152">Gibt die zu aktualisierende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="b494e-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="b494e-153">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="b494e-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b494e-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b494e-154">-Confirm</span></span>
<span data-ttu-id="b494e-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b494e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b494e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b494e-156">-WhatIf</span></span>
<span data-ttu-id="b494e-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b494e-158">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b494e-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b494e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b494e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b494e-160">CommonParameters</span></span>
<span data-ttu-id="b494e-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b494e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b494e-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b494e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b494e-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b494e-163">INPUTS</span></span>

### <span data-ttu-id="b494e-164">System. String</span><span class="sxs-lookup"><span data-stu-id="b494e-164">System.String</span></span>

### <span data-ttu-id="b494e-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b494e-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b494e-166">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b494e-166">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b494e-167">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. Commands. Common. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b494e-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b494e-168">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b494e-169">Parameter: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b494e-169">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="b494e-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b494e-170">OUTPUTS</span></span>

### <span data-ttu-id="b494e-171">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-171">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b494e-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="b494e-172">NOTES</span></span>
<span data-ttu-id="b494e-173">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="b494e-173">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b494e-174">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="b494e-174">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b494e-175">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b494e-175">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b494e-176">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b494e-176">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b494e-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b494e-177">RELATED LINKS</span></span>

[<span data-ttu-id="b494e-178">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-178">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="b494e-179">Neu – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-179">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="b494e-180">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b494e-180">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

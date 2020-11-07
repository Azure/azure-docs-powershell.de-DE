---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842387"
---
# <span data-ttu-id="92878-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="92878-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="92878-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92878-102">SYNOPSIS</span></span>
<span data-ttu-id="92878-103">Entfernt eine DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="92878-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="92878-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92878-104">SYNTAX</span></span>

### <span data-ttu-id="92878-105">Felder</span><span class="sxs-lookup"><span data-stu-id="92878-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92878-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="92878-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92878-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92878-107">DESCRIPTION</span></span>
<span data-ttu-id="92878-108">Das Cmdlet **Remove-AzDnsZone** löscht endgültig eine DNS-Zone (Domain Name System) aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="92878-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="92878-109">Alle in der Zone enthaltenen Daten Satz Sätze werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="92878-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="92878-110">Sie können ein **dnsZone** -Objekt mithilfe des *Name* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="92878-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="92878-111">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="92878-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="92878-112">Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="92878-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="92878-113">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92878-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="92878-114">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="92878-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="92878-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92878-115">EXAMPLES</span></span>

### <span data-ttu-id="92878-116">Beispiel 1: Entfernen einer Zone</span><span class="sxs-lookup"><span data-stu-id="92878-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="92878-117">Mit diesem Befehl wird die Zone mit dem Namen MyZone.com aus der Ressourcengruppe myresourcegroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="92878-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="92878-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="92878-118">PARAMETERS</span></span>

### <span data-ttu-id="92878-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92878-119">-Force</span></span>
<span data-ttu-id="92878-120">Dieser Parameter ist für dieses Cmdlet veraltet.</span><span class="sxs-lookup"><span data-stu-id="92878-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="92878-121">Sie wird in einer zukünftigen Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="92878-121">It will be removed in a future release.</span></span>

<span data-ttu-id="92878-122">Verwenden Sie den Parameter *Confirm* , um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="92878-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="92878-123">-Name</span><span class="sxs-lookup"><span data-stu-id="92878-123">-Name</span></span>
<span data-ttu-id="92878-124">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="92878-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="92878-125">Sie müssen auch den *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="92878-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="92878-126">Alternativ können Sie die DNS-Zone mithilfe des *Zone* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="92878-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92878-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="92878-127">-Overwrite</span></span>
<span data-ttu-id="92878-128">Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="92878-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="92878-129">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92878-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="92878-130">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="92878-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92878-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92878-131">-PassThru</span></span>
<span data-ttu-id="92878-132">passthru</span><span class="sxs-lookup"><span data-stu-id="92878-132">passthru</span></span>

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

### <span data-ttu-id="92878-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92878-133">-ResourceGroupName</span></span>
<span data-ttu-id="92878-134">Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="92878-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="92878-135">Außerdem müssen Sie den Parameter *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="92878-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="92878-136">Alternativ können Sie die DNS-Zone mithilfe eines **dnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="92878-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92878-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="92878-137">-Zone</span></span>
<span data-ttu-id="92878-138">Gibt die zu löschende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="92878-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="92878-139">Das übergebene **dnsZone** -Objekt kann auch über die Pipeline übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="92878-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="92878-140">Alternativ können Sie die zu löschende DNS-Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="92878-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92878-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92878-141">-Confirm</span></span>
<span data-ttu-id="92878-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92878-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92878-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92878-143">-WhatIf</span></span>
<span data-ttu-id="92878-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92878-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92878-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92878-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92878-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92878-146">CommonParameters</span></span>
<span data-ttu-id="92878-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92878-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92878-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92878-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92878-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92878-149">INPUTS</span></span>

### <span data-ttu-id="92878-150">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="92878-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="92878-151">Sie können ein **dnsZone** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="92878-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="92878-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92878-152">OUTPUTS</span></span>

### <span data-ttu-id="92878-153">Keine</span><span class="sxs-lookup"><span data-stu-id="92878-153">None</span></span>
<span data-ttu-id="92878-154">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="92878-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="92878-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="92878-155">NOTES</span></span>
<span data-ttu-id="92878-156">Aufgrund der potenziell großen Auswirkung des Löschens einer DNS-Zone fordert dieses Cmdlet standardmäßig eine Bestätigung an, wenn die $ConfirmPreference Windows PowerShell-Variable einen anderen Wert als None aufweist.</span><span class="sxs-lookup"><span data-stu-id="92878-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="92878-157">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92878-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="92878-158">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="92878-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="92878-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92878-159">RELATED LINKS</span></span>

[<span data-ttu-id="92878-160">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="92878-160">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="92878-161">Neu – AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="92878-161">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="92878-162">Satz-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="92878-162">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)

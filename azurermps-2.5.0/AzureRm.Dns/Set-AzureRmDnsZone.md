---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 347f590ecd6e2825264e6bb0b980dd94450b0f06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849336"
---
# <span data-ttu-id="67811-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="67811-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67811-102">SYNOPSIS</span></span>
<span data-ttu-id="67811-103">Aktualisiert die Eigenschaften einer DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="67811-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67811-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67811-104">SYNTAX</span></span>

### <span data-ttu-id="67811-105">Felder</span><span class="sxs-lookup"><span data-stu-id="67811-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67811-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="67811-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67811-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67811-107">DESCRIPTION</span></span>
<span data-ttu-id="67811-108">Das Cmdlet " **Satz-AzureRmDnsZone** " aktualisiert die angegebene DNS-Zone im Azure DNS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="67811-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="67811-109">Mit diesem Cmdlet werden die Daten Satz Sätze in der Zone nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="67811-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="67811-110">Sie können ein **dnsZone** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="67811-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="67811-111">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="67811-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="67811-112">Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="67811-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="67811-113">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="67811-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="67811-114">Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="67811-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="67811-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67811-115">EXAMPLES</span></span>

### <span data-ttu-id="67811-116">Beispiel 1: Aktualisieren einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="67811-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="67811-117">Der erste Befehl ruft die Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe ab und speichert Sie dann in der $Zone Variablen.</span><span class="sxs-lookup"><span data-stu-id="67811-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="67811-118">Mit dem zweiten Befehl werden die Tags für $Zone aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="67811-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="67811-119">Der endgültige Befehl übernimmt die Änderung.</span><span class="sxs-lookup"><span data-stu-id="67811-119">The final command commits the change.</span></span>

### <span data-ttu-id="67811-120">Beispiel 2: Aktualisieren von Tags für eine Zone</span><span class="sxs-lookup"><span data-stu-id="67811-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="67811-121">Dieser Befehl aktualisiert die Tags für die Zone mit dem Namen MyZone.com, ohne die Zone zuvor explizit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="67811-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="67811-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="67811-122">PARAMETERS</span></span>

### <span data-ttu-id="67811-123">-Name</span><span class="sxs-lookup"><span data-stu-id="67811-123">-Name</span></span>
<span data-ttu-id="67811-124">Gibt den Namen der zu aktualisierende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="67811-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="67811-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="67811-125">-Overwrite</span></span>
<span data-ttu-id="67811-126">Wenn Sie eine DNS-Zone als Objekt (mithilfe des Zone-Objekts oder über die Pipeline) übergeben, wird Sie nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, seit das lokale dnsZone-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="67811-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="67811-127">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="67811-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="67811-128">Sie können dieses Verhalten mit dem Parameter *overwrite* unterdrücken, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="67811-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="67811-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67811-129">-ResourceGroupName</span></span>
<span data-ttu-id="67811-130">Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="67811-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="67811-131">Außerdem müssen Sie den Parameter zonename angeben.</span><span class="sxs-lookup"><span data-stu-id="67811-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="67811-132">Alternativ können Sie die Zone mithilfe eines dnsZone-Objekts mit dem *Zone* -Parameter oder der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="67811-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="67811-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="67811-133">-Tag</span></span>
<span data-ttu-id="67811-134">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="67811-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="67811-135">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="67811-135">For example:</span></span>

<span data-ttu-id="67811-136">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="67811-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67811-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="67811-137">-Zone</span></span>
<span data-ttu-id="67811-138">Gibt die zu aktualisierende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="67811-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="67811-139">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="67811-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="67811-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67811-140">-Confirm</span></span>
<span data-ttu-id="67811-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67811-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67811-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67811-142">-WhatIf</span></span>
<span data-ttu-id="67811-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67811-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67811-144">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67811-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67811-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67811-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67811-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67811-146">CommonParameters</span></span>
<span data-ttu-id="67811-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67811-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67811-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67811-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67811-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67811-149">INPUTS</span></span>

### <span data-ttu-id="67811-150">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="67811-151">Sie können ein dnsZone-Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="67811-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="67811-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67811-152">OUTPUTS</span></span>

### <span data-ttu-id="67811-153">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="67811-154">Dieses Cmdlet gibt ein dnsZone-Objekt zurück, das die aktualisierte DNS-Zone mit einem neuen ETag darstellt.</span><span class="sxs-lookup"><span data-stu-id="67811-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="67811-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="67811-155">NOTES</span></span>
<span data-ttu-id="67811-156">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="67811-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="67811-157">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="67811-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="67811-158">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67811-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="67811-159">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="67811-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="67811-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67811-160">RELATED LINKS</span></span>

[<span data-ttu-id="67811-161">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-161">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="67811-162">Neu – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-162">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="67811-163">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="67811-163">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

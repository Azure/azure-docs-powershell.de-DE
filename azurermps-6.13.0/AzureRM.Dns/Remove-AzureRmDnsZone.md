---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499522"
---
# <span data-ttu-id="87fb3-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="87fb3-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="87fb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="87fb3-103">Entfernt eine DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87fb3-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87fb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87fb3-104">SYNTAX</span></span>

### <span data-ttu-id="87fb3-105">Felder</span><span class="sxs-lookup"><span data-stu-id="87fb3-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87fb3-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="87fb3-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87fb3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87fb3-107">DESCRIPTION</span></span>
<span data-ttu-id="87fb3-108">Das Cmdlet **Remove-AzureRmDnsZone** löscht endgültig eine DNS-Zone (Domain Name System) aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87fb3-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="87fb3-109">Alle in der Zone enthaltenen Daten Satz Sätze werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="87fb3-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="87fb3-110">Sie können ein **dnsZone** -Objekt mithilfe des *Name* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="87fb3-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="87fb3-111">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="87fb3-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="87fb3-112">Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="87fb3-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="87fb3-113">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="87fb3-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="87fb3-114">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="87fb3-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87fb3-115">EXAMPLES</span></span>

### <span data-ttu-id="87fb3-116">Beispiel 1: Entfernen einer Zone</span><span class="sxs-lookup"><span data-stu-id="87fb3-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="87fb3-117">Mit diesem Befehl wird die Zone mit dem Namen MyZone.com aus der Ressourcengruppe myresourcegroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="87fb3-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="87fb3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="87fb3-118">PARAMETERS</span></span>

### <span data-ttu-id="87fb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87fb3-119">-DefaultProfile</span></span>
<span data-ttu-id="87fb3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="87fb3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87fb3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87fb3-121">-Name</span></span>
<span data-ttu-id="87fb3-122">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="87fb3-123">Sie müssen auch den *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="87fb3-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="87fb3-124">Alternativ können Sie die DNS-Zone mithilfe des *Zone* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="87fb3-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87fb3-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="87fb3-125">-Overwrite</span></span>
<span data-ttu-id="87fb3-126">Wenn Sie die Zone mithilfe eines **dnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="87fb3-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="87fb3-127">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="87fb3-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="87fb3-128">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="87fb3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87fb3-129">-PassThru</span></span>
<span data-ttu-id="87fb3-130">passthru</span><span class="sxs-lookup"><span data-stu-id="87fb3-130">passthru</span></span>

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

### <span data-ttu-id="87fb3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87fb3-131">-ResourceGroupName</span></span>
<span data-ttu-id="87fb3-132">Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="87fb3-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="87fb3-133">Außerdem müssen Sie den Parameter *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="87fb3-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="87fb3-134">Alternativ können Sie die DNS-Zone mithilfe eines **dnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87fb3-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="87fb3-135">-Zone</span></span>
<span data-ttu-id="87fb3-136">Gibt die zu löschende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="87fb3-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="87fb3-137">Das übergebene **dnsZone** -Objekt kann auch über die Pipeline übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="87fb3-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="87fb3-138">Alternativ können Sie die zu löschende DNS-Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="87fb3-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="87fb3-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87fb3-139">-Confirm</span></span>
<span data-ttu-id="87fb3-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87fb3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87fb3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87fb3-141">-WhatIf</span></span>
<span data-ttu-id="87fb3-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87fb3-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87fb3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87fb3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fb3-144">CommonParameters</span></span>
<span data-ttu-id="87fb3-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87fb3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fb3-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87fb3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fb3-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87fb3-147">INPUTS</span></span>

### <span data-ttu-id="87fb3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="87fb3-148">System.String</span></span>

### <span data-ttu-id="87fb3-149">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="87fb3-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="87fb3-150">Parameter: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87fb3-150">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="87fb3-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87fb3-151">OUTPUTS</span></span>

### <span data-ttu-id="87fb3-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87fb3-152">System.Boolean</span></span>

## <span data-ttu-id="87fb3-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="87fb3-153">NOTES</span></span>
<span data-ttu-id="87fb3-154">Aufgrund der potenziell großen Auswirkung des Löschens einer DNS-Zone fordert dieses Cmdlet standardmäßig eine Bestätigung an, wenn die $ConfirmPreference Windows PowerShell-Variable einen anderen Wert als None aufweist.</span><span class="sxs-lookup"><span data-stu-id="87fb3-154">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="87fb3-155">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87fb3-155">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="87fb3-156">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="87fb3-156">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="87fb3-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87fb3-157">RELATED LINKS</span></span>

[<span data-ttu-id="87fb3-158">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="87fb3-158">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="87fb3-159">Neu – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="87fb3-159">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="87fb3-160">Satz-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="87fb3-160">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)

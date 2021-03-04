---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935016"
---
# <span data-ttu-id="3cc13-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc13-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="3cc13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc13-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc13-103">Entfernt eine DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cc13-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="3cc13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cc13-104">SYNTAX</span></span>

### <span data-ttu-id="3cc13-105">Felder</span><span class="sxs-lookup"><span data-stu-id="3cc13-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc13-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="3cc13-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc13-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cc13-107">DESCRIPTION</span></span>
<span data-ttu-id="3cc13-108">Das **Cmdlet Remove-AzDnsZone** löscht dauerhaft eine Zone des Domain Name System (DNS) aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cc13-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="3cc13-109">Alle Datensatzsätze, die in der Zone enthalten sind, werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3cc13-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="3cc13-110">Sie können ein **DnsZone-Objekt** mithilfe des Parameters *Name* oder mithilfe des Pipelineoperators übergeben oder alternativ die *Parameter ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="3cc13-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3cc13-111">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3cc13-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3cc13-112">Wenn Sie die Zone mithilfe eines **DnsZone-Objekts** angeben (über die Pipeline oder den Parameter Zone übergeben), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, seit das lokale **DnsZone-Objekt** abgerufen wurde (nur Vorgänge direkt auf der DNS-Zonenressourcenanzahl als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht). </span><span class="sxs-lookup"><span data-stu-id="3cc13-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="3cc13-113">Dies bietet Schutz für gleichzeitige Zonenänderungen.</span><span class="sxs-lookup"><span data-stu-id="3cc13-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="3cc13-114">Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="3cc13-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="3cc13-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3cc13-115">EXAMPLES</span></span>

### <span data-ttu-id="3cc13-116">Beispiel 1: Entfernen einer Zone</span><span class="sxs-lookup"><span data-stu-id="3cc13-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3cc13-117">Mit diesem Befehl wird die Zone myzone.com aus der Ressourcengruppe "MyResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3cc13-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3cc13-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3cc13-118">PARAMETERS</span></span>

### <span data-ttu-id="3cc13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc13-119">-DefaultProfile</span></span>
<span data-ttu-id="3cc13-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3cc13-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cc13-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3cc13-121">-Name</span></span>
<span data-ttu-id="3cc13-122">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3cc13-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="3cc13-123">Sie müssen auch den *Parameter ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="3cc13-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="3cc13-124">Alternativ können Sie die DNS-Zone mit dem Parameter *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="3cc13-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="3cc13-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3cc13-125">-Overwrite</span></span>
<span data-ttu-id="3cc13-126">Wenn Sie die Zone mithilfe eines **DnsZone-Objekts** angeben (über die Pipeline oder den Parameter Zone übergeben), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, seit das lokale **DnsZone-Objekt** abgerufen wurde (nur Vorgänge direkt auf der DNS-Zonenressourcenanzahl als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht). </span><span class="sxs-lookup"><span data-stu-id="3cc13-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="3cc13-127">Dies bietet Schutz für gleichzeitige Zonenänderungen.</span><span class="sxs-lookup"><span data-stu-id="3cc13-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="3cc13-128">Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="3cc13-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="3cc13-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc13-129">-PassThru</span></span>
<span data-ttu-id="3cc13-130">passthru</span><span class="sxs-lookup"><span data-stu-id="3cc13-130">passthru</span></span>

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

### <span data-ttu-id="3cc13-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc13-131">-ResourceGroupName</span></span>
<span data-ttu-id="3cc13-132">Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="3cc13-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="3cc13-133">Sie müssen auch den *Parameter ZoneName* angeben.</span><span class="sxs-lookup"><span data-stu-id="3cc13-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="3cc13-134">Alternativ können Sie die DNS-Zone mit einem **DnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *Zone übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="3cc13-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="3cc13-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="3cc13-135">-Zone</span></span>
<span data-ttu-id="3cc13-136">Gibt die zu löschende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="3cc13-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="3cc13-137">Das **übergebene DnsZone-Objekt** kann auch über die Pipeline übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cc13-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="3cc13-138">Alternativ können Sie die zu löschende DNS-Zone mithilfe der *Parameter ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="3cc13-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="3cc13-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cc13-139">-Confirm</span></span>
<span data-ttu-id="3cc13-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cc13-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc13-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc13-141">-WhatIf</span></span>
<span data-ttu-id="3cc13-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cc13-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc13-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cc13-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc13-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc13-144">CommonParameters</span></span>
<span data-ttu-id="3cc13-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc13-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc13-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc13-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc13-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3cc13-147">INPUTS</span></span>

### <span data-ttu-id="3cc13-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3cc13-148">System.String</span></span>

### <span data-ttu-id="3cc13-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc13-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="3cc13-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3cc13-150">OUTPUTS</span></span>

### <span data-ttu-id="3cc13-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cc13-151">System.Boolean</span></span>

## <span data-ttu-id="3cc13-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3cc13-152">NOTES</span></span>
<span data-ttu-id="3cc13-153">Aufgrund der potenziell hohen Auswirkungen des Löschens einer DNS-Zone wird dieses Cmdlet standardmäßig zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell einen anderen Wert als Keine hat.</span><span class="sxs-lookup"><span data-stu-id="3cc13-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="3cc13-154">Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cc13-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3cc13-155">Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3cc13-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="3cc13-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3cc13-156">RELATED LINKS</span></span>

[<span data-ttu-id="3cc13-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc13-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="3cc13-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc13-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="3cc13-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cc13-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)

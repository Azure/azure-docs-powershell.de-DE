---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842384"
---
# <span data-ttu-id="6b055-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="6b055-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b055-102">SYNOPSIS</span></span>
<span data-ttu-id="6b055-103">Aktualisiert einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="6b055-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="6b055-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b055-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b055-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b055-105">DESCRIPTION</span></span>
<span data-ttu-id="6b055-106">Das Cmdlet " **Satz-AzDnsRecordSet** " aktualisiert einen Daten Satz Satz im Azure DNS-Dienst von einem lokalen **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b055-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="6b055-107">Sie können ein **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="6b055-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="6b055-108">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6b055-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="6b055-109">Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6b055-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6b055-110">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b055-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6b055-111">Sie können dieses Verhalten mithilfe des *overwrite* -Parameters unterdrücken, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6b055-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="6b055-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b055-112">EXAMPLES</span></span>

### <span data-ttu-id="6b055-113">Beispiel 1: Aktualisieren eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="6b055-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="6b055-114">Der erste Befehl verwendet das Get-AzDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset.</span><span class="sxs-lookup"><span data-stu-id="6b055-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="6b055-115">Der zweite und der dritte Befehl sind Offlinevorgänge, um dem Daten Satz Satz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b055-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="6b055-116">Der endgültige Befehl verwendet das Cmdlet " **festlegen-AzDnsRecordSet** ", um das Update zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="6b055-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="6b055-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="6b055-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="6b055-118">Der erste Befehl verwendet das Cmdlet " **Get-AzDnsRecordset** ", um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der $Recordset-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6b055-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="6b055-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $Recordset.</span><span class="sxs-lookup"><span data-stu-id="6b055-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="6b055-120">Der endgültige Befehl verwendet das Cmdlet " **AzDnsRecordSet** ", um das Update in $Recordset weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b055-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="6b055-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b055-121">PARAMETERS</span></span>

### <span data-ttu-id="6b055-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6b055-122">-Overwrite</span></span>
<span data-ttu-id="6b055-123">Gibt an, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b055-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="6b055-124">Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6b055-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6b055-125">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b055-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6b055-126">Um dieses Verhalten zu unterdrücken, können Sie den Parameter *overwrite* verwenden, der dazu führt, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6b055-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6b055-127">-Recordset</span><span class="sxs-lookup"><span data-stu-id="6b055-127">-RecordSet</span></span>
<span data-ttu-id="6b055-128">Gibt das zu aktualisierende **Recordset** an.</span><span class="sxs-lookup"><span data-stu-id="6b055-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b055-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b055-129">-Confirm</span></span>
<span data-ttu-id="6b055-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b055-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b055-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b055-131">-WhatIf</span></span>
<span data-ttu-id="6b055-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b055-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b055-133">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b055-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b055-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b055-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b055-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b055-135">CommonParameters</span></span>
<span data-ttu-id="6b055-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b055-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b055-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b055-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b055-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b055-138">INPUTS</span></span>

### <span data-ttu-id="6b055-139">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6b055-140">Sie können ein **Recordset** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="6b055-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="6b055-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b055-141">OUTPUTS</span></span>

### <span data-ttu-id="6b055-142">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6b055-143">Dieses Cmdlet gibt ein Objekt zurück, das das aktualisierte **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b055-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="6b055-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b055-144">NOTES</span></span>
<span data-ttu-id="6b055-145">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6b055-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6b055-146">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="6b055-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6b055-147">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b055-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6b055-148">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6b055-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="6b055-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b055-149">RELATED LINKS</span></span>

[<span data-ttu-id="6b055-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="6b055-151">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="6b055-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6b055-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

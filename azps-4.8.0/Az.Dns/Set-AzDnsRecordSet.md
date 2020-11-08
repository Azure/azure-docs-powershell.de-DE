---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166951"
---
# <span data-ttu-id="e0be0-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="e0be0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0be0-102">SYNOPSIS</span></span>
<span data-ttu-id="e0be0-103">Aktualisiert einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="e0be0-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="e0be0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0be0-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0be0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0be0-105">DESCRIPTION</span></span>
<span data-ttu-id="e0be0-106">Das Cmdlet " **Satz-AzDnsRecordSet** " aktualisiert einen Daten Satz Satz im Azure DNS-Dienst von einem lokalen **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e0be0-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="e0be0-107">Sie können ein **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="e0be0-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="e0be0-108">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="e0be0-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e0be0-109">Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0be0-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="e0be0-110">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e0be0-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="e0be0-111">Sie können dieses Verhalten mithilfe des *overwrite* -Parameters unterdrücken, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e0be0-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="e0be0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0be0-112">EXAMPLES</span></span>

### <span data-ttu-id="e0be0-113">Beispiel 1: Aktualisieren eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="e0be0-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="e0be0-114">Der erste Befehl verwendet das Get-AzDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset.</span><span class="sxs-lookup"><span data-stu-id="e0be0-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="e0be0-115">Der zweite und der dritte Befehl sind Offlinevorgänge, um dem Daten Satz Satz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0be0-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="e0be0-116">Der endgültige Befehl verwendet das Cmdlet " **festlegen-AzDnsRecordSet** ", um das Update zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="e0be0-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="e0be0-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="e0be0-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="e0be0-118">Der erste Befehl verwendet das Cmdlet " **Get-AzDnsRecordset** ", um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der $Recordset-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e0be0-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="e0be0-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $Recordset.</span><span class="sxs-lookup"><span data-stu-id="e0be0-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="e0be0-120">Der endgültige Befehl verwendet das Cmdlet " **AzDnsRecordSet** ", um das Update in $Recordset weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0be0-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="e0be0-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0be0-121">PARAMETERS</span></span>

### <span data-ttu-id="e0be0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0be0-122">-DefaultProfile</span></span>
<span data-ttu-id="e0be0-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e0be0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0be0-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e0be0-124">-Overwrite</span></span>
<span data-ttu-id="e0be0-125">Gibt an, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0be0-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="e0be0-126">Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure DNS geändert wurde, seit das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e0be0-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="e0be0-127">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e0be0-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="e0be0-128">Um dieses Verhalten zu unterdrücken, können Sie den Parameter *overwrite* verwenden, der dazu führt, dass der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e0be0-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e0be0-129">-Recordset</span><span class="sxs-lookup"><span data-stu-id="e0be0-129">-RecordSet</span></span>
<span data-ttu-id="e0be0-130">Gibt das zu aktualisierende **Recordset** an.</span><span class="sxs-lookup"><span data-stu-id="e0be0-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0be0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0be0-131">-Confirm</span></span>
<span data-ttu-id="e0be0-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0be0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0be0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0be0-133">-WhatIf</span></span>
<span data-ttu-id="e0be0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0be0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0be0-135">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0be0-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0be0-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0be0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0be0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0be0-137">CommonParameters</span></span>
<span data-ttu-id="e0be0-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0be0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0be0-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0be0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0be0-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0be0-140">INPUTS</span></span>

### <span data-ttu-id="e0be0-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="e0be0-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0be0-142">OUTPUTS</span></span>

### <span data-ttu-id="e0be0-143">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="e0be0-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0be0-144">NOTES</span></span>
<span data-ttu-id="e0be0-145">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="e0be0-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e0be0-146">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="e0be0-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="e0be0-147">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0be0-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e0be0-148">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e0be0-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="e0be0-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0be0-149">RELATED LINKS</span></span>

[<span data-ttu-id="e0be0-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="e0be0-151">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="e0be0-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e0be0-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

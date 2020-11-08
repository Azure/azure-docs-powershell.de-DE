---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177675"
---
# <span data-ttu-id="19b98-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="19b98-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="19b98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19b98-102">SYNOPSIS</span></span>
<span data-ttu-id="19b98-103">Löscht einen Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="19b98-103">Deletes a record set.</span></span>

## <span data-ttu-id="19b98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19b98-104">SYNTAX</span></span>

### <span data-ttu-id="19b98-105">Felder</span><span class="sxs-lookup"><span data-stu-id="19b98-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b98-106">Gemischt</span><span class="sxs-lookup"><span data-stu-id="19b98-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b98-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="19b98-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b98-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19b98-108">DESCRIPTION</span></span>
<span data-ttu-id="19b98-109">Das Cmdlet **Remove-AzDnsRecordSet** löscht den angegebenen Daten Satz Satz aus der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="19b98-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="19b98-110">Sie können keine SOA-oder Nameserver (NS)-Einträge löschen, die automatisch in der Zone Apex erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="19b98-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="19b98-111">Sie können ein **Recordset** -Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="19b98-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="19b98-112">Um einen Daten Satz Satz nach Name und Typ ohne Verwendung eines **Recordset** -Objekts zu identifizieren, müssen Sie die Zone als **dnsZone** -Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter verwenden, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="19b98-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="19b98-113">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="19b98-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="19b98-114">Wenn Sie den Daten Satz Satz mit einem **Recordset** -Objekt angeben, wird der Daten Satz Satz nicht gelöscht, wenn er in Azure DNS geändert wurde, nachdem das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="19b98-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="19b98-115">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="19b98-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="19b98-116">Sie können dies unterdrücken, indem Sie den Parameter *overwrite* verwenden, der den Daten Satz Satz unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="19b98-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="19b98-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19b98-117">EXAMPLES</span></span>

### <span data-ttu-id="19b98-118">Beispiel 1: Entfernen eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="19b98-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="19b98-119">Der erste Befehl ruft den angegebenen Daten Satz Satz ab und speichert ihn dann in der $Recordset Variablen. Mit dem zweiten Befehl wird der Satz in $Recordset entfernt.</span><span class="sxs-lookup"><span data-stu-id="19b98-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="19b98-120">Beispiel 2: Entfernen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="19b98-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="19b98-121">Der erste Befehl ruft den angegebenen Daten Satz Satz ab.</span><span class="sxs-lookup"><span data-stu-id="19b98-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="19b98-122">Der zweite Befehl löscht die Datensatzgruppe, auch wenn Sie sich in der Zwischenzeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="19b98-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="19b98-123">Bestätigungsaufforderungen werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="19b98-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="19b98-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="19b98-124">PARAMETERS</span></span>

### <span data-ttu-id="19b98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b98-125">-DefaultProfile</span></span>
<span data-ttu-id="19b98-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="19b98-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19b98-127">-Name</span><span class="sxs-lookup"><span data-stu-id="19b98-127">-Name</span></span>
<span data-ttu-id="19b98-128">Gibt den Namen des zu entfernenden **Recordsets** an.</span><span class="sxs-lookup"><span data-stu-id="19b98-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="19b98-129">Wenn Sie den Daten Satz Satz nach Name angeben, muss die DNS-Zone entweder mithilfe des *Zone* -Parameters oder mit den Parametern *zonename* und *ResourceGroupName* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19b98-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="19b98-130">Alternativ kann der Daten Satz Satz mit einem **Recordset** -Objekt angegeben werden, das mit dem *Recordset* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="19b98-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b98-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="19b98-131">-Overwrite</span></span>
<span data-ttu-id="19b98-132">Wenn Sie den Daten Satz Satz mit einem **Recordset** -Objekt angeben, wird der Daten Satz Satz nicht gelöscht, wenn er in Azure DNS geändert wurde, nachdem das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="19b98-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="19b98-133">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="19b98-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="19b98-134">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="19b98-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="19b98-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19b98-135">-PassThru</span></span>
<span data-ttu-id="19b98-136">passthru</span><span class="sxs-lookup"><span data-stu-id="19b98-136">passthru</span></span>

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

### <span data-ttu-id="19b98-137">-Recordset</span><span class="sxs-lookup"><span data-stu-id="19b98-137">-RecordSet</span></span>
<span data-ttu-id="19b98-138">Gibt das zu entfernende **Recordset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="19b98-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="19b98-139">Alternativ kann der Daten Satz Satz mithilfe der Parameter *Name* und *Zone* oder mithilfe der Parameter *Name* , *zonename* und *ResourceGroupName* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19b98-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19b98-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="19b98-140">-RecordType</span></span>
<span data-ttu-id="19b98-141">Gibt den Typ des DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="19b98-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="19b98-142">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="19b98-142">Valid values are:</span></span>
- <span data-ttu-id="19b98-143">Eine</span><span class="sxs-lookup"><span data-stu-id="19b98-143">A</span></span>
- <span data-ttu-id="19b98-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="19b98-144">AAAA</span></span>
- <span data-ttu-id="19b98-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="19b98-145">CNAME</span></span>
- <span data-ttu-id="19b98-146">MX</span><span class="sxs-lookup"><span data-stu-id="19b98-146">MX</span></span>
- <span data-ttu-id="19b98-147">NS</span><span class="sxs-lookup"><span data-stu-id="19b98-147">NS</span></span>
- <span data-ttu-id="19b98-148">PTR</span><span class="sxs-lookup"><span data-stu-id="19b98-148">PTR</span></span>
- <span data-ttu-id="19b98-149">SRV</span><span class="sxs-lookup"><span data-stu-id="19b98-149">SRV</span></span>
- <span data-ttu-id="19b98-150">TXT-SOA-Einträge werden beim Löschen der Zone automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="19b98-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="19b98-151">Sie können SOA-Einträge nicht manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="19b98-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19b98-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b98-152">-ResourceGroupName</span></span>
<span data-ttu-id="19b98-153">Gibt die Ressourcengruppe an, die die DNS-Zone enthält, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="19b98-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="19b98-154">Dieser Parameter ist nur anwendbar, wenn der Daten Satz Satz und die DNS-Zone mithilfe der Parameter *Name* und *zonename* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19b98-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="19b98-155">Sie können den Daten Satz Satz auch mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* und *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="19b98-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="19b98-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="19b98-156">-Zone</span></span>
<span data-ttu-id="19b98-157">Gibt die DNS-Zone an, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="19b98-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="19b98-158">Dieser Parameter ist nur anwendbar, wenn der Daten Satz Satz mithilfe des *Name* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19b98-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="19b98-159">Sie können den Daten Satz Satz auch mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* , *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="19b98-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19b98-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="19b98-160">-ZoneName</span></span>
<span data-ttu-id="19b98-161">Gibt den Namen der Zone an, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="19b98-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="19b98-162">Sie müssen auch die Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="19b98-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="19b98-163">Alternativ können Sie den Daten Satz Satz entweder mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* und *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="19b98-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="19b98-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19b98-164">-Confirm</span></span>
<span data-ttu-id="19b98-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19b98-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b98-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b98-166">-WhatIf</span></span>
<span data-ttu-id="19b98-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19b98-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b98-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19b98-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b98-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b98-169">CommonParameters</span></span>
<span data-ttu-id="19b98-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b98-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b98-171">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b98-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b98-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19b98-172">INPUTS</span></span>

### <span data-ttu-id="19b98-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="19b98-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="19b98-174">System. String</span><span class="sxs-lookup"><span data-stu-id="19b98-174">System.String</span></span>

### <span data-ttu-id="19b98-175">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="19b98-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="19b98-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="19b98-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="19b98-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19b98-177">OUTPUTS</span></span>

### <span data-ttu-id="19b98-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19b98-178">System.Boolean</span></span>

## <span data-ttu-id="19b98-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="19b98-179">NOTES</span></span>
<span data-ttu-id="19b98-180">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="19b98-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="19b98-181">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="19b98-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="19b98-182">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19b98-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="19b98-183">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="19b98-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="19b98-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19b98-184">RELATED LINKS</span></span>

[<span data-ttu-id="19b98-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="19b98-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="19b98-186">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="19b98-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="19b98-187">Satz-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="19b98-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

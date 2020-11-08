---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995648"
---
# <span data-ttu-id="8ecb2-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ecb2-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="8ecb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ecb2-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecb2-103">Löscht einen Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-103">Deletes a record set.</span></span>

## <span data-ttu-id="8ecb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ecb2-104">SYNTAX</span></span>

### <span data-ttu-id="8ecb2-105">Felder</span><span class="sxs-lookup"><span data-stu-id="8ecb2-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb2-106">Gemischt</span><span class="sxs-lookup"><span data-stu-id="8ecb2-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecb2-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="8ecb2-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecb2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ecb2-108">DESCRIPTION</span></span>
<span data-ttu-id="8ecb2-109">Das Cmdlet **Remove-AzDnsRecordSet** löscht den angegebenen Daten Satz Satz aus der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="8ecb2-110">Sie können keine SOA-oder Nameserver (NS)-Einträge löschen, die automatisch in der Zone Apex erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="8ecb2-111">Sie können ein **Recordset** -Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="8ecb2-112">Um einen Daten Satz Satz nach Name und Typ ohne Verwendung eines **Recordset** -Objekts zu identifizieren, müssen Sie die Zone als **dnsZone** -Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter verwenden, oder Sie können auch die Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8ecb2-113">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8ecb2-114">Wenn Sie den Daten Satz Satz mit einem **Recordset** -Objekt angeben, wird der Daten Satz Satz nicht gelöscht, wenn er in Azure DNS geändert wurde, nachdem das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8ecb2-115">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8ecb2-116">Sie können dies unterdrücken, indem Sie den Parameter *overwrite* verwenden, der den Daten Satz Satz unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="8ecb2-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ecb2-117">EXAMPLES</span></span>

### <span data-ttu-id="8ecb2-118">Beispiel 1: Entfernen eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="8ecb2-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="8ecb2-119">Der erste Befehl ruft den angegebenen Daten Satz Satz ab und speichert ihn dann in der $Recordset Variablen. Mit dem zweiten Befehl wird der Satz in $Recordset entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="8ecb2-120">Beispiel 2: Entfernen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="8ecb2-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="8ecb2-121">Der erste Befehl ruft den angegebenen Daten Satz Satz ab.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="8ecb2-122">Der zweite Befehl löscht die Datensatzgruppe, auch wenn Sie sich in der Zwischenzeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="8ecb2-123">Bestätigungsaufforderungen werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="8ecb2-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ecb2-124">PARAMETERS</span></span>

### <span data-ttu-id="8ecb2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecb2-125">-DefaultProfile</span></span>
<span data-ttu-id="8ecb2-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8ecb2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ecb2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8ecb2-127">-Name</span></span>
<span data-ttu-id="8ecb2-128">Gibt den Namen des zu entfernenden **Recordsets** an.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="8ecb2-129">Wenn Sie den Daten Satz Satz nach Name angeben, muss die DNS-Zone entweder mithilfe des *Zone* -Parameters oder mit den Parametern *zonename* und *ResourceGroupName* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8ecb2-130">Alternativ kann der Daten Satz Satz mit einem **Recordset** -Objekt angegeben werden, das mit dem *Recordset* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="8ecb2-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8ecb2-131">-Overwrite</span></span>
<span data-ttu-id="8ecb2-132">Wenn Sie den Daten Satz Satz mit einem **Recordset** -Objekt angeben, wird der Daten Satz Satz nicht gelöscht, wenn er in Azure DNS geändert wurde, nachdem das lokale **Recordset** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="8ecb2-133">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="8ecb2-134">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="8ecb2-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ecb2-135">-PassThru</span></span>
<span data-ttu-id="8ecb2-136">passthru</span><span class="sxs-lookup"><span data-stu-id="8ecb2-136">passthru</span></span>

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

### <span data-ttu-id="8ecb2-137">-Recordset</span><span class="sxs-lookup"><span data-stu-id="8ecb2-137">-RecordSet</span></span>
<span data-ttu-id="8ecb2-138">Gibt das zu entfernende **Recordset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="8ecb2-139">Alternativ kann der Daten Satz Satz mithilfe der Parameter *Name* und *Zone* oder mithilfe der Parameter *Name* , *zonename* und *ResourceGroupName* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="8ecb2-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="8ecb2-140">-RecordType</span></span>
<span data-ttu-id="8ecb2-141">Gibt den Typ des DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="8ecb2-142">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8ecb2-142">Valid values are:</span></span>
- <span data-ttu-id="8ecb2-143">Eine</span><span class="sxs-lookup"><span data-stu-id="8ecb2-143">A</span></span>
- <span data-ttu-id="8ecb2-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="8ecb2-144">AAAA</span></span>
- <span data-ttu-id="8ecb2-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="8ecb2-145">CNAME</span></span>
- <span data-ttu-id="8ecb2-146">MX</span><span class="sxs-lookup"><span data-stu-id="8ecb2-146">MX</span></span>
- <span data-ttu-id="8ecb2-147">NS</span><span class="sxs-lookup"><span data-stu-id="8ecb2-147">NS</span></span>
- <span data-ttu-id="8ecb2-148">PTR</span><span class="sxs-lookup"><span data-stu-id="8ecb2-148">PTR</span></span>
- <span data-ttu-id="8ecb2-149">SRV</span><span class="sxs-lookup"><span data-stu-id="8ecb2-149">SRV</span></span>
- <span data-ttu-id="8ecb2-150">TXT-SOA-Einträge werden beim Löschen der Zone automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="8ecb2-151">Sie können SOA-Einträge nicht manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="8ecb2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecb2-152">-ResourceGroupName</span></span>
<span data-ttu-id="8ecb2-153">Gibt die Ressourcengruppe an, die die DNS-Zone enthält, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8ecb2-154">Dieser Parameter ist nur anwendbar, wenn der Daten Satz Satz und die DNS-Zone mithilfe der Parameter *Name* und *zonename* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="8ecb2-155">Sie können den Daten Satz Satz auch mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* und *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="8ecb2-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="8ecb2-156">-Zone</span></span>
<span data-ttu-id="8ecb2-157">Gibt die DNS-Zone an, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8ecb2-158">Dieser Parameter ist nur anwendbar, wenn der Daten Satz Satz mithilfe des *Name* -Parameters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="8ecb2-159">Sie können den Daten Satz Satz auch mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* , *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="8ecb2-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="8ecb2-160">-ZoneName</span></span>
<span data-ttu-id="8ecb2-161">Gibt den Namen der Zone an, die das zu löschende **Recordset** enthält.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="8ecb2-162">Sie müssen auch die Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8ecb2-163">Alternativ können Sie den Daten Satz Satz entweder mithilfe des *Recordset* -Parameters oder mit den Parametern *Name* und *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="8ecb2-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ecb2-164">-Confirm</span></span>
<span data-ttu-id="8ecb2-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ecb2-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecb2-166">-WhatIf</span></span>
<span data-ttu-id="8ecb2-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecb2-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ecb2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecb2-169">CommonParameters</span></span>
<span data-ttu-id="8ecb2-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecb2-171">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecb2-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecb2-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ecb2-172">INPUTS</span></span>

### <span data-ttu-id="8ecb2-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="8ecb2-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="8ecb2-174">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecb2-174">System.String</span></span>

### <span data-ttu-id="8ecb2-175">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="8ecb2-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="8ecb2-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ecb2-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="8ecb2-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ecb2-177">OUTPUTS</span></span>

### <span data-ttu-id="8ecb2-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ecb2-178">System.Boolean</span></span>

## <span data-ttu-id="8ecb2-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ecb2-179">NOTES</span></span>
<span data-ttu-id="8ecb2-180">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8ecb2-181">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="8ecb2-182">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8ecb2-183">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8ecb2-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8ecb2-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ecb2-184">RELATED LINKS</span></span>

[<span data-ttu-id="8ecb2-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ecb2-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="8ecb2-186">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ecb2-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8ecb2-187">Satz-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ecb2-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

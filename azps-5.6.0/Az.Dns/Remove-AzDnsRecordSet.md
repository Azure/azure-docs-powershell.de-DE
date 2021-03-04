---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935032"
---
# <span data-ttu-id="6e262-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="6e262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e262-102">SYNOPSIS</span></span>
<span data-ttu-id="6e262-103">Löscht einen Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="6e262-103">Deletes a record set.</span></span>

## <span data-ttu-id="6e262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e262-104">SYNTAX</span></span>

### <span data-ttu-id="6e262-105">Felder</span><span class="sxs-lookup"><span data-stu-id="6e262-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e262-106">Gemischt</span><span class="sxs-lookup"><span data-stu-id="6e262-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e262-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="6e262-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e262-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e262-108">DESCRIPTION</span></span>
<span data-ttu-id="6e262-109">Das **Cmdlet Remove-AzDnsRecordSet** löscht den angegebenen Datensatzsatz aus der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="6e262-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="6e262-110">Sie können keine SOA- oder Namenservereinträge löschen, die automatisch am Zonenapex erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="6e262-111">Sie können ein **RecordSet-Objekt** mithilfe des Pipelineoperators oder als Parameter an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="6e262-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="6e262-112">Um einen Datensatz nach Name und Typ zu identifizieren, ohne ein **RecordSet-Objekt** zu verwenden, müssen Sie die Zone als **DnsZone-Objekt** mithilfe des Pipelineoperators oder als Parameter an dieses Cmdlet übergeben, oder Alternativ können Sie die *Parameter ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="6e262-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6e262-113">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6e262-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6e262-114">Wenn Sie den Datensatzsatz mithilfe eines **RecordSet-Objekts** angeben, wird der Datensatzsatz nicht gelöscht, wenn er seit dem Abrufen des lokalen **RecordSet-Objekts** in Azure DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e262-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6e262-115">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="6e262-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6e262-116">Sie können dies unterdrücken, indem Sie den *Parameter Überschreiben* verwenden, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="6e262-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="6e262-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e262-117">EXAMPLES</span></span>

### <span data-ttu-id="6e262-118">Beispiel 1: Entfernen eines Datensatzsatzs</span><span class="sxs-lookup"><span data-stu-id="6e262-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="6e262-119">Der erste Befehl ruft den angegebenen Datensatzsatz ab und speichert ihn dann in der $RecordSet Variablen. Der zweite Befehl entfernt den datensatzsatz in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e262-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="6e262-120">Beispiel 2: Entfernen eines Datensatzsatzs und Unterdrücken aller Bestätigungen</span><span class="sxs-lookup"><span data-stu-id="6e262-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="6e262-121">Der erste Befehl ruft den angegebenen Datensatzsatz ab.</span><span class="sxs-lookup"><span data-stu-id="6e262-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="6e262-122">Mit dem zweiten Befehl wird der Datensatzsatz gelöscht, auch wenn er in der Zwischenzeit geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e262-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="6e262-123">Bestätigungsaufforderungen werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="6e262-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="6e262-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6e262-124">PARAMETERS</span></span>

### <span data-ttu-id="6e262-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e262-125">-DefaultProfile</span></span>
<span data-ttu-id="6e262-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6e262-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e262-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6e262-127">-Name</span></span>
<span data-ttu-id="6e262-128">Gibt den Namen des zu entfernenden **RecordSets** an.</span><span class="sxs-lookup"><span data-stu-id="6e262-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="6e262-129">Wenn Sie den NachNamen festgelegten Eintrag angeben, muss die DNS-Zone entweder mit dem Parameter *Zone* oder den *Parametern ZoneName* und *ResourceGroupName angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6e262-130">Alternativ kann der Datensatzsatz mit einem **RecordSet-Objekt** angegeben werden, das mit dem *Parameter RecordSet übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="6e262-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6e262-131">-Overwrite</span></span>
<span data-ttu-id="6e262-132">Wenn Sie den Datensatzsatz mithilfe eines **RecordSet-Objekts** angeben, wird der Datensatzsatz nicht gelöscht, wenn er seit dem Abrufen des lokalen **RecordSet-Objekts** in Azure DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e262-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="6e262-133">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="6e262-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="6e262-134">Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, wodurch der Datensatzsatz unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6e262-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e262-135">-PassThru</span></span>
<span data-ttu-id="6e262-136">passthru</span><span class="sxs-lookup"><span data-stu-id="6e262-136">passthru</span></span>

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

### <span data-ttu-id="6e262-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-137">-RecordSet</span></span>
<span data-ttu-id="6e262-138">Gibt das **zu entfernende RecordSet-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6e262-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="6e262-139">Alternativ kann der Datensatzsatz mithilfe der Parameter *Name* und *Zone* oder mit den Parametern *Name,* *ZoneName* und *ResourceGroupName angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6e262-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="6e262-140">-RecordType</span></span>
<span data-ttu-id="6e262-141">Gibt den Typ des DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="6e262-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="6e262-142">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6e262-142">Valid values are:</span></span>
- <span data-ttu-id="6e262-143">A</span><span class="sxs-lookup"><span data-stu-id="6e262-143">A</span></span>
- <span data-ttu-id="6e262-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="6e262-144">AAAA</span></span>
- <span data-ttu-id="6e262-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="6e262-145">CNAME</span></span>
- <span data-ttu-id="6e262-146">MX</span><span class="sxs-lookup"><span data-stu-id="6e262-146">MX</span></span>
- <span data-ttu-id="6e262-147">NS</span><span class="sxs-lookup"><span data-stu-id="6e262-147">NS</span></span>
- <span data-ttu-id="6e262-148">PTR</span><span class="sxs-lookup"><span data-stu-id="6e262-148">PTR</span></span>
- <span data-ttu-id="6e262-149">SRV</span><span class="sxs-lookup"><span data-stu-id="6e262-149">SRV</span></span>
- <span data-ttu-id="6e262-150">TXT-SOA-Einträge werden automatisch gelöscht, wenn die Zone gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="6e262-151">Sie können SOA-Datensätze nicht manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="6e262-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="6e262-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e262-152">-ResourceGroupName</span></span>
<span data-ttu-id="6e262-153">Gibt die Ressourcengruppe an, die die DNS-Zone enthält, die das **zu löschende RecordSet** enthält.</span><span class="sxs-lookup"><span data-stu-id="6e262-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6e262-154">Dieser Parameter gilt nur, wenn der Datensatzsatz und die DNS-Zone mit den *Parametern Name* und *ZoneName angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="6e262-155">Alternativ können Sie den Datensatzsatz entweder mit dem *Parameter RecordSet* oder den *Parametern Name* und *Zone* angeben.</span><span class="sxs-lookup"><span data-stu-id="6e262-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="6e262-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="6e262-156">-Zone</span></span>
<span data-ttu-id="6e262-157">Gibt die DNS-Zone an, die das **zu löschende RecordSet** enthält.</span><span class="sxs-lookup"><span data-stu-id="6e262-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6e262-158">Dieser Parameter gilt nur, wenn der Datensatzsatz mit dem Parameter *Name angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="6e262-159">Alternativ können Sie den Datensatzsatz entweder mit dem *Parameter RecordSet* oder den *Parametern Name,* *ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="6e262-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6e262-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="6e262-160">-ZoneName</span></span>
<span data-ttu-id="6e262-161">Gibt den Namen der Zone an, die das **zu löschende RecordSet** enthält.</span><span class="sxs-lookup"><span data-stu-id="6e262-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="6e262-162">Sie müssen auch die Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="6e262-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6e262-163">Alternativ kann der Datensatzsatz entweder mit dem *Parameter RecordSet* oder den *Parametern Name* und *Zone angegeben* werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="6e262-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e262-164">-Confirm</span></span>
<span data-ttu-id="6e262-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e262-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e262-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e262-166">-WhatIf</span></span>
<span data-ttu-id="6e262-167">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e262-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e262-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e262-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e262-169">CommonParameters</span></span>
<span data-ttu-id="6e262-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e262-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e262-171">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e262-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e262-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e262-172">INPUTS</span></span>

### <span data-ttu-id="6e262-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="6e262-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="6e262-174">System.String</span><span class="sxs-lookup"><span data-stu-id="6e262-174">System.String</span></span>

### <span data-ttu-id="6e262-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="6e262-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="6e262-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="6e262-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e262-177">OUTPUTS</span></span>

### <span data-ttu-id="6e262-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e262-178">System.Boolean</span></span>

## <span data-ttu-id="6e262-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6e262-179">NOTES</span></span>
<span data-ttu-id="6e262-180">Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="6e262-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6e262-181">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.</span><span class="sxs-lookup"><span data-stu-id="6e262-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="6e262-182">Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e262-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6e262-183">Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6e262-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e262-184">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6e262-184">RELATED LINKS</span></span>

[<span data-ttu-id="6e262-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="6e262-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="6e262-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e262-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

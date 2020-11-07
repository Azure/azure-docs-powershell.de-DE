---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844008"
---
# <span data-ttu-id="fc0ec-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fc0ec-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="fc0ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0ec-103">Entfernt einen DNS-Eintrag aus einem lokalen Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="fc0ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc0ec-104">SYNTAX</span></span>

### <span data-ttu-id="fc0ec-105">Eine</span><span class="sxs-lookup"><span data-stu-id="fc0ec-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="fc0ec-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-107">NS</span><span class="sxs-lookup"><span data-stu-id="fc0ec-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-108">MX</span><span class="sxs-lookup"><span data-stu-id="fc0ec-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-109">PTR</span><span class="sxs-lookup"><span data-stu-id="fc0ec-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-110">TXT</span><span class="sxs-lookup"><span data-stu-id="fc0ec-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-111">SRV</span><span class="sxs-lookup"><span data-stu-id="fc0ec-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="fc0ec-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="fc0ec-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="fc0ec-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc0ec-113">DESCRIPTION</span></span>
<span data-ttu-id="fc0ec-114">Mit dem Cmdlet **Remove-AzDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="fc0ec-115">Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="fc0ec-116">Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="fc0ec-117">Sie können keine SOA-Einträge hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="fc0ec-118">SOA-Einträge werden automatisch erstellt, wenn eine DNS-Zone erstellt und automatisch gelöscht wird, wenn die DNS-Zone gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="fc0ec-119">Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="fc0ec-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc0ec-120">EXAMPLES</span></span>

### <span data-ttu-id="fc0ec-121">Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-122">In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-123">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="fc0ec-124">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-125">Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-126">In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-127">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="fc0ec-128">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-129">Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-130">In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-131">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="fc0ec-132">Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-133">In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-134">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="fc0ec-135">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="fc0ec-136">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-137">Beispiel 5: Entfernen eines NS-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-138">In diesem Beispiel wird ein NS-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-139">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="fc0ec-140">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-141">Beispiel 6: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-142">In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-143">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="fc0ec-144">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-145">Beispiel 7: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-146">In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-147">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="fc0ec-148">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="fc0ec-149">Beispiel 8: Entfernen eines txt-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="fc0ec-150">In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="fc0ec-151">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="fc0ec-152">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="fc0ec-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc0ec-153">PARAMETERS</span></span>

### <span data-ttu-id="fc0ec-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="fc0ec-154">-Cname</span></span>
<span data-ttu-id="fc0ec-155">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="fc0ec-156">-Exchange</span></span>
<span data-ttu-id="fc0ec-157">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="fc0ec-158">-Ipv4Address</span></span>
<span data-ttu-id="fc0ec-159">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-159">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-160">-IPv6</span><span class="sxs-lookup"><span data-stu-id="fc0ec-160">-Ipv6Address</span></span>
<span data-ttu-id="fc0ec-161">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="fc0ec-162">-Nsdname</span></span>
<span data-ttu-id="fc0ec-163">Gibt den Namenserver für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-164">-Port</span><span class="sxs-lookup"><span data-stu-id="fc0ec-164">-Port</span></span>
<span data-ttu-id="fc0ec-165">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-166">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="fc0ec-166">-Preference</span></span>
<span data-ttu-id="fc0ec-167">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-168">-Priorität</span><span class="sxs-lookup"><span data-stu-id="fc0ec-168">-Priority</span></span>
<span data-ttu-id="fc0ec-169">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="fc0ec-170">-Ptrdname</span></span>
<span data-ttu-id="fc0ec-171">Gibt den Zieldomänen Namen eines Zeiger (PTR)-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-172">-Recordset</span><span class="sxs-lookup"><span data-stu-id="fc0ec-172">-RecordSet</span></span>
<span data-ttu-id="fc0ec-173">Gibt das **Recordset** -Objekt an, das den zu entfernenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="fc0ec-174">-Target</span><span class="sxs-lookup"><span data-stu-id="fc0ec-174">-Target</span></span>
<span data-ttu-id="fc0ec-175">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-176">-Wert</span><span class="sxs-lookup"><span data-stu-id="fc0ec-176">-Value</span></span>
<span data-ttu-id="fc0ec-177">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-178">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="fc0ec-178">-Weight</span></span>
<span data-ttu-id="fc0ec-179">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0ec-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0ec-180">CommonParameters</span></span>
<span data-ttu-id="fc0ec-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0ec-182">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0ec-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0ec-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc0ec-183">INPUTS</span></span>

### <span data-ttu-id="fc0ec-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fc0ec-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="fc0ec-185">Sie können ein **DnsRecordSet** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="fc0ec-186">Hierbei handelt es sich um eine Offlinedarstellung des Daten Satz Satzes, und es werden keine DNS-Antworten geändert, bis Sie den Satz-AzDnsRecordSet ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="fc0ec-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc0ec-187">OUTPUTS</span></span>

### <span data-ttu-id="fc0ec-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fc0ec-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="fc0ec-189">Dieses Cmdlet gibt das geänderte **Recordset** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="fc0ec-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="fc0ec-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc0ec-190">NOTES</span></span>

## <span data-ttu-id="fc0ec-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc0ec-191">RELATED LINKS</span></span>

[<span data-ttu-id="fc0ec-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fc0ec-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="fc0ec-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fc0ec-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="fc0ec-194">Satz-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fc0ec-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

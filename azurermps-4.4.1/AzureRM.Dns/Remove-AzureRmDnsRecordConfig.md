---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 97d87464f49d9f43d6ab6fb08d0cd8034560a108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501870"
---
# <span data-ttu-id="f3d6b-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f3d6b-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="f3d6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d6b-103">Entfernt einen DNS-Eintrag aus einem lokalen Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d6b-104">SYNTAX</span></span>

### <span data-ttu-id="f3d6b-105">Eine</span><span class="sxs-lookup"><span data-stu-id="f3d6b-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f3d6b-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-107">NS</span><span class="sxs-lookup"><span data-stu-id="f3d6b-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-108">MX</span><span class="sxs-lookup"><span data-stu-id="f3d6b-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-109">PTR</span><span class="sxs-lookup"><span data-stu-id="f3d6b-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-110">TXT</span><span class="sxs-lookup"><span data-stu-id="f3d6b-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="f3d6b-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d6b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="f3d6b-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d6b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3d6b-113">DESCRIPTION</span></span>
<span data-ttu-id="f3d6b-114">Mit dem Cmdlet **Remove-AzureRmDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="f3d6b-115">Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="f3d6b-116">Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="f3d6b-117">Sie können keine SOA-Einträge hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="f3d6b-118">SOA-Einträge werden automatisch erstellt, wenn eine DNS-Zone erstellt und automatisch gelöscht wird, wenn die DNS-Zone gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="f3d6b-119">Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f3d6b-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3d6b-120">EXAMPLES</span></span>

### <span data-ttu-id="f3d6b-121">Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-122">In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-123">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="f3d6b-124">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-125">Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-126">In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-127">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="f3d6b-128">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-129">Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-130">In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-131">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="f3d6b-132">Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-133">In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-134">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="f3d6b-135">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="f3d6b-136">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-137">Beispiel 5: Entfernen eines NS-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-138">In diesem Beispiel wird ein NS-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-139">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="f3d6b-140">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-141">Beispiel 6: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-142">In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-143">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="f3d6b-144">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-145">Beispiel 7: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-146">In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-147">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="f3d6b-148">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="f3d6b-149">Beispiel 8: Entfernen eines txt-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f3d6b-150">In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="f3d6b-151">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="f3d6b-152">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="f3d6b-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3d6b-153">PARAMETERS</span></span>

### <span data-ttu-id="f3d6b-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f3d6b-154">-Cname</span></span>
<span data-ttu-id="f3d6b-155">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f3d6b-156">-Exchange</span></span>
<span data-ttu-id="f3d6b-157">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f3d6b-158">-Ipv4Address</span></span>
<span data-ttu-id="f3d6b-159">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-159">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-160">-IPv6</span><span class="sxs-lookup"><span data-stu-id="f3d6b-160">-Ipv6Address</span></span>
<span data-ttu-id="f3d6b-161">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="f3d6b-162">-Nsdname</span></span>
<span data-ttu-id="f3d6b-163">Gibt den Namenserver für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-164">-Port</span><span class="sxs-lookup"><span data-stu-id="f3d6b-164">-Port</span></span>
<span data-ttu-id="f3d6b-165">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-166">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="f3d6b-166">-Preference</span></span>
<span data-ttu-id="f3d6b-167">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-168">-Priorität</span><span class="sxs-lookup"><span data-stu-id="f3d6b-168">-Priority</span></span>
<span data-ttu-id="f3d6b-169">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f3d6b-170">-Ptrdname</span></span>
<span data-ttu-id="f3d6b-171">Gibt den Zieldomänen Namen eines Zeiger (PTR)-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-172">-Recordset</span><span class="sxs-lookup"><span data-stu-id="f3d6b-172">-RecordSet</span></span>
<span data-ttu-id="f3d6b-173">Gibt das **Recordset** -Objekt an, das den zu entfernenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="f3d6b-174">-Target</span><span class="sxs-lookup"><span data-stu-id="f3d6b-174">-Target</span></span>
<span data-ttu-id="f3d6b-175">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-176">-Wert</span><span class="sxs-lookup"><span data-stu-id="f3d6b-176">-Value</span></span>
<span data-ttu-id="f3d6b-177">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-178">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="f3d6b-178">-Weight</span></span>
<span data-ttu-id="f3d6b-179">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d6b-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d6b-180">-DefaultProfile</span></span>
<span data-ttu-id="f3d6b-181">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-181">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d6b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d6b-182">CommonParameters</span></span>
<span data-ttu-id="f3d6b-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d6b-184">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d6b-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d6b-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3d6b-185">INPUTS</span></span>

### <span data-ttu-id="f3d6b-186">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3d6b-186">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f3d6b-187">Sie können ein **DnsRecordSet** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-187">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="f3d6b-188">Hierbei handelt es sich um eine Offlinedarstellung des Daten Satz Satzes, und es werden keine DNS-Antworten geändert, bis Sie den Satz-AzureRmDnsRecordSet ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-188">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="f3d6b-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3d6b-189">OUTPUTS</span></span>

### <span data-ttu-id="f3d6b-190">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3d6b-190">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f3d6b-191">Dieses Cmdlet gibt das geänderte **Recordset** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f3d6b-191">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="f3d6b-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3d6b-192">NOTES</span></span>

## <span data-ttu-id="f3d6b-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3d6b-193">RELATED LINKS</span></span>

[<span data-ttu-id="f3d6b-194">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f3d6b-194">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="f3d6b-195">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3d6b-195">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f3d6b-196">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3d6b-196">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

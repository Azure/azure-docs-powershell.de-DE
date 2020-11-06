---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f4521b50d338d18eaa3c811ee64c5cff20dcf54a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497494"
---
# <span data-ttu-id="573d6-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="573d6-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="573d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="573d6-102">SYNOPSIS</span></span>
<span data-ttu-id="573d6-103">Entfernt einen DNS-Eintrag aus einem lokalen Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="573d6-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="573d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="573d6-104">SYNTAX</span></span>

### <span data-ttu-id="573d6-105">Eine</span><span class="sxs-lookup"><span data-stu-id="573d6-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="573d6-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-107">NS</span><span class="sxs-lookup"><span data-stu-id="573d6-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-108">MX</span><span class="sxs-lookup"><span data-stu-id="573d6-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-109">PTR</span><span class="sxs-lookup"><span data-stu-id="573d6-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-110">TXT</span><span class="sxs-lookup"><span data-stu-id="573d6-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-111">SRV</span><span class="sxs-lookup"><span data-stu-id="573d6-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="573d6-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573d6-113">CAA</span><span class="sxs-lookup"><span data-stu-id="573d6-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="573d6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="573d6-114">DESCRIPTION</span></span>
<span data-ttu-id="573d6-115">Mit dem Cmdlet **Remove-AzureRmDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="573d6-116">Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="573d6-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="573d6-117">Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="573d6-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="573d6-118">Sie können keine SOA-Einträge hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="573d6-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="573d6-119">SOA-Einträge werden automatisch erstellt, wenn eine DNS-Zone erstellt und automatisch gelöscht wird, wenn die DNS-Zone gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="573d6-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="573d6-120">Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="573d6-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="573d6-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="573d6-121">EXAMPLES</span></span>

### <span data-ttu-id="573d6-122">Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-123">In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="573d6-124">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="573d6-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="573d6-125">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-126">Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-127">In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="573d6-128">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="573d6-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="573d6-129">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-130">Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-131">In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="573d6-132">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.</span><span class="sxs-lookup"><span data-stu-id="573d6-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="573d6-133">Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-134">In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="573d6-135">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="573d6-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="573d6-136">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="573d6-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="573d6-137">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-138">Beispiel 5: Entfernen eines NS-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-139">In diesem Beispiel wird ein NS-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="573d6-140">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="573d6-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="573d6-141">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-142">Beispiel 6: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-143">In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="573d6-144">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="573d6-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="573d6-145">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-146">Beispiel 7: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-147">In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="573d6-148">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="573d6-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="573d6-149">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="573d6-150">Beispiel 8: Entfernen eines txt-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="573d6-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="573d6-151">In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="573d6-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="573d6-152">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="573d6-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="573d6-153">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="573d6-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="573d6-154">Parameter</span><span class="sxs-lookup"><span data-stu-id="573d6-154">PARAMETERS</span></span>

### <span data-ttu-id="573d6-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="573d6-155">-CaaFlags</span></span>
<span data-ttu-id="573d6-156">Die Flags für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="573d6-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="573d6-157">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="573d6-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="573d6-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="573d6-158">-CaaTag</span></span>
<span data-ttu-id="573d6-159">Das Tag-Feld des hinzuzufügenden CAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="573d6-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="573d6-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="573d6-160">-CaaValue</span></span>
<span data-ttu-id="573d6-161">Das Feld "Wert" für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="573d6-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="573d6-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="573d6-162">-Cname</span></span>
<span data-ttu-id="573d6-163">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="573d6-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="573d6-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573d6-164">-DefaultProfile</span></span>
<span data-ttu-id="573d6-165">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="573d6-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="573d6-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="573d6-166">-Exchange</span></span>
<span data-ttu-id="573d6-167">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="573d6-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="573d6-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="573d6-168">-Ipv4Address</span></span>
<span data-ttu-id="573d6-169">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="573d6-170">-IPv6</span><span class="sxs-lookup"><span data-stu-id="573d6-170">-Ipv6Address</span></span>
<span data-ttu-id="573d6-171">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="573d6-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="573d6-172">-Nsdname</span></span>
<span data-ttu-id="573d6-173">Gibt den Namenserver für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="573d6-174">-Port</span><span class="sxs-lookup"><span data-stu-id="573d6-174">-Port</span></span>
<span data-ttu-id="573d6-175">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="573d6-176">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="573d6-176">-Preference</span></span>
<span data-ttu-id="573d6-177">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="573d6-178">-Priorität</span><span class="sxs-lookup"><span data-stu-id="573d6-178">-Priority</span></span>
<span data-ttu-id="573d6-179">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="573d6-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="573d6-180">-Ptrdname</span></span>
<span data-ttu-id="573d6-181">Gibt den Zieldomänen Namen eines Zeiger (PTR)-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="573d6-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="573d6-182">-Recordset</span><span class="sxs-lookup"><span data-stu-id="573d6-182">-RecordSet</span></span>
<span data-ttu-id="573d6-183">Gibt das **Recordset** -Objekt an, das den zu entfernenden Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="573d6-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="573d6-184">-Target</span><span class="sxs-lookup"><span data-stu-id="573d6-184">-Target</span></span>
<span data-ttu-id="573d6-185">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="573d6-186">-Wert</span><span class="sxs-lookup"><span data-stu-id="573d6-186">-Value</span></span>
<span data-ttu-id="573d6-187">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="573d6-188">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="573d6-188">-Weight</span></span>
<span data-ttu-id="573d6-189">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="573d6-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="573d6-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573d6-190">CommonParameters</span></span>
<span data-ttu-id="573d6-191">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573d6-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573d6-192">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573d6-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573d6-193">Eingaben</span><span class="sxs-lookup"><span data-stu-id="573d6-193">INPUTS</span></span>

### <span data-ttu-id="573d6-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573d6-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="573d6-195">Parameter: Recordset (ByValue)</span><span class="sxs-lookup"><span data-stu-id="573d6-195">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="573d6-196">System. String</span><span class="sxs-lookup"><span data-stu-id="573d6-196">System.String</span></span>

### <span data-ttu-id="573d6-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="573d6-197">System.UInt16</span></span>

### <span data-ttu-id="573d6-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="573d6-198">System.Byte</span></span>

## <span data-ttu-id="573d6-199">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="573d6-199">OUTPUTS</span></span>

### <span data-ttu-id="573d6-200">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573d6-200">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="573d6-201">Notizen</span><span class="sxs-lookup"><span data-stu-id="573d6-201">NOTES</span></span>

## <span data-ttu-id="573d6-202">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="573d6-202">RELATED LINKS</span></span>

[<span data-ttu-id="573d6-203">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="573d6-203">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="573d6-204">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573d6-204">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="573d6-205">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573d6-205">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2ba0cb03b4819c444f43a59f5556cf2ec8c17a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848859"
---
# <span data-ttu-id="96d8c-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="96d8c-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="96d8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="96d8c-103">Fügt einen DNS-Eintrag zu einem lokalen Datensatzobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="96d8c-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96d8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96d8c-104">SYNTAX</span></span>

### <span data-ttu-id="96d8c-105">Eine</span><span class="sxs-lookup"><span data-stu-id="96d8c-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="96d8c-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-107">NS</span><span class="sxs-lookup"><span data-stu-id="96d8c-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-108">MX</span><span class="sxs-lookup"><span data-stu-id="96d8c-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="96d8c-109">PTR</span><span class="sxs-lookup"><span data-stu-id="96d8c-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-110">TXT</span><span class="sxs-lookup"><span data-stu-id="96d8c-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-111">SRV</span><span class="sxs-lookup"><span data-stu-id="96d8c-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="96d8c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="96d8c-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="96d8c-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96d8c-113">DESCRIPTION</span></span>
<span data-ttu-id="96d8c-114">Mit dem Cmdlet **Add-AzureRmDnsRecordConfig** wird ein DNS-Eintrag (Domain Name System) zu einem **Recordset** -Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="96d8c-115">Das **Recordset** -Objekt ist ein Offlineobjekt, und Änderungen daran ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure-DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="96d8c-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="96d8c-116">Bei der Erstellung einer DNS-Zone werden SOA-Einträge erstellt, die beim Löschen der DNS-Zone entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="96d8c-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="96d8c-117">Sie können keine SOA-Einträge hinzufügen oder entfernen, aber Sie können Sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="96d8c-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="96d8c-118">Sie können das **Recordset** -Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="96d8c-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="96d8c-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96d8c-119">EXAMPLES</span></span>

### <span data-ttu-id="96d8c-120">Beispiel 1: Hinzufügen eines a-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-121">In diesem Beispiel wird ein A-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="96d8c-122">Beispiel 2: Hinzufügen eines AAAA-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-123">In diesem Beispiel wird ein AAAA-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="96d8c-124">Beispiel 3: Hinzufügen eines CNAME-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-125">In diesem Beispiel wird ein CNAME-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="96d8c-126">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, muss er zunächst ein leerer Daten Satz Satz sein, oder vorhandene Datensätze müssen mithilfe von Remove-AzureRmDnsRecordConfig entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="96d8c-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="96d8c-127">Beispiel 4: Hinzufügen eines MX-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-128">In diesem Beispiel wird ein MX-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="96d8c-129">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="96d8c-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="96d8c-130">Beispiel 5: Hinzufügen eines NS-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-131">In diesem Beispiel wird ein NS-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="96d8c-132">Beispiel 6: Hinzufügen eines PTR-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-133">In diesem Beispiel wird ein PTR-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="96d8c-134">Beispiel 7: Hinzufügen eines SRV-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-135">In diesem Beispiel wird ein SRV-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="96d8c-136">Beispiel 8: Hinzufügen eines txt-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="96d8c-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="96d8c-137">In diesem Beispiel wird ein TXT-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96d8c-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="96d8c-138">Parameter</span><span class="sxs-lookup"><span data-stu-id="96d8c-138">PARAMETERS</span></span>

### <span data-ttu-id="96d8c-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="96d8c-139">-Cname</span></span>
<span data-ttu-id="96d8c-140">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="96d8c-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="96d8c-141">-Exchange</span></span>
<span data-ttu-id="96d8c-142">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="96d8c-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="96d8c-143">-Ipv4Address</span></span>
<span data-ttu-id="96d8c-144">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="96d8c-145">-IPv6</span><span class="sxs-lookup"><span data-stu-id="96d8c-145">-Ipv6Address</span></span>
<span data-ttu-id="96d8c-146">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="96d8c-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="96d8c-147">-Nsdname</span></span>
<span data-ttu-id="96d8c-148">Gibt den Namenserver Namen für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="96d8c-149">-Port</span><span class="sxs-lookup"><span data-stu-id="96d8c-149">-Port</span></span>
<span data-ttu-id="96d8c-150">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="96d8c-151">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="96d8c-151">-Preference</span></span>
<span data-ttu-id="96d8c-152">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="96d8c-153">-Priorität</span><span class="sxs-lookup"><span data-stu-id="96d8c-153">-Priority</span></span>
<span data-ttu-id="96d8c-154">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="96d8c-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="96d8c-155">-Ptrdname</span></span>
<span data-ttu-id="96d8c-156">Gibt den Zieldomänen Namen eines PTR-Eintrags (Pointer Resource) an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="96d8c-157">-Recordset</span><span class="sxs-lookup"><span data-stu-id="96d8c-157">-RecordSet</span></span>
<span data-ttu-id="96d8c-158">Gibt das **Recordset** -Objekt an, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96d8c-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="96d8c-159">-Target</span><span class="sxs-lookup"><span data-stu-id="96d8c-159">-Target</span></span>
<span data-ttu-id="96d8c-160">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="96d8c-161">-Wert</span><span class="sxs-lookup"><span data-stu-id="96d8c-161">-Value</span></span>
<span data-ttu-id="96d8c-162">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="96d8c-163">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="96d8c-163">-Weight</span></span>
<span data-ttu-id="96d8c-164">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="96d8c-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="96d8c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d8c-165">CommonParameters</span></span>
<span data-ttu-id="96d8c-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d8c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d8c-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d8c-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d8c-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96d8c-168">INPUTS</span></span>

### <span data-ttu-id="96d8c-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="96d8c-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="96d8c-170">Sie können ein **Recordset** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="96d8c-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="96d8c-171">Hierbei handelt es sich um eine Offlinedarstellung des **Recordsets** , und Änderungen an ihm ändern die DNS-Antworten erst, nachdem Sie das Set-AzureRmDnsRecordSet-Cmdlet ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="96d8c-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="96d8c-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96d8c-172">OUTPUTS</span></span>

### <span data-ttu-id="96d8c-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="96d8c-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="96d8c-174">Dieses Cmdlet gibt das geänderte **Recordset** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="96d8c-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="96d8c-175">Darüber hinaus wird das übergebene Objekt direkt geändert.</span><span class="sxs-lookup"><span data-stu-id="96d8c-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="96d8c-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="96d8c-176">NOTES</span></span>

## <span data-ttu-id="96d8c-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96d8c-177">RELATED LINKS</span></span>

[<span data-ttu-id="96d8c-178">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="96d8c-178">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="96d8c-179">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="96d8c-179">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="96d8c-180">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="96d8c-180">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 0327837f6e28d7147892669bd77b1aa78747a5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844007"
---
# <span data-ttu-id="a2fe6-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a2fe6-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="a2fe6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fe6-103">Erstellt einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="a2fe6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2fe6-104">SYNTAX</span></span>

### <span data-ttu-id="a2fe6-105">Felder</span><span class="sxs-lookup"><span data-stu-id="a2fe6-105">Fields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2fe6-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="a2fe6-106">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2fe6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2fe6-107">DESCRIPTION</span></span>
<span data-ttu-id="a2fe6-108">Das Cmdlet **New-AzDnsRecordSet** erstellt einen neuen DNS-Eintrag (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-108">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="a2fe6-109">Ein **Recordset** -Objekt ist ein Satz von DNS-Einträgen mit dem gleichen Namen und Typ.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="a2fe6-110">Beachten Sie, dass der Name relativ zur Zone und nicht zum vollqualifizierten Namen gehört.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="a2fe6-111">Der *DnsRecords* -Parameter gibt die Datensätze in der Datensatzgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="a2fe6-112">Dieser Parameter akzeptiert ein Array von DNS-Einträgen, die mithilfe von New-AzDnsRecordConfig erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-112">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>

<span data-ttu-id="a2fe6-113">Sie können den Pipelineoperator verwenden, um ein **dnsZone** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **dnsZone** -Objekt als *Zone* -Parameter übergeben, oder Sie können die Zone auch nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="a2fe6-114">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="a2fe6-115">Wenn bereits ein übereinstimmendes **Recordset** vorhanden ist (gleicher Name und Datensatztyp), müssen Sie den Parameter *overwrite* angeben, andernfalls wird vom Cmdlet kein neues **Recordset** -Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="a2fe6-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2fe6-116">EXAMPLES</span></span>

### <span data-ttu-id="a2fe6-117">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="a2fe6-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-118">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-119">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-120">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="a2fe6-121">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="a2fe6-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-122">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-123">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-124">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-124">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-125">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-126">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="a2fe6-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-127">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-128">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-129">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-129">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-130">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-131">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="a2fe6-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-132">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-133">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-134">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-134">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-135">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-136">Beispiel 5: Erstellen eines Recordsets des Typs NS</span><span class="sxs-lookup"><span data-stu-id="a2fe6-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-137">Dieser Befehl erstellt ein **Recordset** mit dem Namen ns1 in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-138">Der Daten Satz Satz ist vom Typ NS und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-139">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-139">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-140">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-141">Beispiel 6: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="a2fe6-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-142">Mit diesem Befehl wird ein **Recordset** mit dem Namen 4 in der Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="a2fe6-143">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-144">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-144">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-145">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-146">Beispiel 7: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="a2fe6-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-147">Dieser Befehl erstellt ein **Recordset** mit dem Namen "_sip. _tcp" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-148">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-149">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="a2fe6-150">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="a2fe6-151">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-152">Beispiel 8: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="a2fe6-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-153">Dieser Befehl erstellt ein **Recordset** mit dem Namen "Text" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-154">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-155">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-155">It contains a single DNS record.</span></span>

<span data-ttu-id="a2fe6-156">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-157">Beispiel 9: Erstellen eines Recordsets am Scheitelbereich der Zone</span><span class="sxs-lookup"><span data-stu-id="a2fe6-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-158">Mit diesem Befehl wird ein **Recordset** am Scheitel (oder Stamm) der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-159">Dazu wird der Name des Daten Satz Satzes als "@" (einschließlich der doppelten Anführungszeichen) angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="a2fe6-160">Sie können keine CNAME-Einträge am Scheitel einer Zone erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="a2fe6-161">Hierbei handelt es sich um eine Einschränkung der DNS-Standards; Es handelt sich nicht um eine Einschränkung von Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="a2fe6-162">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-163">Beispiel 10: Erstellen eines Platzhaltersatz-Datensatzes</span><span class="sxs-lookup"><span data-stu-id="a2fe6-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="a2fe6-164">Dieser Befehl erstellt ein **Recordset** mit dem Namen \* in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-165">Hierbei handelt es sich um einen Platzhaltersatz.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-165">This is a wildcard record set.</span></span>

<span data-ttu-id="a2fe6-166">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a2fe6-167">Beispiel 11: Erstellen eines leeren Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="a2fe6-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="a2fe6-168">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="a2fe6-169">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="a2fe6-170">Hierbei handelt es sich um einen leeren Daten Satz Satz, der als Platzhalter fungiert, auf den Sie später Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="a2fe6-171">Beispiel 12: Erstellen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="a2fe6-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="a2fe6-172">Mit diesem Befehl wird ein **Recordset** erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="a2fe6-173">Der Parameter *overwrite* stellt sicher, dass dieser Daten Satz Satz alle bereits vorhandenen Daten Satz Sätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatz gehen verloren).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="a2fe6-174">Der *Confirm* -Parameter mit dem Wert $false unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="a2fe6-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2fe6-175">PARAMETERS</span></span>

### <span data-ttu-id="a2fe6-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="a2fe6-176">-DnsRecords</span></span>
<span data-ttu-id="a2fe6-177">Gibt das Array von DNS-Einträgen an, die in den Daten Satz Satz einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="a2fe6-178">Sie können das New-AzDnsRecordConfig-Cmdlet verwenden, um DNS-Eintrags Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-178">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="a2fe6-179">Weitere Informationen finden Sie in den Beispielen.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-180">-Force</span><span class="sxs-lookup"><span data-stu-id="a2fe6-180">-Force</span></span>
<span data-ttu-id="a2fe6-181">Dieser Parameter ist für dieses Cmdlet veraltet.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="a2fe6-182">Sie wird in einer zukünftigen Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-182">It will be removed in a future release.</span></span>

<span data-ttu-id="a2fe6-183">Verwenden Sie den Parameter *Confirm* , um zu steuern, ob das Cmdlet Sie zur Eingabe von Comfirmation auffordert.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="a2fe6-184">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="a2fe6-184">-Metadata</span></span>
<span data-ttu-id="a2fe6-185">Gibt ein Array von Metadaten an, das dem Recordset zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="a2fe6-186">Metadaten werden mithilfe von Name-Wert-Paaren angegeben, die als Hashtabellen dargestellt werden, beispielsweise @ (@ {"Name" = "Dept"; "Wert" = "Einkaufen"}, @ {"Name" = "env"; "Wert" = "Production"}).</span><span class="sxs-lookup"><span data-stu-id="a2fe6-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-187">-Name</span><span class="sxs-lookup"><span data-stu-id="a2fe6-187">-Name</span></span>
<span data-ttu-id="a2fe6-188">Gibt den Namen des **Recordsets** an, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a2fe6-189">-Overwrite</span></span>
<span data-ttu-id="a2fe6-190">Gibt an, dass dieses Cmdlet das angegebene **Recordset** überschreibt, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="a2fe6-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a2fe6-191">-RecordType</span></span>
<span data-ttu-id="a2fe6-192">Gibt den Typ des zu erstellenden DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="a2fe6-193">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a2fe6-193">Valid values are:</span></span>

- <span data-ttu-id="a2fe6-194">Eine</span><span class="sxs-lookup"><span data-stu-id="a2fe6-194">A</span></span>
- <span data-ttu-id="a2fe6-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="a2fe6-195">AAAA</span></span>
- <span data-ttu-id="a2fe6-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="a2fe6-196">CNAME</span></span>
- <span data-ttu-id="a2fe6-197">MX</span><span class="sxs-lookup"><span data-stu-id="a2fe6-197">MX</span></span>
- <span data-ttu-id="a2fe6-198">NS</span><span class="sxs-lookup"><span data-stu-id="a2fe6-198">NS</span></span>
- <span data-ttu-id="a2fe6-199">PTR</span><span class="sxs-lookup"><span data-stu-id="a2fe6-199">PTR</span></span>
- <span data-ttu-id="a2fe6-200">SRV</span><span class="sxs-lookup"><span data-stu-id="a2fe6-200">SRV</span></span>
- <span data-ttu-id="a2fe6-201">TXT</span><span class="sxs-lookup"><span data-stu-id="a2fe6-201">TXT</span></span>

<span data-ttu-id="a2fe6-202">SOA-Einträge werden beim Erstellen der Zone automatisch erstellt und können nicht manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fe6-203">-ResourceGroupName</span></span>
<span data-ttu-id="a2fe6-204">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a2fe6-205">Sie müssen auch den Parameter *zonename* angeben, um den Zonennamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="a2fe6-206">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="a2fe6-207">-Ttl</span></span>
<span data-ttu-id="a2fe6-208">Gibt die Gültigkeitsdauer (Time to Live, TTL) für das DNS-Recordset an.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="a2fe6-209">-Zone</span></span>
<span data-ttu-id="a2fe6-210">Gibt den dnsZone an, in dem das **Recordset** erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="a2fe6-211">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-212">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="a2fe6-212">-ZoneName</span></span>
<span data-ttu-id="a2fe6-213">Gibt den Namen der Zone an, in der das **Recordset** erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="a2fe6-214">Sie müssen auch die Ressourcengruppe, die die Zone enthält, mithilfe des *ResourceGroupName* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="a2fe6-215">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2fe6-216">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2fe6-216">-Confirm</span></span>
<span data-ttu-id="a2fe6-217">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2fe6-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fe6-218">-WhatIf</span></span>
<span data-ttu-id="a2fe6-219">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2fe6-220">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2fe6-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fe6-221">CommonParameters</span></span>
<span data-ttu-id="a2fe6-222">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fe6-223">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2fe6-223">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fe6-224">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2fe6-224">INPUTS</span></span>

### <span data-ttu-id="a2fe6-225">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="a2fe6-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a2fe6-226">Sie können ein dnsZone-Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="a2fe6-227">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2fe6-227">OUTPUTS</span></span>

### <span data-ttu-id="a2fe6-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a2fe6-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a2fe6-229">Dieses Cmdlet gibt ein **Recordset** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="a2fe6-230">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2fe6-230">NOTES</span></span>
<span data-ttu-id="a2fe6-231">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a2fe6-232">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="a2fe6-233">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a2fe6-234">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a2fe6-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a2fe6-235">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2fe6-235">RELATED LINKS</span></span>

[<span data-ttu-id="a2fe6-236">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a2fe6-236">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="a2fe6-237">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a2fe6-237">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="a2fe6-238">Neu – AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a2fe6-238">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="a2fe6-239">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a2fe6-239">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="a2fe6-240">Satz-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a2fe6-240">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

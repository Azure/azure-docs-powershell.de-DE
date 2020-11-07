---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848852"
---
# <span data-ttu-id="5f1d8-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5f1d8-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="5f1d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1d8-103">Erstellt einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f1d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f1d8-104">SYNTAX</span></span>

### <span data-ttu-id="5f1d8-105">Felder</span><span class="sxs-lookup"><span data-stu-id="5f1d8-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f1d8-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="5f1d8-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f1d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f1d8-107">DESCRIPTION</span></span>
<span data-ttu-id="5f1d8-108">Das Cmdlet **New-AzureRmDnsRecordSet** erstellt einen neuen DNS-Eintrag (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="5f1d8-109">Ein **Recordset** -Objekt ist ein Satz von DNS-Einträgen mit dem gleichen Namen und Typ.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="5f1d8-110">Beachten Sie, dass der Name relativ zur Zone und nicht zum vollqualifizierten Namen gehört.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="5f1d8-111">Der *DnsRecords* -Parameter gibt die Datensätze in der Datensatzgruppe an.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="5f1d8-112">Dieser Parameter akzeptiert ein Array von DNS-Einträgen, die mithilfe von New-AzureRmDnsRecordConfig erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="5f1d8-113">Sie können den Pipelineoperator verwenden, um ein **dnsZone** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **dnsZone** -Objekt als *Zone* -Parameter übergeben, oder Sie können die Zone auch nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="5f1d8-114">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="5f1d8-115">Wenn bereits ein übereinstimmendes **Recordset** vorhanden ist (gleicher Name und Datensatztyp), müssen Sie den Parameter *overwrite* angeben, andernfalls wird vom Cmdlet kein neues **Recordset** -Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="5f1d8-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f1d8-116">EXAMPLES</span></span>

### <span data-ttu-id="5f1d8-117">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="5f1d8-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-118">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-119">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-120">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="5f1d8-121">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="5f1d8-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-122">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-123">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-124">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-124">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-125">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-126">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="5f1d8-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-127">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-128">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-129">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-129">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-130">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-131">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="5f1d8-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-132">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-133">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-134">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-134">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-135">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-136">Beispiel 5: Erstellen eines Recordsets des Typs NS</span><span class="sxs-lookup"><span data-stu-id="5f1d8-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-137">Dieser Befehl erstellt ein **Recordset** mit dem Namen ns1 in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-138">Der Daten Satz Satz ist vom Typ NS und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-139">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-139">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-140">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-141">Beispiel 6: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="5f1d8-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-142">Mit diesem Befehl wird ein **Recordset** mit dem Namen 4 in der Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="5f1d8-143">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-144">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-144">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-145">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-146">Beispiel 7: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="5f1d8-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-147">Dieser Befehl erstellt ein **Recordset** mit dem Namen "_sip. _tcp" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-148">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-149">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="5f1d8-150">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="5f1d8-151">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-152">Beispiel 8: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="5f1d8-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-153">Dieser Befehl erstellt ein **Recordset** mit dem Namen "Text" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-154">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-155">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-155">It contains a single DNS record.</span></span>

<span data-ttu-id="5f1d8-156">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-157">Beispiel 9: Erstellen eines Recordsets am Scheitelbereich der Zone</span><span class="sxs-lookup"><span data-stu-id="5f1d8-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-158">Mit diesem Befehl wird ein **Recordset** am Scheitel (oder Stamm) der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-159">Dazu wird der Name des Daten Satz Satzes als "@" (einschließlich der doppelten Anführungszeichen) angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="5f1d8-160">Sie können keine CNAME-Einträge am Scheitel einer Zone erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="5f1d8-161">Hierbei handelt es sich um eine Einschränkung der DNS-Standards; Es handelt sich nicht um eine Einschränkung von Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="5f1d8-162">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-163">Beispiel 10: Erstellen eines Platzhaltersatz-Datensatzes</span><span class="sxs-lookup"><span data-stu-id="5f1d8-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="5f1d8-164">Dieser Befehl erstellt ein **Recordset** mit dem Namen \* in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-165">Hierbei handelt es sich um einen Platzhaltersatz.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-165">This is a wildcard record set.</span></span>

<span data-ttu-id="5f1d8-166">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5f1d8-167">Beispiel 11: Erstellen eines leeren Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="5f1d8-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="5f1d8-168">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="5f1d8-169">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="5f1d8-170">Hierbei handelt es sich um einen leeren Daten Satz Satz, der als Platzhalter fungiert, auf den Sie später Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="5f1d8-171">Beispiel 12: Erstellen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="5f1d8-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="5f1d8-172">Mit diesem Befehl wird ein **Recordset** erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="5f1d8-173">Der Parameter *overwrite* stellt sicher, dass dieser Daten Satz Satz alle bereits vorhandenen Daten Satz Sätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatz gehen verloren).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="5f1d8-174">Der *Confirm* -Parameter mit dem Wert $false unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="5f1d8-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f1d8-175">PARAMETERS</span></span>

### <span data-ttu-id="5f1d8-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="5f1d8-176">-DnsRecords</span></span>
<span data-ttu-id="5f1d8-177">Gibt das Array von DNS-Einträgen an, die in den Daten Satz Satz einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="5f1d8-178">Sie können das New-AzureRmDnsRecordConfig-Cmdlet verwenden, um DNS-Eintrags Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="5f1d8-179">Weitere Informationen finden Sie in den Beispielen.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-179">See the examples for more information.</span></span>

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

### <span data-ttu-id="5f1d8-180">-Force</span><span class="sxs-lookup"><span data-stu-id="5f1d8-180">-Force</span></span>
<span data-ttu-id="5f1d8-181">Dieser Parameter ist für dieses Cmdlet veraltet.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="5f1d8-182">Sie wird in einer zukünftigen Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-182">It will be removed in a future release.</span></span>

<span data-ttu-id="5f1d8-183">Verwenden Sie den Parameter *Confirm* , um zu steuern, ob das Cmdlet Sie zur Eingabe von Comfirmation auffordert.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="5f1d8-184">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="5f1d8-184">-Metadata</span></span>
<span data-ttu-id="5f1d8-185">Gibt ein Array von Metadaten an, das dem Recordset zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="5f1d8-186">Metadaten werden mithilfe von Name-Wert-Paaren angegeben, die als Hashtabellen dargestellt werden, beispielsweise @ (@ {"Name" = "Dept"; "Wert" = "Einkaufen"}, @ {"Name" = "env"; "Wert" = "Production"}).</span><span class="sxs-lookup"><span data-stu-id="5f1d8-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="5f1d8-187">-Name</span><span class="sxs-lookup"><span data-stu-id="5f1d8-187">-Name</span></span>
<span data-ttu-id="5f1d8-188">Gibt den Namen des **Recordsets** an, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="5f1d8-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5f1d8-189">-Overwrite</span></span>
<span data-ttu-id="5f1d8-190">Gibt an, dass dieses Cmdlet das angegebene **Recordset** überschreibt, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="5f1d8-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="5f1d8-191">-RecordType</span></span>
<span data-ttu-id="5f1d8-192">Gibt den Typ des zu erstellenden DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="5f1d8-193">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5f1d8-193">Valid values are:</span></span>

- <span data-ttu-id="5f1d8-194">Eine</span><span class="sxs-lookup"><span data-stu-id="5f1d8-194">A</span></span>
- <span data-ttu-id="5f1d8-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="5f1d8-195">AAAA</span></span>
- <span data-ttu-id="5f1d8-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="5f1d8-196">CNAME</span></span>
- <span data-ttu-id="5f1d8-197">MX</span><span class="sxs-lookup"><span data-stu-id="5f1d8-197">MX</span></span>
- <span data-ttu-id="5f1d8-198">NS</span><span class="sxs-lookup"><span data-stu-id="5f1d8-198">NS</span></span>
- <span data-ttu-id="5f1d8-199">PTR</span><span class="sxs-lookup"><span data-stu-id="5f1d8-199">PTR</span></span>
- <span data-ttu-id="5f1d8-200">SRV</span><span class="sxs-lookup"><span data-stu-id="5f1d8-200">SRV</span></span>
- <span data-ttu-id="5f1d8-201">TXT</span><span class="sxs-lookup"><span data-stu-id="5f1d8-201">TXT</span></span>

<span data-ttu-id="5f1d8-202">SOA-Einträge werden beim Erstellen der Zone automatisch erstellt und können nicht manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="5f1d8-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1d8-203">-ResourceGroupName</span></span>
<span data-ttu-id="5f1d8-204">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="5f1d8-205">Sie müssen auch den Parameter *zonename* angeben, um den Zonennamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="5f1d8-206">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5f1d8-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="5f1d8-207">-Ttl</span></span>
<span data-ttu-id="5f1d8-208">Gibt die Gültigkeitsdauer (Time to Live, TTL) für das DNS-Recordset an.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="5f1d8-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="5f1d8-209">-Zone</span></span>
<span data-ttu-id="5f1d8-210">Gibt den dnsZone an, in dem das **Recordset** erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="5f1d8-211">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="5f1d8-212">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5f1d8-212">-ZoneName</span></span>
<span data-ttu-id="5f1d8-213">Gibt den Namen der Zone an, in der das **Recordset** erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="5f1d8-214">Sie müssen auch die Ressourcengruppe, die die Zone enthält, mithilfe des *ResourceGroupName* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="5f1d8-215">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5f1d8-216">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f1d8-216">-Confirm</span></span>
<span data-ttu-id="5f1d8-217">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f1d8-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1d8-218">-WhatIf</span></span>
<span data-ttu-id="5f1d8-219">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f1d8-220">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f1d8-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1d8-221">CommonParameters</span></span>
<span data-ttu-id="5f1d8-222">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1d8-223">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f1d8-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1d8-224">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f1d8-224">INPUTS</span></span>

### <span data-ttu-id="5f1d8-225">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="5f1d8-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="5f1d8-226">Sie können ein dnsZone-Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="5f1d8-227">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f1d8-227">OUTPUTS</span></span>

### <span data-ttu-id="5f1d8-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5f1d8-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="5f1d8-229">Dieses Cmdlet gibt ein **Recordset** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="5f1d8-230">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f1d8-230">NOTES</span></span>
<span data-ttu-id="5f1d8-231">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5f1d8-232">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="5f1d8-233">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5f1d8-234">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5f1d8-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5f1d8-235">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f1d8-235">RELATED LINKS</span></span>

[<span data-ttu-id="5f1d8-236">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5f1d8-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="5f1d8-237">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5f1d8-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="5f1d8-238">Neu – AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5f1d8-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="5f1d8-239">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5f1d8-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="5f1d8-240">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5f1d8-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175548"
---
# <span data-ttu-id="182ce-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="182ce-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="182ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="182ce-102">SYNOPSIS</span></span>
<span data-ttu-id="182ce-103">Erstellt einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="182ce-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="182ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="182ce-104">SYNTAX</span></span>

### <span data-ttu-id="182ce-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="182ce-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="182ce-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="182ce-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="182ce-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="182ce-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="182ce-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="182ce-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="182ce-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="182ce-109">DESCRIPTION</span></span>
<span data-ttu-id="182ce-110">Das **Cmdlet "New-AzDnsRecordSet"** erstellt einen neuen DNS (Domain Name System)-Eintrag, der mit dem angegebenen Namen und Typ in der angegebenen Zone festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="182ce-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="182ce-111">Ein **"RecordSet"-Objekt** ist eine Reihe von DNS-Einträgen mit demselben Namen und Typ.</span><span class="sxs-lookup"><span data-stu-id="182ce-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="182ce-112">Beachten Sie, dass der Name relativ zur Zone und nicht zum vollqualifizierten Namen ist.</span><span class="sxs-lookup"><span data-stu-id="182ce-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="182ce-113">Der *Parameter "DnsRecords"* gibt die Einträge im Datensatzsatz an.</span><span class="sxs-lookup"><span data-stu-id="182ce-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="182ce-114">Dieser Parameter übernimmt ein Array von DNS-Einträgen, das mit "New-AzDnsRecordConfig" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="182ce-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="182ce-115">Sie können den Pipelineoperator verwenden, um ein **"DnsZone"-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **"DnsZone"-Objekt** als *Parameter "Zone"* übergeben, oder Sie können die Zone auch nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="182ce-116">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="182ce-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="182ce-117">Wenn bereits ein übereinstimmender **Eintrag** vorhanden ist (derselbe Name und Datensatztyp), müssen Sie den Parameter *"Overwrite"* angeben. Andernfalls erstellt das Cmdlet kein neues **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="182ce-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="182ce-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="182ce-118">EXAMPLES</span></span>

### <span data-ttu-id="182ce-119">Beispiel 1: Erstellen eines Datensatzes vom Typ A</span><span class="sxs-lookup"><span data-stu-id="182ce-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="182ce-120">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-121">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-122">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="182ce-123">Beispiel 2: Erstellen eines RecordSets vom Typ AAAA</span><span class="sxs-lookup"><span data-stu-id="182ce-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-124">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-125">Der Datensatzsatz ist vom Typ AAAA und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-126">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-126">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-127">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-128">Beispiel 3: Erstellen eines Eintrags vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="182ce-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-129">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-130">Der Datensatzsatz ist vom Typ CNAME und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-131">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-131">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-132">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-133">Beispiel 4: Erstellen eines Eintrags vom Typ MX</span><span class="sxs-lookup"><span data-stu-id="182ce-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-134">Dieser Befehl erstellt ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-135">Der Eintragssatz ist vom Typ MX und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-136">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-136">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-137">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-138">Beispiel 5: Erstellen eines Datensatzes vom Typ NS</span><span class="sxs-lookup"><span data-stu-id="182ce-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-139">Dieser Befehl erstellt ein **RecordSet** namens "ns1" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-140">Der Datensatzsatz ist vom Typ "NS" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-141">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-141">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-142">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-143">Beispiel 6: Erstellen eines Datensatzes vom Typ PTR</span><span class="sxs-lookup"><span data-stu-id="182ce-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="182ce-144">Dieser Befehl erstellt ein **RecordSet** mit dem Namen 4 in der Zone 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="182ce-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="182ce-145">Der Datensatzsatz ist vom Typ "PTR" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-146">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-146">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-147">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-148">Beispiel 7: Erstellen eines RecordSet vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="182ce-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-149">Dieser Befehl erstellt ein **RecordSet** namens _sip._tcp in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-150">Der Datensatzsatz ist vom Typ SRV und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-151">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 zeigt.</span><span class="sxs-lookup"><span data-stu-id="182ce-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="182ce-152">Der Dienst (sip) und das Protokoll (tcp) werden als Teil des Datensatzsatznamens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="182ce-153">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-154">Beispiel 8: Erstellen eines Eintrags vom Typ TXT</span><span class="sxs-lookup"><span data-stu-id="182ce-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-155">Dieser Befehl erstellt einen **"RecordSet"-Benannten** Text in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-156">Der Datensatzsatz ist vom Typ TXT und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-157">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="182ce-157">It contains a single DNS record.</span></span>
<span data-ttu-id="182ce-158">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-159">Beispiel 9: Erstellen eines "RecordSet"-Eintrags am Anpunkt der Zone</span><span class="sxs-lookup"><span data-stu-id="182ce-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-160">Dieser Befehl erstellt **ein "RecordSet"** an der Spitze (oder Stamm) der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="182ce-161">Dazu wird der Name des Datensatzes als "@" angegeben (einschließlich der doppelten Anführungszeichen).</span><span class="sxs-lookup"><span data-stu-id="182ce-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="182ce-162">Sie können keine #A0 an der Spitze einer Zone erstellen.</span><span class="sxs-lookup"><span data-stu-id="182ce-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="182ce-163">Dies ist eine Einschränkung der DNS-Standards. ist keine Einschränkung von Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="182ce-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="182ce-164">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-165">Beispiel 10: Erstellen eines Platzhalterdatensatzes</span><span class="sxs-lookup"><span data-stu-id="182ce-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="182ce-166">Mit diesem Befehl wird ein **RecordSet** mit dem Namen \* in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-167">Dies ist ein Platzhalterdatensatz.</span><span class="sxs-lookup"><span data-stu-id="182ce-167">This is a wildcard record set.</span></span>
<span data-ttu-id="182ce-168">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="182ce-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="182ce-169">Beispiel 11: Erstellen eines leeren Datensatzes</span><span class="sxs-lookup"><span data-stu-id="182ce-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="182ce-170">Dieser Befehl erstellt ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="182ce-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="182ce-171">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="182ce-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="182ce-172">Dies ist ein leerer Datensatzsatz, der als Platzhalter fungiert, dem Sie später Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="182ce-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="182ce-173">Beispiel 12: Erstellen eines Datensatzes und Unterdrücken aller Bestätigungen</span><span class="sxs-lookup"><span data-stu-id="182ce-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="182ce-174">Mit diesem Befehl wird ein **RecordSet erstellt.**</span><span class="sxs-lookup"><span data-stu-id="182ce-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="182ce-175">Der *Parameter "Overwrite"* stellt sicher, dass dieser Datensatzsatz alle bereits vorhandenen Datensatzsätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatzsatz gehen verloren).</span><span class="sxs-lookup"><span data-stu-id="182ce-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="182ce-176">Der *Parameter "Bestätigen"* mit dem Wert $False Bestätigungsaufforderung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="182ce-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="182ce-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="182ce-177">PARAMETERS</span></span>

### <span data-ttu-id="182ce-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182ce-178">-DefaultProfile</span></span>
<span data-ttu-id="182ce-179">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="182ce-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="182ce-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="182ce-180">-DnsRecords</span></span>
<span data-ttu-id="182ce-181">Gibt das Array der DNS-Einträge an, die in den Datensatzsatz aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="182ce-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="182ce-182">Sie können das cmdlet New-AzDnsRecordConfig zum Erstellen von Objekten für den DNS-Eintrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="182ce-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="182ce-183">Weitere Informationen finden Sie in den Beispielen.</span><span class="sxs-lookup"><span data-stu-id="182ce-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="182ce-184">-Metadata</span></span>
<span data-ttu-id="182ce-185">Gibt ein Array von Metadaten an, das dem RecordSet zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="182ce-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="182ce-186">Metadaten werden mithilfe von Name-Wert-Paaren angegeben, die als Hashtabellen dargestellt werden, z. B. @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="182ce-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-187">-Name</span><span class="sxs-lookup"><span data-stu-id="182ce-187">-Name</span></span>
<span data-ttu-id="182ce-188">Gibt den Namen des zu erstellenden **Datensatzes** an.</span><span class="sxs-lookup"><span data-stu-id="182ce-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="182ce-189">-Overwrite</span></span>
<span data-ttu-id="182ce-190">Gibt an, dass dieses Cmdlet das angegebene **RecordSet** überschreibt, wenn es bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="182ce-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="182ce-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="182ce-191">-RecordType</span></span>
<span data-ttu-id="182ce-192">Gibt den Typ des zu erstellenden DNS-Eintrags an.</span><span class="sxs-lookup"><span data-stu-id="182ce-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="182ce-193">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="182ce-193">Valid values are:</span></span>
- <span data-ttu-id="182ce-194">A</span><span class="sxs-lookup"><span data-stu-id="182ce-194">A</span></span>
- <span data-ttu-id="182ce-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="182ce-195">AAAA</span></span>
- <span data-ttu-id="182ce-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="182ce-196">CNAME</span></span>
- <span data-ttu-id="182ce-197">MX</span><span class="sxs-lookup"><span data-stu-id="182ce-197">MX</span></span>
- <span data-ttu-id="182ce-198">NS</span><span class="sxs-lookup"><span data-stu-id="182ce-198">NS</span></span>
- <span data-ttu-id="182ce-199">PTR</span><span class="sxs-lookup"><span data-stu-id="182ce-199">PTR</span></span>
- <span data-ttu-id="182ce-200">SRV</span><span class="sxs-lookup"><span data-stu-id="182ce-200">SRV</span></span>
- <span data-ttu-id="182ce-201">TXT-SOA-Einträge werden beim Erstellen der Zone automatisch erstellt und können nicht manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="182ce-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="182ce-202">-ResourceGroupName</span></span>
<span data-ttu-id="182ce-203">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="182ce-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="182ce-204">Sie müssen auch den *Parameter "ZoneName"* angeben, um den Zonennamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="182ce-205">Alternativ können Sie die Zone und Ressourcengruppe angeben, indem Sie ein DNS -Zonenobjekt mit dem Parameter *"Zone"* übergeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="182ce-206">-TargetResourceId</span></span>
<span data-ttu-id="182ce-207">Aliaszielressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="182ce-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="182ce-208">-Ttl</span></span>
<span data-ttu-id="182ce-209">Gibt die Gültigkeitsdauer (Time to Live, TTL) für das DNS RecordSet an.</span><span class="sxs-lookup"><span data-stu-id="182ce-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="182ce-210">-Zone</span></span>
<span data-ttu-id="182ce-211">Gibt den DnsZone-Wert an, in dem **recordSet erstellt werden soll.**</span><span class="sxs-lookup"><span data-stu-id="182ce-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="182ce-212">Alternativ können Sie die Zone mit den Parametern *"ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="182ce-213">-ZoneName</span></span>
<span data-ttu-id="182ce-214">Gibt den Namen der Zone an, in der das **RecordSet erstellt werden soll.**</span><span class="sxs-lookup"><span data-stu-id="182ce-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="182ce-215">Sie müssen auch die Ressourcengruppe angeben, die die Zone enthält, indem Sie den *Parameter "ResourceGroupName"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="182ce-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="182ce-216">Alternativ können Sie die Zone und Ressourcengruppe angeben, indem Sie ein DNS -Zonenobjekt mit dem Parameter *"Zone"* übergeben.</span><span class="sxs-lookup"><span data-stu-id="182ce-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="182ce-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="182ce-217">-Confirm</span></span>
<span data-ttu-id="182ce-218">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="182ce-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="182ce-219">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="182ce-219">-WhatIf</span></span>
<span data-ttu-id="182ce-220">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="182ce-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="182ce-221">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="182ce-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="182ce-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182ce-222">CommonParameters</span></span>
<span data-ttu-id="182ce-223">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="182ce-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182ce-224">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182ce-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182ce-225">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="182ce-225">INPUTS</span></span>

### <span data-ttu-id="182ce-226">System.String</span><span class="sxs-lookup"><span data-stu-id="182ce-226">System.String</span></span>

### <span data-ttu-id="182ce-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="182ce-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="182ce-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="182ce-228">System.UInt32</span></span>

### <span data-ttu-id="182ce-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="182ce-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="182ce-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="182ce-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="182ce-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="182ce-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="182ce-232">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="182ce-232">OUTPUTS</span></span>

### <span data-ttu-id="182ce-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="182ce-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="182ce-234">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="182ce-234">NOTES</span></span>
<span data-ttu-id="182ce-235">Mit dem Parameter *"Bestätigen"* können Sie steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="182ce-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="182ce-236">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn $ConfirmPreference Windows PowerShell Variable den Wert "Mittel" oder "Niedriger" hat.</span><span class="sxs-lookup"><span data-stu-id="182ce-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="182ce-237">Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True"* angeben, fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="182ce-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="182ce-238">Wenn Sie *"Confirm:$False" angeben,* werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="182ce-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="182ce-239">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="182ce-239">RELATED LINKS</span></span>

[<span data-ttu-id="182ce-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="182ce-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="182ce-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="182ce-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="182ce-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="182ce-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="182ce-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="182ce-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="182ce-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="182ce-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

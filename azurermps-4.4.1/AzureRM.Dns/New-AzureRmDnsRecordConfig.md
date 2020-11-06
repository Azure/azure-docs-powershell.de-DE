---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 98418beaf029b1e1a40ec78fa2a794c2218ab753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502741"
---
# <span data-ttu-id="d29c0-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d29c0-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="d29c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d29c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d29c0-103">Erstellt ein neues lokales DNS-Eintrags Objekt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d29c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d29c0-104">SYNTAX</span></span>

### <span data-ttu-id="d29c0-105">Eine</span><span class="sxs-lookup"><span data-stu-id="d29c0-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29c0-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="d29c0-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29c0-107">NS</span><span class="sxs-lookup"><span data-stu-id="d29c0-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29c0-108">MX</span><span class="sxs-lookup"><span data-stu-id="d29c0-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29c0-109">PTR</span><span class="sxs-lookup"><span data-stu-id="d29c0-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29c0-110">Txt</span><span class="sxs-lookup"><span data-stu-id="d29c0-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29c0-111">SRV</span><span class="sxs-lookup"><span data-stu-id="d29c0-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d29c0-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="d29c0-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d29c0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d29c0-113">DESCRIPTION</span></span>
<span data-ttu-id="d29c0-114">Mit dem Cmdlet **New-AzureRmDnsRecordConfig** wird ein lokales **DnsRecord** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="d29c0-115">Ein Array dieser Objekte wird mithilfe des *DnsRecords* -Parameters an das New-AzureRmDnsRecordSet-Cmdlet übergeben, um die in der Datensatzgruppe zu erstellenden Datensätze anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d29c0-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="d29c0-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d29c0-116">EXAMPLES</span></span>

### <span data-ttu-id="d29c0-117">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="d29c0-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="d29c0-118">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-119">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-120">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="d29c0-121">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="d29c0-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-122">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-123">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-124">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-124">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-125">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-126">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="d29c0-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-127">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-128">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-129">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-129">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-130">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-131">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="d29c0-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-132">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-133">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-134">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-134">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-135">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-136">Beispiel 5: Erstellen eines Recordsets des Typs NS</span><span class="sxs-lookup"><span data-stu-id="d29c0-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-137">Dieser Befehl erstellt ein **Recordset** mit dem Namen ns1 in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d29c0-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-138">Der Daten Satz Satz ist vom Typ NS und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-139">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-139">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-140">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-141">Beispiel 6: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="d29c0-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="d29c0-142">Mit diesem Befehl wird ein **Recordset** mit dem Namen 4 in der Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="d29c0-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="d29c0-143">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-144">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-144">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-145">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-146">Beispiel 7: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="d29c0-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-147">Dieser Befehl erstellt ein **Recordset** mit dem Namen "_sip. _tcp" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d29c0-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-148">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-149">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="d29c0-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="d29c0-150">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="d29c0-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="d29c0-151">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d29c0-152">Beispiel 8: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="d29c0-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d29c0-153">Dieser Befehl erstellt ein **Recordset** mit dem Namen "Text" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d29c0-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="d29c0-154">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d29c0-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d29c0-155">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d29c0-155">It contains a single DNS record.</span></span>

<span data-ttu-id="d29c0-156">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="d29c0-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="d29c0-157">Parameter</span><span class="sxs-lookup"><span data-stu-id="d29c0-157">PARAMETERS</span></span>

### <span data-ttu-id="d29c0-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="d29c0-158">-Cname</span></span>
<span data-ttu-id="d29c0-159">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d29c0-160">-Exchange</span></span>
<span data-ttu-id="d29c0-161">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d29c0-162">-Ipv4Address</span></span>
<span data-ttu-id="d29c0-163">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="d29c0-164">-IPv6</span><span class="sxs-lookup"><span data-stu-id="d29c0-164">-Ipv6Address</span></span>
<span data-ttu-id="d29c0-165">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="d29c0-166">-Nsdname</span></span>
<span data-ttu-id="d29c0-167">Gibt den Namenserver Namen für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-168">-Port</span><span class="sxs-lookup"><span data-stu-id="d29c0-168">-Port</span></span>
<span data-ttu-id="d29c0-169">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-170">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="d29c0-170">-Preference</span></span>
<span data-ttu-id="d29c0-171">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-172">-Priorität</span><span class="sxs-lookup"><span data-stu-id="d29c0-172">-Priority</span></span>
<span data-ttu-id="d29c0-173">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d29c0-174">-Ptrdname</span></span>
<span data-ttu-id="d29c0-175">Gibt den Zieldomänen Namen eines PTR-Eintrags (Pointer Resource) an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-176">-Target</span><span class="sxs-lookup"><span data-stu-id="d29c0-176">-Target</span></span>
<span data-ttu-id="d29c0-177">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-178">-Wert</span><span class="sxs-lookup"><span data-stu-id="d29c0-178">-Value</span></span>
<span data-ttu-id="d29c0-179">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-180">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="d29c0-180">-Weight</span></span>
<span data-ttu-id="d29c0-181">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="d29c0-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29c0-182">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29c0-182">-DefaultProfile</span></span>
<span data-ttu-id="d29c0-183">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d29c0-183">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29c0-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29c0-184">CommonParameters</span></span>
<span data-ttu-id="d29c0-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29c0-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29c0-186">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29c0-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29c0-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d29c0-187">INPUTS</span></span>

### <span data-ttu-id="d29c0-188">Keine.</span><span class="sxs-lookup"><span data-stu-id="d29c0-188">None.</span></span>

## <span data-ttu-id="d29c0-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d29c0-189">OUTPUTS</span></span>

### <span data-ttu-id="d29c0-190">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="d29c0-190">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="d29c0-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="d29c0-191">NOTES</span></span>

## <span data-ttu-id="d29c0-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d29c0-192">RELATED LINKS</span></span>

[<span data-ttu-id="d29c0-193">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d29c0-193">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="d29c0-194">Neu – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d29c0-194">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d29c0-195">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d29c0-195">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

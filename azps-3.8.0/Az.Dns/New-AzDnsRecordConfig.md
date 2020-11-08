---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996140"
---
# <span data-ttu-id="9d9c6-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d9c6-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9d9c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9c6-103">Erstellt ein neues lokales DNS-Eintrags Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="9d9c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d9c6-104">SYNTAX</span></span>

### <span data-ttu-id="9d9c6-105">Eine</span><span class="sxs-lookup"><span data-stu-id="9d9c6-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9d9c6-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-107">NS</span><span class="sxs-lookup"><span data-stu-id="9d9c6-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-108">MX</span><span class="sxs-lookup"><span data-stu-id="9d9c6-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-109">PTR</span><span class="sxs-lookup"><span data-stu-id="9d9c6-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-110">Txt</span><span class="sxs-lookup"><span data-stu-id="9d9c6-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-111">SRV</span><span class="sxs-lookup"><span data-stu-id="9d9c6-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="9d9c6-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-113">CAA</span><span class="sxs-lookup"><span data-stu-id="9d9c6-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d9c6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d9c6-114">DESCRIPTION</span></span>
<span data-ttu-id="9d9c6-115">Mit dem Cmdlet **New-AzDnsRecordConfig** wird ein lokales **DnsRecord** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="9d9c6-116">Ein Array dieser Objekte wird mithilfe des *DnsRecords* -Parameters an das New-AzDnsRecordSet-Cmdlet übergeben, um die in der Datensatzgruppe zu erstellenden Datensätze anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="9d9c6-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d9c6-117">EXAMPLES</span></span>

### <span data-ttu-id="9d9c6-118">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="9d9c6-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="9d9c6-119">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-120">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-121">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="9d9c6-122">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="9d9c6-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-123">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-124">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-125">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-125">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-126">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-127">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="9d9c6-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-128">In diesem Beispiel wird ein **Recordset** mit dem Namen www in der Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-129">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-130">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-130">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-131">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-132">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="9d9c6-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-133">Mit diesem Befehl wird in der Zone myzone.com ein **Recordset** mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-134">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-135">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-135">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-136">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-137">Beispiel 5: Erstellen eines Recordsets des Typs NS</span><span class="sxs-lookup"><span data-stu-id="9d9c6-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-138">Dieser Befehl erstellt ein **Recordset** mit dem Namen ns1 in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-139">Der Daten Satz Satz ist vom Typ NS und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-140">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-140">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-141">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-142">Beispiel 6: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="9d9c6-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-143">Mit diesem Befehl wird ein **Recordset** mit dem Namen 4 in der Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="9d9c6-144">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-145">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-145">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-146">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-147">Beispiel 7: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="9d9c6-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-148">Dieser Befehl erstellt ein **Recordset** mit dem Namen "_sip. _tcp" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-149">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-150">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="9d9c6-151">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="9d9c6-152">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9d9c6-153">Beispiel 8: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="9d9c6-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9d9c6-154">Dieser Befehl erstellt ein **Recordset** mit dem Namen "Text" in der Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="9d9c6-155">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9d9c6-156">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-156">It contains a single DNS record.</span></span>
<span data-ttu-id="9d9c6-157">Informationen zum Erstellen eines **Recordsets** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="9d9c6-158">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d9c6-158">PARAMETERS</span></span>

### <span data-ttu-id="9d9c6-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="9d9c6-159">-CaaFlags</span></span>
<span data-ttu-id="9d9c6-160">Die Flags für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="9d9c6-161">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="9d9c6-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="9d9c6-162">-CaaTag</span></span>
<span data-ttu-id="9d9c6-163">Das Tag-Feld des hinzuzufügenden CAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="9d9c6-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="9d9c6-164">-CaaValue</span></span>
<span data-ttu-id="9d9c6-165">Das Feld "Wert" für den hinzuzufügenden CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="9d9c6-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="9d9c6-166">-Cname</span></span>
<span data-ttu-id="9d9c6-167">Gibt den Domänennamen für einen CNAME-Eintrag (Kanonischer Name) an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="9d9c6-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9c6-168">-DefaultProfile</span></span>
<span data-ttu-id="9d9c6-169">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d9c6-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d9c6-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9d9c6-170">-Exchange</span></span>
<span data-ttu-id="9d9c6-171">Gibt den e-Mail-Exchange-Servernamen für einen MX-Eintrag (Mail Exchange) an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="9d9c6-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9d9c6-172">-Ipv4Address</span></span>
<span data-ttu-id="9d9c6-173">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9d9c6-174">-IPv6</span><span class="sxs-lookup"><span data-stu-id="9d9c6-174">-Ipv6Address</span></span>
<span data-ttu-id="9d9c6-175">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="9d9c6-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="9d9c6-176">-Nsdname</span></span>
<span data-ttu-id="9d9c6-177">Gibt den Namenserver Namen für einen Namenserver (NS)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="9d9c6-178">-Port</span><span class="sxs-lookup"><span data-stu-id="9d9c6-178">-Port</span></span>
<span data-ttu-id="9d9c6-179">Gibt den Port für einen Dienst (SRV)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="9d9c6-180">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="9d9c6-180">-Preference</span></span>
<span data-ttu-id="9d9c6-181">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="9d9c6-182">-Priorität</span><span class="sxs-lookup"><span data-stu-id="9d9c6-182">-Priority</span></span>
<span data-ttu-id="9d9c6-183">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="9d9c6-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9d9c6-184">-Ptrdname</span></span>
<span data-ttu-id="9d9c6-185">Gibt den Zieldomänen Namen eines PTR-Eintrags (Pointer Resource) an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="9d9c6-186">-Target</span><span class="sxs-lookup"><span data-stu-id="9d9c6-186">-Target</span></span>
<span data-ttu-id="9d9c6-187">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="9d9c6-188">-Wert</span><span class="sxs-lookup"><span data-stu-id="9d9c6-188">-Value</span></span>
<span data-ttu-id="9d9c6-189">Gibt den Wert für einen TXT-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="9d9c6-190">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="9d9c6-190">-Weight</span></span>
<span data-ttu-id="9d9c6-191">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="9d9c6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9c6-192">CommonParameters</span></span>
<span data-ttu-id="9d9c6-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9c6-194">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9c6-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9c6-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d9c6-195">INPUTS</span></span>

### <span data-ttu-id="9d9c6-196">System. String</span><span class="sxs-lookup"><span data-stu-id="9d9c6-196">System.String</span></span>

### <span data-ttu-id="9d9c6-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="9d9c6-197">System.UInt16</span></span>

### <span data-ttu-id="9d9c6-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="9d9c6-198">System.Byte</span></span>

## <span data-ttu-id="9d9c6-199">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d9c6-199">OUTPUTS</span></span>

### <span data-ttu-id="9d9c6-200">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="9d9c6-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="9d9c6-201">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d9c6-201">NOTES</span></span>

## <span data-ttu-id="9d9c6-202">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d9c6-202">RELATED LINKS</span></span>

[<span data-ttu-id="9d9c6-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d9c6-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="9d9c6-204">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9d9c6-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="9d9c6-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d9c6-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

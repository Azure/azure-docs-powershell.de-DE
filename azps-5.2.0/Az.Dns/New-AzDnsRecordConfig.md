---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302379"
---
# <span data-ttu-id="89221-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="89221-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="89221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89221-102">SYNOPSIS</span></span>
<span data-ttu-id="89221-103">Erstellt ein neues lokales Objekt für den DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="89221-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89221-104">SYNTAX</span></span>

### <span data-ttu-id="89221-105">A</span><span class="sxs-lookup"><span data-stu-id="89221-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="89221-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-107">Ns</span><span class="sxs-lookup"><span data-stu-id="89221-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-108">Mx</span><span class="sxs-lookup"><span data-stu-id="89221-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89221-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="89221-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-110">Txt</span><span class="sxs-lookup"><span data-stu-id="89221-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-111">Srv</span><span class="sxs-lookup"><span data-stu-id="89221-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-112">CName</span><span class="sxs-lookup"><span data-stu-id="89221-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89221-113">Caa</span><span class="sxs-lookup"><span data-stu-id="89221-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89221-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89221-114">DESCRIPTION</span></span>
<span data-ttu-id="89221-115">Das **Cmdlet "New-AzDnsRecordConfig"** erstellt ein lokales **DnsRecord-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="89221-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="89221-116">Ein Array dieser Objekte wird mithilfe des New-AzDnsRecordSet *DnsRecords* an das cmdlet New-AzDnsRecordSet übergeben, um die Einträge anzugeben, die im Datensatzsatz erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="89221-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="89221-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89221-117">EXAMPLES</span></span>

### <span data-ttu-id="89221-118">Beispiel 1: Erstellen eines Datensatzes vom Typ A</span><span class="sxs-lookup"><span data-stu-id="89221-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="89221-119">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="89221-120">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-121">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="89221-122">Beispiel 2: Erstellen eines RecordSets vom Typ AAAA</span><span class="sxs-lookup"><span data-stu-id="89221-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-123">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="89221-124">Der Datensatzsatz ist vom Typ AAAA und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-125">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-125">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-126">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-127">Beispiel 3: Erstellen eines Eintrags vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="89221-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-128">In diesem Beispiel wird ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="89221-129">Der Datensatzsatz ist vom Typ CNAME und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-130">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-130">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-131">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-132">Beispiel 4: Erstellen eines Eintrags vom Typ MX</span><span class="sxs-lookup"><span data-stu-id="89221-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-133">Dieser Befehl erstellt ein **RecordSet** mit dem Namen "www" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="89221-134">Der Eintragssatz ist vom Typ MX und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-135">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-135">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-136">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-137">Beispiel 5: Erstellen eines Datensatzes vom Typ NS</span><span class="sxs-lookup"><span data-stu-id="89221-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-138">Dieser Befehl erstellt ein **RecordSet** namens "ns1" in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="89221-139">Der Datensatzsatz ist vom Typ "NS" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-140">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-140">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-141">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-142">Beispiel 6: Erstellen eines Datensatzes vom Typ PTR</span><span class="sxs-lookup"><span data-stu-id="89221-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="89221-143">Mit diesem Befehl wird ein **RecordSet** mit dem Namen 4 in der Zone 3.2.1.in-addr.arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="89221-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="89221-144">Der Datensatzsatz ist vom Typ "PTR" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-145">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-145">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-146">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-147">Beispiel 7: Erstellen eines RecordSet vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="89221-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-148">Dieser Befehl erstellt ein **RecordSet** namens _sip._tcp in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="89221-149">Der Datensatzsatz ist vom Typ SRV und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-150">Sie enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 zeigt.</span><span class="sxs-lookup"><span data-stu-id="89221-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="89221-151">Der Dienst (sip) und das Protokoll (tcp) werden als Teil des Datensatzsatznamens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="89221-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="89221-152">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="89221-153">Beispiel 8: Erstellen eines Eintrags vom Typ TXT</span><span class="sxs-lookup"><span data-stu-id="89221-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="89221-154">Dieser Befehl erstellt einen **"RecordSet"-Benannten** Text in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="89221-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="89221-155">Der Datensatzsatz ist vom Typ TXT und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="89221-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="89221-156">Sie enthält einen einzelnen DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-156">It contains a single DNS record.</span></span>
<span data-ttu-id="89221-157">Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="89221-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="89221-158">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89221-158">PARAMETERS</span></span>

### <span data-ttu-id="89221-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="89221-159">-CaaFlags</span></span>
<span data-ttu-id="89221-160">Die Kennzeichen für den hinzuzufügende CAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="89221-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="89221-161">Muss eine Zahl zwischen 0 und 255 sein.</span><span class="sxs-lookup"><span data-stu-id="89221-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="89221-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="89221-162">-CaaTag</span></span>
<span data-ttu-id="89221-163">Das Tagfeld des hinzuzufügende ZERTIFIZIERUNGA-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="89221-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="89221-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="89221-164">-CaaValue</span></span>
<span data-ttu-id="89221-165">Das Wertfeld für den hinzuzufügende ZERTIFIZIERUNGA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89221-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="89221-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="89221-166">-Cname</span></span>
<span data-ttu-id="89221-167">Gibt den Domänennamen für einen kanonischen Namen (CNAME)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="89221-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89221-168">-DefaultProfile</span></span>
<span data-ttu-id="89221-169">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89221-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89221-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="89221-170">-Exchange</span></span>
<span data-ttu-id="89221-171">Gibt den E-Mail-Exchange-Servernamen für einen Mail Exchange (MX)-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="89221-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="89221-172">-Ipv4Address</span></span>
<span data-ttu-id="89221-173">Gibt eine IPv4-Adresse für einen A-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="89221-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="89221-174">-Ipv6Address</span></span>
<span data-ttu-id="89221-175">Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="89221-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="89221-176">-Nsdname</span></span>
<span data-ttu-id="89221-177">Gibt den Namen des Namenservers für einen Namenserverdatensatz an.</span><span class="sxs-lookup"><span data-stu-id="89221-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="89221-178">-Port</span><span class="sxs-lookup"><span data-stu-id="89221-178">-Port</span></span>
<span data-ttu-id="89221-179">Gibt den Port für einen Dienstdatensatz (SRV) an.</span><span class="sxs-lookup"><span data-stu-id="89221-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="89221-180">-Preference</span><span class="sxs-lookup"><span data-stu-id="89221-180">-Preference</span></span>
<span data-ttu-id="89221-181">Gibt die Einstellung für einen MX-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="89221-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="89221-182">-Priority</span></span>
<span data-ttu-id="89221-183">Gibt die Priorität für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="89221-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="89221-184">-Ptrdname</span></span>
<span data-ttu-id="89221-185">Gibt den Zieldomänennamen eines Zeigerressourcendatensatzes (PtR) an.</span><span class="sxs-lookup"><span data-stu-id="89221-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="89221-186">-Target</span><span class="sxs-lookup"><span data-stu-id="89221-186">-Target</span></span>
<span data-ttu-id="89221-187">Gibt das Ziel für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="89221-188">-Value</span><span class="sxs-lookup"><span data-stu-id="89221-188">-Value</span></span>
<span data-ttu-id="89221-189">Gibt den Wert für einen "TXT"-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="89221-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="89221-190">-Weight</span></span>
<span data-ttu-id="89221-191">Gibt die Gewichtung für einen SRV-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="89221-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="89221-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89221-192">CommonParameters</span></span>
<span data-ttu-id="89221-193">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89221-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89221-194">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89221-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89221-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89221-195">INPUTS</span></span>

### <span data-ttu-id="89221-196">System.String</span><span class="sxs-lookup"><span data-stu-id="89221-196">System.String</span></span>

### <span data-ttu-id="89221-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="89221-197">System.UInt16</span></span>

### <span data-ttu-id="89221-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="89221-198">System.Byte</span></span>

## <span data-ttu-id="89221-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89221-199">OUTPUTS</span></span>

### <span data-ttu-id="89221-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="89221-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="89221-201">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89221-201">NOTES</span></span>

## <span data-ttu-id="89221-202">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89221-202">RELATED LINKS</span></span>

[<span data-ttu-id="89221-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="89221-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="89221-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89221-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="89221-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="89221-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

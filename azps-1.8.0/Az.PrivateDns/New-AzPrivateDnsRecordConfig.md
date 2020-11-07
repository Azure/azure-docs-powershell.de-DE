---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659990"
---
# <span data-ttu-id="0e6f5-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="0e6f5-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="0e6f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6f5-103">Erstellt ein neues privates DNS-Eintrags lokales Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="0e6f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e6f5-104">SYNTAX</span></span>

### <span data-ttu-id="0e6f5-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e6f5-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="0e6f5-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-107">MX</span><span class="sxs-lookup"><span data-stu-id="0e6f5-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-108">PTR</span><span class="sxs-lookup"><span data-stu-id="0e6f5-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-109">TXT</span><span class="sxs-lookup"><span data-stu-id="0e6f5-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-110">SRV</span><span class="sxs-lookup"><span data-stu-id="0e6f5-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e6f5-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="0e6f5-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e6f5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e6f5-112">DESCRIPTION</span></span>
<span data-ttu-id="0e6f5-113">Mit dem New-AzPrivateDnsRecordConfig-Cmdlet wird ein lokales PSPrivateDnsRecord-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="0e6f5-114">Ein Array dieser Objekte wird mithilfe des PrivateDnsRecord-Parameters an das New-AzPrivateDnsRecordSet-Cmdlet übergeben, um die in der Datensatzgruppe zu erstellenden Datensätze anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="0e6f5-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e6f5-115">EXAMPLES</span></span>

### <span data-ttu-id="0e6f5-116">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="0e6f5-116">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-117">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-118">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-119">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="0e6f5-120">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="0e6f5-120">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-121">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-122">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-123">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="0e6f5-124">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e6f5-125">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="0e6f5-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-126">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-127">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-128">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="0e6f5-129">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e6f5-130">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="0e6f5-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-131">Mit diesem Befehl wird in der privaten Zone myzone.com ein Recordset mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-132">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-133">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="0e6f5-134">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e6f5-135">Beispiel 5: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="0e6f5-135">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-136">Mit diesem Befehl wird ein Recordset mit dem Namen 4 in der privaten Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="0e6f5-137">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-138">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="0e6f5-139">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e6f5-140">Beispiel 6: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="0e6f5-140">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-141">Dieser Befehl erstellt ein Recordset mit dem Namen "_sip. _tcp" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-142">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-143">Sie enthält einen einzelnen privaten DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="0e6f5-144">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="0e6f5-145">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0e6f5-146">Beispiel 7: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="0e6f5-146">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0e6f5-147">Dieser Befehl erstellt ein Recordset mit dem Namen "Text" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="0e6f5-148">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0e6f5-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0e6f5-149">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="0e6f5-150">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="0e6f5-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e6f5-151">PARAMETERS</span></span>

### <span data-ttu-id="0e6f5-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="0e6f5-152">-Cname</span></span>
<span data-ttu-id="0e6f5-153">Der kanonische Name für den hinzuzufügenden CNAME-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="0e6f5-154">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0e6f5-155">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6f5-156">-DefaultProfile</span></span>
<span data-ttu-id="0e6f5-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e6f5-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0e6f5-158">-Exchange</span></span>
<span data-ttu-id="0e6f5-159">Der e-Mail-Exchange-Host für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="0e6f5-160">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0e6f5-161">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="0e6f5-162">-Ipv4Address</span></span>
<span data-ttu-id="0e6f5-163">Die IPv4-Adresse des hinzuzufügenden A-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-164">-IPv6</span><span class="sxs-lookup"><span data-stu-id="0e6f5-164">-Ipv6Address</span></span>
<span data-ttu-id="0e6f5-165">Die IPv6-Adresse des hinzuzufügenden AAAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-166">-Port</span><span class="sxs-lookup"><span data-stu-id="0e6f5-166">-Port</span></span>
<span data-ttu-id="0e6f5-167">Die Portnummer für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-168">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="0e6f5-168">-Preference</span></span>
<span data-ttu-id="0e6f5-169">Der Einstellungswert für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-170">-Priorität</span><span class="sxs-lookup"><span data-stu-id="0e6f5-170">-Priority</span></span>
<span data-ttu-id="0e6f5-171">Der hinzuzufügende SRV-Eintrag des Prioritätswerts.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="0e6f5-172">-Ptrdname</span></span>
<span data-ttu-id="0e6f5-173">Der Ziel Host für den hinzuzufügenden PTR-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="0e6f5-174">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0e6f5-175">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-176">-Target</span><span class="sxs-lookup"><span data-stu-id="0e6f5-176">-Target</span></span>
<span data-ttu-id="0e6f5-177">Der Ziel Host für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="0e6f5-178">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="0e6f5-179">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-180">-Wert</span><span class="sxs-lookup"><span data-stu-id="0e6f5-180">-Value</span></span>
<span data-ttu-id="0e6f5-181">Der Textwert für den hinzuzufügenden TXT-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-182">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="0e6f5-182">-Weight</span></span>
<span data-ttu-id="0e6f5-183">Der Gewichtungswert für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6f5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6f5-184">CommonParameters</span></span>
<span data-ttu-id="0e6f5-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6f5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6f5-186">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6f5-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6f5-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-187">INPUTS</span></span>

### <span data-ttu-id="0e6f5-188">Keine</span><span class="sxs-lookup"><span data-stu-id="0e6f5-188">None</span></span>

## <span data-ttu-id="0e6f5-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e6f5-189">OUTPUTS</span></span>

### <span data-ttu-id="0e6f5-190">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e6f5-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0e6f5-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e6f5-191">NOTES</span></span>

## <span data-ttu-id="0e6f5-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e6f5-192">RELATED LINKS</span></span>

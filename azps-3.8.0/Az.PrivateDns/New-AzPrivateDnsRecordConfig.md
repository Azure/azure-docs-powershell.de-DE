---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 6653491e7ee4a60b6ad9b392895454e5ee6dc3ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003167"
---
# <span data-ttu-id="f58ed-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f58ed-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f58ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f58ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f58ed-103">Erstellt ein neues privates DNS-Eintrags lokales Objekt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="f58ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f58ed-104">SYNTAX</span></span>

### <span data-ttu-id="f58ed-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="f58ed-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f58ed-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f58ed-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f58ed-107">MX</span><span class="sxs-lookup"><span data-stu-id="f58ed-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f58ed-108">PTR</span><span class="sxs-lookup"><span data-stu-id="f58ed-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58ed-109">TXT</span><span class="sxs-lookup"><span data-stu-id="f58ed-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58ed-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f58ed-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58ed-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="f58ed-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f58ed-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f58ed-112">DESCRIPTION</span></span>
<span data-ttu-id="f58ed-113">Mit dem New-AzPrivateDnsRecordConfig-Cmdlet wird ein lokales PSPrivateDnsRecord-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="f58ed-114">Ein Array dieser Objekte wird mithilfe des PrivateDnsRecord-Parameters an das New-AzPrivateDnsRecordSet-Cmdlet übergeben, um die in der Datensatzgruppe zu erstellenden Datensätze anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f58ed-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="f58ed-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f58ed-115">EXAMPLES</span></span>

### <span data-ttu-id="f58ed-116">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="f58ed-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="f58ed-117">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-118">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-119">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="f58ed-120">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="f58ed-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="f58ed-121">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-122">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-123">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="f58ed-124">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f58ed-125">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="f58ed-125">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="f58ed-126">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-127">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-128">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="f58ed-129">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f58ed-130">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="f58ed-130">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="f58ed-131">Mit diesem Befehl wird in der privaten Zone myzone.com ein Recordset mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-132">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-133">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="f58ed-134">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f58ed-135">Beispiel 5: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="f58ed-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="f58ed-136">Mit diesem Befehl wird ein Recordset mit dem Namen 4 in der privaten Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58ed-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="f58ed-137">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-138">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="f58ed-139">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f58ed-140">Beispiel 6: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="f58ed-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="f58ed-141">Dieser Befehl erstellt ein Recordset mit dem Namen "_sip. _tcp" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f58ed-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-142">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-143">Sie enthält einen einzelnen privaten DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="f58ed-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="f58ed-144">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="f58ed-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="f58ed-145">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f58ed-146">Beispiel 7: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="f58ed-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="f58ed-147">Dieser Befehl erstellt ein Recordset mit dem Namen "Text" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="f58ed-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="f58ed-148">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="f58ed-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="f58ed-149">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="f58ed-150">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="f58ed-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="f58ed-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="f58ed-151">PARAMETERS</span></span>

### <span data-ttu-id="f58ed-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f58ed-152">-Cname</span></span>
<span data-ttu-id="f58ed-153">Der kanonische Name für den hinzuzufügenden CNAME-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="f58ed-154">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="f58ed-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f58ed-155">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="f58ed-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f58ed-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58ed-156">-DefaultProfile</span></span>
<span data-ttu-id="f58ed-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f58ed-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f58ed-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f58ed-158">-Exchange</span></span>
<span data-ttu-id="f58ed-159">Der e-Mail-Exchange-Host für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="f58ed-160">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="f58ed-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f58ed-161">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="f58ed-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f58ed-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f58ed-162">-Ipv4Address</span></span>
<span data-ttu-id="f58ed-163">Die IPv4-Adresse des hinzuzufügenden A-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="f58ed-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="f58ed-164">-IPv6</span><span class="sxs-lookup"><span data-stu-id="f58ed-164">-Ipv6Address</span></span>
<span data-ttu-id="f58ed-165">Die IPv6-Adresse des hinzuzufügenden AAAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="f58ed-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="f58ed-166">-Port</span><span class="sxs-lookup"><span data-stu-id="f58ed-166">-Port</span></span>
<span data-ttu-id="f58ed-167">Die Portnummer für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="f58ed-168">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="f58ed-168">-Preference</span></span>
<span data-ttu-id="f58ed-169">Der Einstellungswert für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="f58ed-170">-Priorität</span><span class="sxs-lookup"><span data-stu-id="f58ed-170">-Priority</span></span>
<span data-ttu-id="f58ed-171">Der hinzuzufügende SRV-Eintrag des Prioritätswerts.</span><span class="sxs-lookup"><span data-stu-id="f58ed-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="f58ed-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f58ed-172">-Ptrdname</span></span>
<span data-ttu-id="f58ed-173">Der Ziel Host für den hinzuzufügenden PTR-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="f58ed-174">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="f58ed-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f58ed-175">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="f58ed-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f58ed-176">-Target</span><span class="sxs-lookup"><span data-stu-id="f58ed-176">-Target</span></span>
<span data-ttu-id="f58ed-177">Der Ziel Host für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="f58ed-178">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="f58ed-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f58ed-179">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="f58ed-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f58ed-180">-Wert</span><span class="sxs-lookup"><span data-stu-id="f58ed-180">-Value</span></span>
<span data-ttu-id="f58ed-181">Der Textwert für den hinzuzufügenden TXT-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="f58ed-182">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="f58ed-182">-Weight</span></span>
<span data-ttu-id="f58ed-183">Der Gewichtungswert für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f58ed-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="f58ed-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58ed-184">CommonParameters</span></span>
<span data-ttu-id="f58ed-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58ed-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58ed-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58ed-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58ed-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f58ed-187">INPUTS</span></span>

### <span data-ttu-id="f58ed-188">Keine</span><span class="sxs-lookup"><span data-stu-id="f58ed-188">None</span></span>

## <span data-ttu-id="f58ed-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f58ed-189">OUTPUTS</span></span>

### <span data-ttu-id="f58ed-190">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f58ed-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f58ed-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="f58ed-191">NOTES</span></span>

## <span data-ttu-id="f58ed-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f58ed-192">RELATED LINKS</span></span>

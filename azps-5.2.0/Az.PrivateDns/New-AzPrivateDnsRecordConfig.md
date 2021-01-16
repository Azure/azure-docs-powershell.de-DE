---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297912"
---
# <span data-ttu-id="26888-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="26888-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="26888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26888-102">SYNOPSIS</span></span>
<span data-ttu-id="26888-103">Erstellt ein neues lokales Objekt für einen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="26888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26888-104">SYNTAX</span></span>

### <span data-ttu-id="26888-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="26888-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26888-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="26888-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26888-107">MX</span><span class="sxs-lookup"><span data-stu-id="26888-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26888-108">PTR</span><span class="sxs-lookup"><span data-stu-id="26888-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26888-109">TXT</span><span class="sxs-lookup"><span data-stu-id="26888-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26888-110">SRV</span><span class="sxs-lookup"><span data-stu-id="26888-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26888-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="26888-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26888-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26888-112">DESCRIPTION</span></span>
<span data-ttu-id="26888-113">Das New-AzPrivateDnsRecordConfig erstellt ein lokales PSPrivateDnsRecord-Objekt.</span><span class="sxs-lookup"><span data-stu-id="26888-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="26888-114">Ein Array dieser Objekte wird mithilfe des New-AzPrivateDnsRecordSet Datensatzparameters an das cmdlet "privateDnsRecord" übergeben, um die Datensätze anzugeben, die im Datensatzsatz erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="26888-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="26888-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26888-115">EXAMPLES</span></span>

### <span data-ttu-id="26888-116">Beispiel 1: Erstellen eines Datensatzes vom Typ A</span><span class="sxs-lookup"><span data-stu-id="26888-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="26888-117">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="26888-118">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-119">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="26888-120">Beispiel 2: Erstellen eines RecordSets vom Typ AAAA</span><span class="sxs-lookup"><span data-stu-id="26888-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="26888-121">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="26888-122">Der Datensatzsatz ist vom Typ AAAA und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-123">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="26888-124">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="26888-125">Beispiel 3: Erstellen eines Eintrags vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="26888-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="26888-126">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="26888-127">Der Datensatzsatz ist vom Typ CNAME und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-128">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="26888-129">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="26888-130">Beispiel 4: Erstellen eines Eintrags vom Typ MX</span><span class="sxs-lookup"><span data-stu-id="26888-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="26888-131">Mit diesem Befehl wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="26888-132">Der Eintragssatz ist vom Typ MX und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-133">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="26888-134">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="26888-135">Beispiel 5: Erstellen eines Datensatzes vom Typ PTR</span><span class="sxs-lookup"><span data-stu-id="26888-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="26888-136">Mit diesem Befehl wird ein RecordSet mit dem Namen 4 in der privaten Zone 3.2.1.in-addr.arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="26888-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="26888-137">Der Datensatzsatz ist vom Typ "PTR" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-138">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="26888-139">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="26888-140">Beispiel 6: Erstellen eines RecordSet vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="26888-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="26888-141">Dieser Befehl erstellt ein RecordSet namens _sip._tcp in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="26888-142">Der Datensatzsatz ist vom Typ SRV und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-143">Sie enthält einen einzelnen privaten DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 zeigt.</span><span class="sxs-lookup"><span data-stu-id="26888-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="26888-144">Der Dienst (sip) und das Protokoll (tcp) werden als Teil des Datensatzsatznamens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="26888-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="26888-145">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="26888-146">Beispiel 7: Erstellen eines Eintrags vom Typ TXT</span><span class="sxs-lookup"><span data-stu-id="26888-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="26888-147">Mit diesem Befehl wird ein "RecordSet"-Benannter Text in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="26888-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="26888-148">Der Datensatzsatz ist vom Typ TXT und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="26888-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="26888-149">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="26888-150">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="26888-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="26888-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26888-151">PARAMETERS</span></span>

### <span data-ttu-id="26888-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="26888-152">-Cname</span></span>
<span data-ttu-id="26888-153">Der kanonische Name für den hinzuzufügende CNAME-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="26888-154">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="26888-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="26888-155">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="26888-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="26888-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26888-156">-DefaultProfile</span></span>
<span data-ttu-id="26888-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26888-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26888-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="26888-158">-Exchange</span></span>
<span data-ttu-id="26888-159">Der E-Mail-Exchange-Host für den hinzuzufügende MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="26888-160">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="26888-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="26888-161">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="26888-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="26888-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="26888-162">-Ipv4Address</span></span>
<span data-ttu-id="26888-163">Die IPv4-Adresse für den hinzuzufügende A-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="26888-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="26888-164">-Ipv6Address</span></span>
<span data-ttu-id="26888-165">Die IPv6-Adresse für den hinzuzufügende AAAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="26888-166">-Port</span><span class="sxs-lookup"><span data-stu-id="26888-166">-Port</span></span>
<span data-ttu-id="26888-167">Die Portnummer für den hinzuzufügende SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="26888-168">-Preference</span><span class="sxs-lookup"><span data-stu-id="26888-168">-Preference</span></span>
<span data-ttu-id="26888-169">Der Einstellungswert für den hinzuzufügende MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="26888-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="26888-170">-Priority</span></span>
<span data-ttu-id="26888-171">Der hinzuzufügende Prioritätswert des SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="26888-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="26888-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="26888-172">-Ptrdname</span></span>
<span data-ttu-id="26888-173">Der Zielhost für den hinzuzufügende PTR-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="26888-174">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="26888-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="26888-175">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="26888-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="26888-176">-Target</span><span class="sxs-lookup"><span data-stu-id="26888-176">-Target</span></span>
<span data-ttu-id="26888-177">Der Zielhost für den hinzuzufügende SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="26888-178">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="26888-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="26888-179">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="26888-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="26888-180">-Value</span><span class="sxs-lookup"><span data-stu-id="26888-180">-Value</span></span>
<span data-ttu-id="26888-181">Der Textwert für den hinzuzufügende TXT-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="26888-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="26888-182">-Weight</span></span>
<span data-ttu-id="26888-183">Der Gewichtungswert für den addieren SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="26888-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="26888-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26888-184">CommonParameters</span></span>
<span data-ttu-id="26888-185">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26888-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26888-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26888-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26888-187">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26888-187">INPUTS</span></span>

### <span data-ttu-id="26888-188">Keine</span><span class="sxs-lookup"><span data-stu-id="26888-188">None</span></span>

## <span data-ttu-id="26888-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26888-189">OUTPUTS</span></span>

### <span data-ttu-id="26888-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="26888-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="26888-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26888-191">NOTES</span></span>

## <span data-ttu-id="26888-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26888-192">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358139"
---
# <span data-ttu-id="0a380-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a380-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0a380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a380-102">SYNOPSIS</span></span>
<span data-ttu-id="0a380-103">Erstellt einen Datensatzsatz in einer privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="0a380-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="0a380-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a380-104">SYNTAX</span></span>

### <span data-ttu-id="0a380-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a380-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a380-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="0a380-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a380-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a380-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a380-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a380-108">DESCRIPTION</span></span>
<span data-ttu-id="0a380-109">Das New-AzPrivateDnsRecordSet erstellt einen neuen DNS (Private Domain Name System)-Eintrag, der mit dem angegebenen Namen und Typ in der angegebenen privaten Zone festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a380-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="0a380-110">Ein "RecordSet"-Objekt ist eine Reihe privater DNS-Einträge mit demselben Namen und Typ.</span><span class="sxs-lookup"><span data-stu-id="0a380-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="0a380-111">Beachten Sie, dass der Name relativ zur privaten Zone und nicht zum vollqualifizierten Namen ist.</span><span class="sxs-lookup"><span data-stu-id="0a380-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="0a380-112">Der Parameter "PrivateDnsRecord" gibt die Datensätze im Datensatzsatz an.</span><span class="sxs-lookup"><span data-stu-id="0a380-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="0a380-113">Dieser Parameter übernimmt ein Array privater DNS-Einträge, das mit New-AzPrivateDnsRecordConfig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0a380-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="0a380-114">Sie können den Pipelineoperator verwenden, um ein "PSPrivateDnsZone"-Objekt an dieses Cmdlet zu übergeben, oder Sie können ein "PSPrivateDnsZone"-Objekt als Zonenparameter übergeben, oder Sie können die Zone durch die ResourceId angeben. Alternativ können Sie die Zone auch nach Name angeben.</span><span class="sxs-lookup"><span data-stu-id="0a380-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="0a380-115">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0a380-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="0a380-116">Wenn bereits ein übereinstimmender Eintrag vorhanden ist (derselbe Name und Datensatztyp), müssen Sie den Parameter "Overwrite" angeben. Andernfalls erstellt das Cmdlet kein neues RecordSet.</span><span class="sxs-lookup"><span data-stu-id="0a380-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="0a380-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a380-117">EXAMPLES</span></span>

### <span data-ttu-id="0a380-118">Beispiel 1: Erstellen eines Datensatzes vom Typ A</span><span class="sxs-lookup"><span data-stu-id="0a380-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="0a380-119">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-120">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-121">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="0a380-122">Beispiel 2: Erstellen eines RecordSets vom Typ AAAA</span><span class="sxs-lookup"><span data-stu-id="0a380-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="0a380-123">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-124">Der Datensatzsatz ist vom Typ AAAA und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-125">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="0a380-126">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-127">Beispiel 3: Erstellen eines Eintrags vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="0a380-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="0a380-128">In diesem Beispiel wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-129">Der Datensatzsatz ist vom Typ CNAME und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-130">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="0a380-131">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-132">Beispiel 4: Erstellen eines Eintrags vom Typ MX</span><span class="sxs-lookup"><span data-stu-id="0a380-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="0a380-133">Mit diesem Befehl wird ein RecordSet mit dem Namen "www" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-134">Der Eintragssatz ist vom Typ MX und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-135">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="0a380-136">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-137">Beispiel 5: Erstellen eines Datensatzes vom Typ PTR</span><span class="sxs-lookup"><span data-stu-id="0a380-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="0a380-138">Mit diesem Befehl wird ein RecordSet mit dem Namen 4 in der privaten Zone 3.2.1.in-addr.arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a380-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="0a380-139">Der Datensatzsatz ist vom Typ "PTR" und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-140">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="0a380-141">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-142">Beispiel 6: Erstellen eines RecordSet vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="0a380-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="0a380-143">Dieser Befehl erstellt ein RecordSet namens _sip._tcp in der myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-144">Der Datensatzsatz ist vom Typ SRV und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-145">Sie enthält einen einzelnen privaten DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 zeigt.</span><span class="sxs-lookup"><span data-stu-id="0a380-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="0a380-146">Der Dienst (sip) und das Protokoll (tcp) werden als Teil des Datensatzsatznamens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="0a380-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="0a380-147">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-148">Beispiel 7: Erstellen eines Eintrags vom Typ TXT</span><span class="sxs-lookup"><span data-stu-id="0a380-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="0a380-149">Mit diesem Befehl wird ein "RecordSet"-Benannter Text in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-150">Der Datensatzsatz ist vom Typ TXT und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-151">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0a380-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="0a380-152">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-153">Beispiel 8: Erstellen eines "RecordSet"-Eintrags am Anpunkt der Zone</span><span class="sxs-lookup"><span data-stu-id="0a380-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0a380-154">Mit diesem Befehl wird ein RecordSet an der Spitze (oder Stamm) der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="0a380-155">Dazu wird der Name des Datensatzes als "@" angegeben (einschließlich der doppelten Anführungszeichen).</span><span class="sxs-lookup"><span data-stu-id="0a380-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="0a380-156">Sie können keine #A0 an der Spitze einer Zone erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a380-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="0a380-157">Dies ist eine Einschränkung der DNS-Standards. dies ist keine Einschränkung des privaten Azure-DNS.</span><span class="sxs-lookup"><span data-stu-id="0a380-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="0a380-158">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-159">Beispiel 9: Erstellen eines Platzhalterdatensatzes</span><span class="sxs-lookup"><span data-stu-id="0a380-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0a380-160">Mit diesem Befehl wird ein RecordSet mit dem Namen \* in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-161">Dies ist ein Platzhalterdatensatz.</span><span class="sxs-lookup"><span data-stu-id="0a380-161">This is a wildcard record set.</span></span> <span data-ttu-id="0a380-162">Informationen zum Erstellen eines Datensatzes mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="0a380-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="0a380-163">Beispiel 10: Erstellen eines leeren Datensatzes</span><span class="sxs-lookup"><span data-stu-id="0a380-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="0a380-164">Mit diesem Befehl wird ein RecordSet mit dem Namen \* in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="0a380-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="0a380-165">Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="0a380-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="0a380-166">Dies ist ein leerer Datensatzsatz, der als Platzhalter fungiert, dem Sie später Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="0a380-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="0a380-167">Beispiel 11: Erstellen eines Datensatzes und Unterdrücken aller Bestätigungen</span><span class="sxs-lookup"><span data-stu-id="0a380-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="0a380-168">Mit diesem Befehl wird ein RecordSet erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a380-168">This command creates a RecordSet.</span></span> <span data-ttu-id="0a380-169">Der Parameter "Overwrite" stellt sicher, dass dieser Datensatzsatz alle bereits vorhandenen Datensatzsätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatzsatz gehen verloren).</span><span class="sxs-lookup"><span data-stu-id="0a380-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="0a380-170">Der "Confirm"-Parameter mit dem Wert "$False" unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="0a380-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="0a380-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a380-171">PARAMETERS</span></span>

### <span data-ttu-id="0a380-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a380-172">-DefaultProfile</span></span>
<span data-ttu-id="0a380-173">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a380-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a380-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0a380-174">-Metadata</span></span>
<span data-ttu-id="0a380-175">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a380-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-176">-Name</span><span class="sxs-lookup"><span data-stu-id="0a380-176">-Name</span></span>
<span data-ttu-id="0a380-177">Der Name der Datensätze in diesem Datensatzsatz (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="0a380-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0a380-178">-Overwrite</span></span>
<span data-ttu-id="0a380-179">Führen Sie keinen Fehler aus, wenn der Datensatzsatz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a380-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="0a380-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a380-180">-ParentResourceId</span></span>
<span data-ttu-id="0a380-181">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="0a380-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="0a380-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="0a380-183">Die privaten DNS-Einträge, die Teil dieses Eintragssets sind.</span><span class="sxs-lookup"><span data-stu-id="0a380-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="0a380-184">-RecordType</span></span>
<span data-ttu-id="0a380-185">Der Typ der privaten DNS-Einträge in diesem Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="0a380-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a380-186">-ResourceGroupName</span></span>
<span data-ttu-id="0a380-187">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="0a380-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="0a380-188">-Ttl</span></span>
<span data-ttu-id="0a380-189">Der TTL-Wert aller Datensätze in diesem Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="0a380-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="0a380-190">-Zone</span></span>
<span data-ttu-id="0a380-191">Das PrivateDnsZone-Objekt, das die Zone darstellt, in der der Datensatzsatz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a380-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="0a380-192">-ZoneName</span></span>
<span data-ttu-id="0a380-193">Die Zone, in der der Datensatzsatz erstellt werden soll (ohne endenden Punkt).</span><span class="sxs-lookup"><span data-stu-id="0a380-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a380-194">-Confirm</span></span>
<span data-ttu-id="0a380-195">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a380-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-196">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a380-196">-WhatIf</span></span>
<span data-ttu-id="0a380-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a380-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a380-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a380-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a380-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a380-199">CommonParameters</span></span>
<span data-ttu-id="0a380-200">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a380-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a380-201">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a380-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a380-202">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a380-202">INPUTS</span></span>

### <span data-ttu-id="0a380-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0a380-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="0a380-204">System.String</span><span class="sxs-lookup"><span data-stu-id="0a380-204">System.String</span></span>

## <span data-ttu-id="0a380-205">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a380-205">OUTPUTS</span></span>

### <span data-ttu-id="0a380-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0a380-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="0a380-207">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a380-207">NOTES</span></span>

## <span data-ttu-id="0a380-208">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a380-208">RELATED LINKS</span></span>

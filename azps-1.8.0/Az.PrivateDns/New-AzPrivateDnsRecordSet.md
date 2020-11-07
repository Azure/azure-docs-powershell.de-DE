---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a68848ccf86ab2f2aabc3c9e67cbb00954bcec12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659989"
---
# <span data-ttu-id="de570-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="de570-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="de570-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de570-102">SYNOPSIS</span></span>
<span data-ttu-id="de570-103">Erstellt einen Daten Satz Satz in einer privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="de570-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="de570-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de570-104">SYNTAX</span></span>

### <span data-ttu-id="de570-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="de570-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de570-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="de570-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de570-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de570-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de570-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de570-108">DESCRIPTION</span></span>
<span data-ttu-id="de570-109">Das New-AzPrivateDnsRecordSet-Cmdlet erstellt einen neuen DNS-Daten Satz Satz (Private Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen privaten Zone.</span><span class="sxs-lookup"><span data-stu-id="de570-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="de570-110">Ein Recordset-Objekt ist ein Satz privater DNS-Einträge mit dem gleichen Namen und Typ.</span><span class="sxs-lookup"><span data-stu-id="de570-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="de570-111">Beachten Sie, dass der Name relativ zur privaten Zone und nicht zum vollqualifizierten Namen gehört.</span><span class="sxs-lookup"><span data-stu-id="de570-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="de570-112">Der PrivateDnsRecord-Parameter gibt die Datensätze in der Datensatzgruppe an.</span><span class="sxs-lookup"><span data-stu-id="de570-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="de570-113">Dieser Parameter akzeptiert ein Array privater DNS-Einträge, die mithilfe von New-AzPrivateDnsRecordConfig erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="de570-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="de570-114">Sie können den Pipelineoperator verwenden, um ein PSPrivateDnsZone-Objekt an dieses Cmdlet zu übergeben, oder Sie können ein PSPrivateDnsZone-Objekt als Zone-Parameter übergeben, oder Sie können die Zone anhand der zugehörigen Ressourcenwerte angeben, oder Sie können die Zone auch nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="de570-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="de570-115">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="de570-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="de570-116">Wenn bereits ein übereinstimmendes Recordset vorhanden ist (gleicher Name und Datensatztyp), müssen Sie den Parameter overwrite angeben, andernfalls wird vom Cmdlet kein neues Recordset-Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="de570-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de570-117">EXAMPLES</span></span>

### <span data-ttu-id="de570-118">Beispiel 1: Erstellen eines Recordsets des Typs a</span><span class="sxs-lookup"><span data-stu-id="de570-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="de570-119">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="de570-120">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-121">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="de570-122">Beispiel 2: Erstellen eines Recordsets des Typs AAAA</span><span class="sxs-lookup"><span data-stu-id="de570-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="de570-123">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="de570-124">Der Daten Satz Satz ist vom Typ AAAA und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-125">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="de570-126">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-127">Beispiel 3: Erstellen eines Recordsets vom Typ CNAME</span><span class="sxs-lookup"><span data-stu-id="de570-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="de570-128">In diesem Beispiel wird ein Recordset mit dem Namen www in der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="de570-129">Der Daten Satz Satz ist vom Typ CNAME und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-130">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="de570-131">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-132">Beispiel 4: Erstellen eines Recordsets vom Typ "MX"</span><span class="sxs-lookup"><span data-stu-id="de570-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="de570-133">Mit diesem Befehl wird in der privaten Zone myzone.com ein Recordset mit dem Namen "www" erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="de570-134">Der Daten Satz Satz ist vom Typ MX und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-135">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="de570-136">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-137">Beispiel 5: Erstellen eines Recordsets des Typs PTR</span><span class="sxs-lookup"><span data-stu-id="de570-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="de570-138">Mit diesem Befehl wird ein Recordset mit dem Namen 4 in der privaten Zone 3.2.1.in-addr. arpa erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="de570-139">Der Daten Satz Satz ist vom Typ PTR und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-140">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="de570-141">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-142">Beispiel 6: Erstellen eines Recordsets vom Typ SRV</span><span class="sxs-lookup"><span data-stu-id="de570-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="de570-143">Dieser Befehl erstellt ein Recordset mit dem Namen "_sip. _tcp" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="de570-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="de570-144">Der Daten Satz Satz ist vom Typ SRV und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-145">Sie enthält einen einzelnen privaten DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 verweist.</span><span class="sxs-lookup"><span data-stu-id="de570-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="de570-146">Der Dienst (SIP) und das Protokoll (TCP) werden als Teil des Daten Satz Satz namens und nicht als Teil der Datensatzdaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="de570-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="de570-147">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-148">Beispiel 7: Erstellen eines Recordsets vom Typ txt</span><span class="sxs-lookup"><span data-stu-id="de570-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="de570-149">Dieser Befehl erstellt ein Recordset mit dem Namen "Text" in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="de570-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="de570-150">Der Daten Satz Satz ist vom Typ txt und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-151">Sie enthält einen einzelnen privaten DNS-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="de570-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="de570-152">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-153">Beispiel 8: Erstellen eines Recordsets am Scheitelbereich der Zone</span><span class="sxs-lookup"><span data-stu-id="de570-153">Example 8:  Create a RecordSet at the zone apex</span></span>
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

<span data-ttu-id="de570-154">Mit diesem Befehl wird ein Recordset am Scheitel (oder Stamm) der privaten Zone myzone.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="de570-155">Dazu wird der Name des Daten Satz Satzes als "@" (einschließlich der doppelten Anführungszeichen) angegeben.</span><span class="sxs-lookup"><span data-stu-id="de570-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="de570-156">Sie können keine CNAME-Einträge am Scheitel einer Zone erstellen.</span><span class="sxs-lookup"><span data-stu-id="de570-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="de570-157">Hierbei handelt es sich um eine Einschränkung der DNS-Standards; Es handelt sich nicht um eine Einschränkung von Azure private DNS.</span><span class="sxs-lookup"><span data-stu-id="de570-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="de570-158">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-159">Beispiel 9: Erstellen eines Platzhaltersatz-Datensatzes</span><span class="sxs-lookup"><span data-stu-id="de570-159">Example 9:  Create a wildcard Record Set</span></span>

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

<span data-ttu-id="de570-160">Dieser Befehl erstellt ein Recordset mit dem Namen \* in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="de570-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="de570-161">Hierbei handelt es sich um einen Platzhaltersatz.</span><span class="sxs-lookup"><span data-stu-id="de570-161">This is a wildcard record set.</span></span> <span data-ttu-id="de570-162">Informationen zum Erstellen eines Recordsets mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Daten Satz Satzes mit mehreren Datensätzen finden Sie unter Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="de570-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="de570-163">Beispiel 10: Erstellen eines leeren Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="de570-163">Example 10:  Create an empty Record Set</span></span>

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

<span data-ttu-id="de570-164">Dieser Befehl erstellt ein Recordset mit dem Namen \* in der privaten Zone myzone.com.</span><span class="sxs-lookup"><span data-stu-id="de570-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="de570-165">Der Daten Satz Satz ist vom Typ a und hat einen TTL-Wert von 1 Stunde (3600 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="de570-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="de570-166">Hierbei handelt es sich um einen leeren Daten Satz Satz, der als Platzhalter fungiert, auf den Sie später Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="de570-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="de570-167">Beispiel 11: Erstellen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="de570-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="de570-168">Mit diesem Befehl wird ein Recordset erstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-168">This command creates a RecordSet.</span></span> <span data-ttu-id="de570-169">Der Parameter overwrite stellt sicher, dass dieser Daten Satz Satz alle bereits vorhandenen Daten Satz Sätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatz gehen verloren).</span><span class="sxs-lookup"><span data-stu-id="de570-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="de570-170">Der Confirm-Parameter mit dem Wert $false unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="de570-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="de570-171">Parameter</span><span class="sxs-lookup"><span data-stu-id="de570-171">PARAMETERS</span></span>

### <span data-ttu-id="de570-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de570-172">-DefaultProfile</span></span>
<span data-ttu-id="de570-173">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de570-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de570-174">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="de570-174">-Metadata</span></span>
<span data-ttu-id="de570-175">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="de570-175">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="de570-176">-Name</span><span class="sxs-lookup"><span data-stu-id="de570-176">-Name</span></span>
<span data-ttu-id="de570-177">Der Name der Datensätze in diesem Daten Satz Satz (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="de570-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="de570-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="de570-178">-Overwrite</span></span>
<span data-ttu-id="de570-179">Führen Sie keinen Fehler aus, wenn der Daten Satz Satz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de570-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="de570-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de570-180">-ParentResourceId</span></span>
<span data-ttu-id="de570-181">Private DNS Zone-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="de570-181">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="de570-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="de570-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="de570-183">Die privaten DNS-Einträge, die Teil dieses Daten Satz Satzes sind.</span><span class="sxs-lookup"><span data-stu-id="de570-183">The private dns records that are part of this record set.</span></span>

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

### <span data-ttu-id="de570-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="de570-184">-RecordType</span></span>
<span data-ttu-id="de570-185">Der Typ der privaten DNS-Einträge in diesem Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="de570-185">The type of Private DNS records in this record set.</span></span>

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

### <span data-ttu-id="de570-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de570-186">-ResourceGroupName</span></span>
<span data-ttu-id="de570-187">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="de570-187">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="de570-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="de570-188">-Ttl</span></span>
<span data-ttu-id="de570-189">Der TTL-Wert aller Datensätze in diesem Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="de570-189">The TTL value of all the records in this record set.</span></span>

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

### <span data-ttu-id="de570-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="de570-190">-Zone</span></span>
<span data-ttu-id="de570-191">Das PrivateDnsZone-Objekt, das die Zone darstellt, in der der Daten Satz Satz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="de570-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="de570-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="de570-192">-ZoneName</span></span>
<span data-ttu-id="de570-193">Die Zone, in der die Datensatzgruppe erstellt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="de570-193">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="de570-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de570-194">-Confirm</span></span>
<span data-ttu-id="de570-195">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de570-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de570-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de570-196">-WhatIf</span></span>
<span data-ttu-id="de570-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de570-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de570-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de570-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de570-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de570-199">CommonParameters</span></span>
<span data-ttu-id="de570-200">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de570-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de570-201">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de570-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de570-202">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de570-202">INPUTS</span></span>

### <span data-ttu-id="de570-203">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="de570-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="de570-204">System. String</span><span class="sxs-lookup"><span data-stu-id="de570-204">System.String</span></span>

## <span data-ttu-id="de570-205">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de570-205">OUTPUTS</span></span>

### <span data-ttu-id="de570-206">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="de570-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="de570-207">Notizen</span><span class="sxs-lookup"><span data-stu-id="de570-207">NOTES</span></span>

## <span data-ttu-id="de570-208">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de570-208">RELATED LINKS</span></span>

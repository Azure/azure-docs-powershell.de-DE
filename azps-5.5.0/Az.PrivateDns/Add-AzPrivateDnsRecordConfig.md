---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: a6150f6f54db57abbcd643c99729d41254db7d27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146300"
---
# <span data-ttu-id="109b4-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="109b4-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="109b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="109b4-102">SYNOPSIS</span></span>
<span data-ttu-id="109b4-103">Fügt einem lokalen Datensatzsatzobjekt einen privaten DNS-Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="109b4-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="109b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="109b4-104">SYNTAX</span></span>

### <span data-ttu-id="109b4-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="109b4-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="109b4-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-107">MX</span><span class="sxs-lookup"><span data-stu-id="109b4-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-108">PTR</span><span class="sxs-lookup"><span data-stu-id="109b4-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-109">TXT</span><span class="sxs-lookup"><span data-stu-id="109b4-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-110">SRV</span><span class="sxs-lookup"><span data-stu-id="109b4-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="109b4-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="109b4-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="109b4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="109b4-112">DESCRIPTION</span></span>
<span data-ttu-id="109b4-113">Das Add-AzPrivateDnsRecordConfig cmdlet fügt einem "RecordSet"-Objekt einen Privaten Domain Name System (DNS)-Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="109b4-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="109b4-114">Das Objekt "RecordSet" ist ein Offlineobjekt, und durch Änderungen an diesem Objekt werden die privaten DNS-Antworten erst geändert, nachdem Sie das Cmdlet Set-AzPrivateDnsRecordSet ausgeführt haben, um die Änderung beim privaten Microsoft Azure-DNS-Dienst dauerhaft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="109b4-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="109b4-115">SOA-Einträge werden erstellt, wenn eine private DNS-Zone erstellt wird, und beim Löschen der privaten DNS-Zone entfernt.</span><span class="sxs-lookup"><span data-stu-id="109b4-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="109b4-116">Sie können keine SOA-Einträge hinzufügen oder entfernen, sie aber bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="109b4-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="109b4-117">Sie können das Objekt "RecordSet" als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="109b4-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="109b4-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="109b4-118">EXAMPLES</span></span>

### <span data-ttu-id="109b4-119">Beispiel 1: Hinzufügen eines A-Datensatzes zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="109b4-120">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein A-Datensatz hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="109b4-121">Beispiel 2: Hinzufügen eines AAAA-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="109b4-122">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein AAAAA-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="109b4-123">Beispiel 3: Hinzufügen eines #A0 zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="109b4-124">In diesem Beispiel wird einem vorhandenen Datensatz ein #A0 hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="109b4-125">Beispiel 4: Hinzufügen eines MX-Eintrags zu einem Eintragssatz</span><span class="sxs-lookup"><span data-stu-id="109b4-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="109b4-126">In diesem Beispiel wird einem vorhandenen Eintragssatz ein "MX"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="109b4-127">Beispiel 5: Hinzufügen eines PTR-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="109b4-128">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein PtR-Datensatz hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="109b4-129">Beispiel 6: Hinzufügen eines SRV-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="109b4-130">In diesem Beispiel wird einem vorhandenen Datensatz ein "SRV"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="109b4-131">Beispiel 7: Hinzufügen eines TXT-Eintrags zu einem Datensatzsatz</span><span class="sxs-lookup"><span data-stu-id="109b4-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="109b4-132">In diesem Beispiel wird einem vorhandenen Datensatzsatz ein "TXT"-Eintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="109b4-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="109b4-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="109b4-133">PARAMETERS</span></span>

### <span data-ttu-id="109b4-134">-Cname</span><span class="sxs-lookup"><span data-stu-id="109b4-134">-Cname</span></span>
<span data-ttu-id="109b4-135">Der kanonische Name für den hinzuzufügende CNAME-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="109b4-136">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="109b4-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="109b4-137">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="109b4-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="109b4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109b4-138">-DefaultProfile</span></span>
<span data-ttu-id="109b4-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="109b4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109b4-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="109b4-140">-Exchange</span></span>
<span data-ttu-id="109b4-141">Der E-Mail-Exchange-Host für den hinzuzufügende MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="109b4-142">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="109b4-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="109b4-143">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="109b4-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="109b4-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="109b4-144">-Ipv4Address</span></span>
<span data-ttu-id="109b4-145">Die IPv4-Adresse für den hinzuzufügende A-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="109b4-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="109b4-146">-Ipv6Address</span></span>
<span data-ttu-id="109b4-147">Die IPv6-Adresse für den hinzuzufügende AAAA-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="109b4-148">-Port</span><span class="sxs-lookup"><span data-stu-id="109b4-148">-Port</span></span>
<span data-ttu-id="109b4-149">Die Portnummer für den hinzuzufügende SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="109b4-150">-Preference</span><span class="sxs-lookup"><span data-stu-id="109b4-150">-Preference</span></span>
<span data-ttu-id="109b4-151">Der Einstellungswert für den hinzuzufügende MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="109b4-152">-Priority</span><span class="sxs-lookup"><span data-stu-id="109b4-152">-Priority</span></span>
<span data-ttu-id="109b4-153">Der hinzuzufügende Prioritätswert des SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="109b4-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="109b4-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="109b4-154">-Ptrdname</span></span>
<span data-ttu-id="109b4-155">Der Zielhost für den hinzuzufügende PTR-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="109b4-156">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="109b4-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="109b4-157">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="109b4-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="109b4-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="109b4-158">-RecordSet</span></span>
<span data-ttu-id="109b4-159">Der Datensatzsatz, in dem der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="109b4-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="109b4-160">-Target</span><span class="sxs-lookup"><span data-stu-id="109b4-160">-Target</span></span>
<span data-ttu-id="109b4-161">Der Zielhost für den hinzuzufügende SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="109b4-162">dürfen nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="109b4-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="109b4-163">Dürfen keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="109b4-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="109b4-164">-Value</span><span class="sxs-lookup"><span data-stu-id="109b4-164">-Value</span></span>
<span data-ttu-id="109b4-165">Der Textwert für den hinzuzufügende TXT-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="109b4-166">-Weight</span><span class="sxs-lookup"><span data-stu-id="109b4-166">-Weight</span></span>
<span data-ttu-id="109b4-167">Der Gewichtungswert für den addieren SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="109b4-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="109b4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109b4-168">CommonParameters</span></span>
<span data-ttu-id="109b4-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="109b4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109b4-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="109b4-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109b4-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="109b4-171">INPUTS</span></span>

### <span data-ttu-id="109b4-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="109b4-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="109b4-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="109b4-173">OUTPUTS</span></span>

### <span data-ttu-id="109b4-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="109b4-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="109b4-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="109b4-175">NOTES</span></span>

## <span data-ttu-id="109b4-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="109b4-176">RELATED LINKS</span></span>

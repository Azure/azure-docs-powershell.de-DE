---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: a6150f6f54db57abbcd643c99729d41254db7d27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009599"
---
# <span data-ttu-id="da24f-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="da24f-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="da24f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da24f-102">SYNOPSIS</span></span>
<span data-ttu-id="da24f-103">Fügt einen privaten DNS-Eintrag zu einem lokalen Datensatzobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="da24f-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="da24f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da24f-104">SYNTAX</span></span>

### <span data-ttu-id="da24f-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="da24f-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="da24f-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-107">MX</span><span class="sxs-lookup"><span data-stu-id="da24f-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-108">PTR</span><span class="sxs-lookup"><span data-stu-id="da24f-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-109">TXT</span><span class="sxs-lookup"><span data-stu-id="da24f-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-110">SRV</span><span class="sxs-lookup"><span data-stu-id="da24f-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da24f-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="da24f-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da24f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da24f-112">DESCRIPTION</span></span>
<span data-ttu-id="da24f-113">Mit dem Add-AzPrivateDnsRecordConfig-Cmdlet wird einem Recordset-Objekt ein privater DNS-Eintrag (Domain Name System) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="da24f-114">Das Recordset-Objekt ist ein Offlineobjekt, und Änderungen daran ändern die privaten DNS-Antworten erst, nachdem Sie das Set-AzPrivateDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure private DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="da24f-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="da24f-115">Bei der Erstellung einer privaten DNS-Zone werden SOA-Einträge erstellt, die beim Löschen der privaten DNS-Zone entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="da24f-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="da24f-116">Sie können keine SOA-Einträge hinzufügen oder entfernen, aber Sie können Sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="da24f-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="da24f-117">Sie können das Recordset-Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="da24f-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="da24f-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da24f-118">EXAMPLES</span></span>

### <span data-ttu-id="da24f-119">Beispiel 1: Hinzufügen eines a-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-119">Example 1: Add an A record to a record set</span></span>
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

<span data-ttu-id="da24f-120">In diesem Beispiel wird ein A-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="da24f-121">Beispiel 2: Hinzufügen eines AAAA-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-121">Example 2: Add an AAAA record to a record set</span></span>
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

<span data-ttu-id="da24f-122">In diesem Beispiel wird ein aaaaa-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="da24f-123">Beispiel 3: Hinzufügen eines CNAME-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-123">Example 3: Add a CNAME record to a record set</span></span>
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

<span data-ttu-id="da24f-124">In diesem Beispiel wird ein CNAME-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="da24f-125">Beispiel 4: Hinzufügen eines MX-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-125">Example 4: Add a MX record to a record set</span></span>
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

<span data-ttu-id="da24f-126">In diesem Beispiel wird ein MX-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="da24f-127">Beispiel 5: Hinzufügen eines PTR-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-127">Example 5: Add a PTR record to a record set</span></span>
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

<span data-ttu-id="da24f-128">In diesem Beispiel wird ein PTR-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="da24f-129">Beispiel 6: Hinzufügen eines SRV-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-129">Example 6: Add a SRV record to a record set</span></span>
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

<span data-ttu-id="da24f-130">In diesem Beispiel wird ein SRV-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="da24f-131">Beispiel 7: Hinzufügen eines txt-Eintrags zu einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="da24f-131">Example 7: Add a TXT record to a record set</span></span>
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

<span data-ttu-id="da24f-132">In diesem Beispiel wird ein TXT-Eintrag zu einem vorhandenen Daten Satz Satz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="da24f-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="da24f-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="da24f-133">PARAMETERS</span></span>

### <span data-ttu-id="da24f-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="da24f-134">-Cname</span></span>
<span data-ttu-id="da24f-135">Der kanonische Name für den hinzuzufügenden CNAME-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="da24f-136">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="da24f-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="da24f-137">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="da24f-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="da24f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da24f-138">-DefaultProfile</span></span>
<span data-ttu-id="da24f-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da24f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da24f-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="da24f-140">-Exchange</span></span>
<span data-ttu-id="da24f-141">Der e-Mail-Exchange-Host für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="da24f-142">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="da24f-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="da24f-143">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="da24f-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="da24f-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="da24f-144">-Ipv4Address</span></span>
<span data-ttu-id="da24f-145">Die IPv4-Adresse des hinzuzufügenden A-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="da24f-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="da24f-146">-IPv6</span><span class="sxs-lookup"><span data-stu-id="da24f-146">-Ipv6Address</span></span>
<span data-ttu-id="da24f-147">Die IPv6-Adresse des hinzuzufügenden AAAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="da24f-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="da24f-148">-Port</span><span class="sxs-lookup"><span data-stu-id="da24f-148">-Port</span></span>
<span data-ttu-id="da24f-149">Die Portnummer für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="da24f-150">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="da24f-150">-Preference</span></span>
<span data-ttu-id="da24f-151">Der Einstellungswert für den hinzuzufügenden MX-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="da24f-152">-Priorität</span><span class="sxs-lookup"><span data-stu-id="da24f-152">-Priority</span></span>
<span data-ttu-id="da24f-153">Der hinzuzufügende SRV-Eintrag des Prioritätswerts.</span><span class="sxs-lookup"><span data-stu-id="da24f-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="da24f-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="da24f-154">-Ptrdname</span></span>
<span data-ttu-id="da24f-155">Der Ziel Host für den hinzuzufügenden PTR-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="da24f-156">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="da24f-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="da24f-157">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="da24f-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="da24f-158">-Recordset</span><span class="sxs-lookup"><span data-stu-id="da24f-158">-RecordSet</span></span>
<span data-ttu-id="da24f-159">Die Datensatzgruppe, in der der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da24f-159">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="da24f-160">-Target</span><span class="sxs-lookup"><span data-stu-id="da24f-160">-Target</span></span>
<span data-ttu-id="da24f-161">Der Ziel Host für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="da24f-162">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="da24f-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="da24f-163">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="da24f-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="da24f-164">-Wert</span><span class="sxs-lookup"><span data-stu-id="da24f-164">-Value</span></span>
<span data-ttu-id="da24f-165">Der Textwert für den hinzuzufügenden TXT-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="da24f-166">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="da24f-166">-Weight</span></span>
<span data-ttu-id="da24f-167">Der Gewichtungswert für den hinzuzufügenden SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="da24f-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="da24f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da24f-168">CommonParameters</span></span>
<span data-ttu-id="da24f-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da24f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da24f-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da24f-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da24f-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da24f-171">INPUTS</span></span>

### <span data-ttu-id="da24f-172">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da24f-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="da24f-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da24f-173">OUTPUTS</span></span>

### <span data-ttu-id="da24f-174">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="da24f-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="da24f-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="da24f-175">NOTES</span></span>

## <span data-ttu-id="da24f-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da24f-176">RELATED LINKS</span></span>

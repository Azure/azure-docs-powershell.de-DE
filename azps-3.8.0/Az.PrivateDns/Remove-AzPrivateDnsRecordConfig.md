---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995718"
---
# <span data-ttu-id="fcbfe-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fcbfe-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="fcbfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbfe-103">Entfernt einen privaten DNS-Eintrag aus einem lokalen Datensatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="fcbfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcbfe-104">SYNTAX</span></span>

### <span data-ttu-id="fcbfe-105">A (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcbfe-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="fcbfe-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-107">MX</span><span class="sxs-lookup"><span data-stu-id="fcbfe-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-108">PTR</span><span class="sxs-lookup"><span data-stu-id="fcbfe-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-109">TXT</span><span class="sxs-lookup"><span data-stu-id="fcbfe-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-110">SRV</span><span class="sxs-lookup"><span data-stu-id="fcbfe-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbfe-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="fcbfe-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbfe-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcbfe-112">DESCRIPTION</span></span>
<span data-ttu-id="fcbfe-113">Das Remove-AzPrivateDnsRecordConfig-Cmdlet entfernt einen privaten DNS-Eintrag (Domain Name System) aus einem Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="fcbfe-114">Das Recordset-Objekt ist ein Offlineobjekt, und Änderungen daran ändern die privaten DNS-Antworten erst, nachdem Sie das Set-AzPrivateDnsRecordSet-Cmdlet ausgeführt haben, um die Änderung am Microsoft Azure private DNS-Dienst beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="fcbfe-115">Zum Entfernen eines Datensatzes müssen alle Felder für diesen Datensatztyp genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="fcbfe-116">Sie können keine SOA-Einträge hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="fcbfe-117">SOA-Einträge werden automatisch erstellt, wenn eine private DNS-Zone erstellt und automatisch gelöscht wird, wenn die private DNS-Zone gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="fcbfe-118">Sie können das Recordset-Objekt als Parameter oder mithilfe des Pipelineoperators an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="fcbfe-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcbfe-119">EXAMPLES</span></span>

### <span data-ttu-id="fcbfe-120">Beispiel 1: Entfernen eines a-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-121">In diesem Beispiel wird ein A-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="fcbfe-122">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="fcbfe-123">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="fcbfe-124">Beispiel 2: Entfernen eines AAAA-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-125">In diesem Beispiel wird ein AAAA-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="fcbfe-126">Wenn es sich um den einzigen Datensatz in der Datensatzgruppe handelt, handelt es sich bei dem Ergebnis um einen leeren Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="fcbfe-127">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="fcbfe-128">Beispiel 3: Entfernen eines CNAME-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-129">In diesem Beispiel wird ein CNAME-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="fcbfe-130">Da ein CNAME-Eintragssatz höchstens einen Datensatz enthalten kann, ist das Ergebnis ein leerer Datensatz.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="fcbfe-131">Beispiel 4: Entfernen eines MX-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-132">In diesem Beispiel wird ein MX-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="fcbfe-133">Der Datensatzname "@" steht für einen Datensatz, der in der Zone Apex festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="fcbfe-134">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="fcbfe-135">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="fcbfe-136">Beispiel 5: Entfernen eines PTR-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-137">In diesem Beispiel wird ein PTR-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="fcbfe-138">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="fcbfe-139">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="fcbfe-140">Beispiel 6: Entfernen eines SRV-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-141">In diesem Beispiel wird ein SRV-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="fcbfe-142">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="fcbfe-143">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="fcbfe-144">Beispiel 7: Entfernen eines txt-Eintrags aus einem Daten Satz Satz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="fcbfe-145">In diesem Beispiel wird ein TXT-Eintrag aus einem vorhandenen Daten Satz Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="fcbfe-146">Wenn dies der einzige Datensatz in der Datensatzgruppe ist, ist das Ergebnis eine leere Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="fcbfe-147">Informationen zum vollständigen Entfernen eines Daten Satz Satzes finden Sie unter Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="fcbfe-148">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcbfe-148">PARAMETERS</span></span>

### <span data-ttu-id="fcbfe-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="fcbfe-149">-Cname</span></span>
<span data-ttu-id="fcbfe-150">Der kanonische Name des zu entfernenden CNAME-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="fcbfe-151">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fcbfe-152">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fcbfe-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbfe-153">-DefaultProfile</span></span>
<span data-ttu-id="fcbfe-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcbfe-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="fcbfe-155">-Exchange</span></span>
<span data-ttu-id="fcbfe-156">Der e-Mail-Exchange-Host des zu entfernenden MX-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="fcbfe-157">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fcbfe-158">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fcbfe-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="fcbfe-159">-Ipv4Address</span></span>
<span data-ttu-id="fcbfe-160">Die IPv4-Adresse des zu entfernenden A-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-161">-IPv6</span><span class="sxs-lookup"><span data-stu-id="fcbfe-161">-Ipv6Address</span></span>
<span data-ttu-id="fcbfe-162">Die IPv6-Adresse des zu entfernenden AAAA-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-163">-Port</span><span class="sxs-lookup"><span data-stu-id="fcbfe-163">-Port</span></span>
<span data-ttu-id="fcbfe-164">Die Portnummer des zu entfernenden SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-165">-Präferenz</span><span class="sxs-lookup"><span data-stu-id="fcbfe-165">-Preference</span></span>
<span data-ttu-id="fcbfe-166">Der Einstellungswert des zu entfernenden MX-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-167">-Priorität</span><span class="sxs-lookup"><span data-stu-id="fcbfe-167">-Priority</span></span>
<span data-ttu-id="fcbfe-168">Der Prioritätswert des zu entfernenden SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="fcbfe-169">-Ptrdname</span></span>
<span data-ttu-id="fcbfe-170">Der Ziel Host des zu entfernenden PTR-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="fcbfe-171">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fcbfe-172">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fcbfe-173">-Recordset</span><span class="sxs-lookup"><span data-stu-id="fcbfe-173">-RecordSet</span></span>
<span data-ttu-id="fcbfe-174">Die Datensatzgruppe, aus der der Datensatz entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="fcbfe-175">-Target</span><span class="sxs-lookup"><span data-stu-id="fcbfe-175">-Target</span></span>
<span data-ttu-id="fcbfe-176">Der Ziel Host des zu entfernenden SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="fcbfe-177">Darf nicht relativ zum Namen der Zone sein.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fcbfe-178">Darf keinen Endpunkt haben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fcbfe-179">-Wert</span><span class="sxs-lookup"><span data-stu-id="fcbfe-179">-Value</span></span>
<span data-ttu-id="fcbfe-180">Der Textwert des zu entfernenden txt-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-181">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="fcbfe-181">-Weight</span></span>
<span data-ttu-id="fcbfe-182">Der Gewichtungswert des zu entfernenden SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="fcbfe-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbfe-183">CommonParameters</span></span>
<span data-ttu-id="fcbfe-184">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcbfe-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbfe-185">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbfe-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbfe-186">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-186">INPUTS</span></span>

### <span data-ttu-id="fcbfe-187">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fcbfe-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="fcbfe-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcbfe-188">OUTPUTS</span></span>

### <span data-ttu-id="fcbfe-189">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fcbfe-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="fcbfe-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcbfe-190">NOTES</span></span>

## <span data-ttu-id="fcbfe-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcbfe-191">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a0b527a0931c5c3423e5e64bad0abb7128fc3497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824524"
---
# <span data-ttu-id="68ce0-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68ce0-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="68ce0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="68ce0-103">Ruft einen Daten Satz Satz aus einer privaten DNS-Zone ab.</span><span class="sxs-lookup"><span data-stu-id="68ce0-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="68ce0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ce0-104">SYNTAX</span></span>

### <span data-ttu-id="68ce0-105">FieldsWithNoName (Standard)</span><span class="sxs-lookup"><span data-stu-id="68ce0-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ce0-106">Felder</span><span class="sxs-lookup"><span data-stu-id="68ce0-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ce0-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="68ce0-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ce0-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="68ce0-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ce0-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68ce0-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ce0-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="68ce0-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68ce0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68ce0-111">DESCRIPTION</span></span>
<span data-ttu-id="68ce0-112">Das Get-AzPrivateDnsRecordSet-Cmdlet ruft den privaten DNS-Eintragssatz (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen privaten Zone ab.</span><span class="sxs-lookup"><span data-stu-id="68ce0-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="68ce0-113">Wenn Sie die Parameter Name oder RecordType nicht angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Typs in der privaten Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="68ce0-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="68ce0-114">Wenn Sie den Parameter RecordType, aber nicht den Parameter Name angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Datensatztyps zurück.</span><span class="sxs-lookup"><span data-stu-id="68ce0-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="68ce0-115">Sie können den Pipelineoperator verwenden, um ein PSPrivateDnsZone-Objekt an dieses Cmdlet zu übergeben, oder Sie können ein PSPrivateDnsZone-Objekt als Zone-Parameter übergeben, oder Alternativ können Sie die Zone und die Ressourcengruppe nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="68ce0-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="68ce0-116">Sie können auch die Private Zone mithilfe der Ressourcen-ID der privaten Zone angeben.</span><span class="sxs-lookup"><span data-stu-id="68ce0-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="68ce0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68ce0-117">EXAMPLES</span></span>

### <span data-ttu-id="68ce0-118">Beispiel 1: Abrufen von Daten Satz Sätzen mit einem angegebenen Namen und Typ</span><span class="sxs-lookup"><span data-stu-id="68ce0-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="68ce0-119">Dieser Befehl ruft den Datensatz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und privaten Zone ab und speichert ihn dann in der $Recordset Variablen.</span><span class="sxs-lookup"><span data-stu-id="68ce0-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="68ce0-120">Da die Parameter Name und RecordType angegeben werden, wird nur ein Recordset-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68ce0-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="68ce0-121">Beispiel 2: Abrufen von Daten Satz Sätzen eines angegebenen Typs</span><span class="sxs-lookup"><span data-stu-id="68ce0-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="68ce0-122">Dieser Befehl ruft ein Array aller Daten Satz Sätze des Datensatztyps A in der privaten Zone mit dem Namen "MyZone.com" in der Ressourcengruppe "myresourcegroup" ab und speichert Sie dann in der $Recordsets Variablen.</span><span class="sxs-lookup"><span data-stu-id="68ce0-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="68ce0-123">Beispiel 3: Abrufen aller Daten Satz Sätze in einer privaten Zone</span><span class="sxs-lookup"><span data-stu-id="68ce0-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="68ce0-124">Dieser Befehl ruft ein Array aller Datensatzgruppen in der privaten Zone mit dem Namen "MyZone.com" in der Ressourcengruppe "myresourcegroup" ab und speichert Sie dann in der $Recordsets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="68ce0-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="68ce0-125">Beispiel 4: Abrufen aller Daten Satz Sätze in einer privaten Zone mithilfe eines PSPrivateDnsZone-Objekts</span><span class="sxs-lookup"><span data-stu-id="68ce0-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="68ce0-126">Dieses Beispiel entspricht Beispiel 3 oben.</span><span class="sxs-lookup"><span data-stu-id="68ce0-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="68ce0-127">Dieses Mal wird die Private Zone mithilfe eines privaten Zone-Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="68ce0-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="68ce0-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ce0-128">PARAMETERS</span></span>

### <span data-ttu-id="68ce0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ce0-129">-DefaultProfile</span></span>
<span data-ttu-id="68ce0-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68ce0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ce0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="68ce0-131">-Name</span></span>
<span data-ttu-id="68ce0-132">Der Name der Datensätze in diesem Daten Satz Satz (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="68ce0-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="68ce0-133">-ParentResourceId</span></span>
<span data-ttu-id="68ce0-134">Private DNS Zone-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="68ce0-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="68ce0-135">-RecordType</span></span>
<span data-ttu-id="68ce0-136">Der Typ der DNS-Einträge in diesem Daten Satz Satz.</span><span class="sxs-lookup"><span data-stu-id="68ce0-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ce0-137">-ResourceGroupName</span></span>
<span data-ttu-id="68ce0-138">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="68ce0-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="68ce0-139">-Zone</span></span>
<span data-ttu-id="68ce0-140">Das dnsZone-Objekt, das die Zone darstellt, in der der Daten Satz Satz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ce0-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="68ce0-141">-ZoneName</span></span>
<span data-ttu-id="68ce0-142">Die Zone, in der die Datensatzgruppe erstellt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="68ce0-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ce0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ce0-143">CommonParameters</span></span>
<span data-ttu-id="68ce0-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ce0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ce0-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ce0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ce0-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68ce0-146">INPUTS</span></span>

### <span data-ttu-id="68ce0-147">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68ce0-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="68ce0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="68ce0-148">System.String</span></span>

## <span data-ttu-id="68ce0-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68ce0-149">OUTPUTS</span></span>

### <span data-ttu-id="68ce0-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68ce0-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="68ce0-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="68ce0-151">NOTES</span></span>

## <span data-ttu-id="68ce0-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68ce0-152">RELATED LINKS</span></span>

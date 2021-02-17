---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169369"
---
# <span data-ttu-id="5c928-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5c928-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5c928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c928-102">SYNOPSIS</span></span>
<span data-ttu-id="5c928-103">Ruft einen Eintragssatz aus einer privaten DNS-Zone ab.</span><span class="sxs-lookup"><span data-stu-id="5c928-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="5c928-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c928-104">SYNTAX</span></span>

### <span data-ttu-id="5c928-105">FieldsWithNoName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c928-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c928-106">Felder</span><span class="sxs-lookup"><span data-stu-id="5c928-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c928-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="5c928-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c928-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="5c928-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c928-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c928-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c928-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="5c928-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c928-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c928-111">DESCRIPTION</span></span>
<span data-ttu-id="5c928-112">Das Get-AzPrivateDnsRecordSet-Cmdlet ruft den mit dem angegebenen Namen und Typ festgelegten DNS (Private Domain Name System)-Eintrag in der angegebenen privaten Zone ab.</span><span class="sxs-lookup"><span data-stu-id="5c928-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="5c928-113">Wenn Sie die Parameter "Name" oder "RecordType" nicht angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Typs in der privaten Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="5c928-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="5c928-114">Wenn Sie den Parameter "RecordType", aber nicht den Parameter "Name" angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Datensatztyps zurück.</span><span class="sxs-lookup"><span data-stu-id="5c928-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="5c928-115">Sie können den Pipelineoperator verwenden, um ein "PSPrivateDnsZone"-Objekt an dieses Cmdlet zu übergeben, oder Sie können ein "PSPrivateDnsZone"-Objekt als Zonenparameter übergeben, oder Sie können die Zone und Ressourcengruppe auch nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="5c928-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="5c928-116">Sie können die private Zone auch mit der Ressourcen-ID der privaten Zone angeben.</span><span class="sxs-lookup"><span data-stu-id="5c928-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="5c928-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c928-117">EXAMPLES</span></span>

### <span data-ttu-id="5c928-118">Beispiel 1: Erhalten von Datensatzsätzen mit einem angegebenen Namen und Typ</span><span class="sxs-lookup"><span data-stu-id="5c928-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="5c928-119">Dieser Befehl ruft den Datensatzsatz des Datensatztyps A mit dem Namen "www" in der angegebenen Ressourcengruppe und privaten Zone ab und speichert ihn dann in der $RecordSet Variable.</span><span class="sxs-lookup"><span data-stu-id="5c928-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="5c928-120">Da die Parameter "Name" und "RecordType" angegeben werden, wird nur ein "RecordSet"-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c928-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="5c928-121">Beispiel 2: Erhalten von Datensatzgruppen eines angegebenen Typs</span><span class="sxs-lookup"><span data-stu-id="5c928-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="5c928-122">Dieser Befehl ruft ein Array aller Datensatzgruppen des Datensatztyps A in der privaten Zone namens myzone.com in der Ressourcengruppe namens "MyResourceGroup" ab und speichert sie dann in der $RecordSets Variable.</span><span class="sxs-lookup"><span data-stu-id="5c928-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="5c928-123">Beispiel 3: Alle Datensatzsätze in einer privaten Zone erhalten</span><span class="sxs-lookup"><span data-stu-id="5c928-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="5c928-124">Dieser Befehl ruft ein Array aller Datensatzsätze in der privaten Zone namens myzone.com in der Ressourcengruppe namens "MyResourceGroup" ab und speichert sie dann in der $RecordSets Variable.</span><span class="sxs-lookup"><span data-stu-id="5c928-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="5c928-125">Beispiel 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span><span class="sxs-lookup"><span data-stu-id="5c928-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="5c928-126">Dieses Beispiel entspricht Beispiel 3 oben.</span><span class="sxs-lookup"><span data-stu-id="5c928-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="5c928-127">Dieses Mal wird die private Zone mit einem Objekt der privaten Zone angegeben.</span><span class="sxs-lookup"><span data-stu-id="5c928-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="5c928-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c928-128">PARAMETERS</span></span>

### <span data-ttu-id="5c928-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c928-129">-DefaultProfile</span></span>
<span data-ttu-id="5c928-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c928-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c928-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5c928-131">-Name</span></span>
<span data-ttu-id="5c928-132">Der Name der Datensätze in diesem Datensatzsatz (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="5c928-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="5c928-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5c928-133">-ParentResourceId</span></span>
<span data-ttu-id="5c928-134">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="5c928-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="5c928-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="5c928-135">-RecordType</span></span>
<span data-ttu-id="5c928-136">Der Typ der DNS-Einträge in diesem Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="5c928-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="5c928-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c928-137">-ResourceGroupName</span></span>
<span data-ttu-id="5c928-138">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="5c928-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="5c928-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="5c928-139">-Zone</span></span>
<span data-ttu-id="5c928-140">Das DnsZone-Objekt, das die Zone darstellt, in der der Eintragssatz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c928-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="5c928-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5c928-141">-ZoneName</span></span>
<span data-ttu-id="5c928-142">Die Zone, in der der Datensatzsatz erstellt werden soll (ohne endenden Punkt).</span><span class="sxs-lookup"><span data-stu-id="5c928-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="5c928-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c928-143">CommonParameters</span></span>
<span data-ttu-id="5c928-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c928-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c928-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c928-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c928-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c928-146">INPUTS</span></span>

### <span data-ttu-id="5c928-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5c928-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="5c928-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5c928-148">System.String</span></span>

## <span data-ttu-id="5c928-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c928-149">OUTPUTS</span></span>

### <span data-ttu-id="5c928-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5c928-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5c928-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c928-151">NOTES</span></span>

## <span data-ttu-id="5c928-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c928-152">RELATED LINKS</span></span>

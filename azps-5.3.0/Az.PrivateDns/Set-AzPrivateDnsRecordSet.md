---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459748"
---
# <span data-ttu-id="d8245-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d8245-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d8245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8245-102">SYNOPSIS</span></span>
<span data-ttu-id="d8245-103">Aktualisiert/legt einen Datensatzsatz in einer privaten DNS-Zone fest.</span><span class="sxs-lookup"><span data-stu-id="d8245-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="d8245-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8245-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8245-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8245-105">DESCRIPTION</span></span>
<span data-ttu-id="d8245-106">Das Set-AzPrivateDnsRecordSet cmdlet aktualisiert einen Datensatzsatz im Azure Private DNS-Dienst von einem lokalen RecordSet-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d8245-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="d8245-107">Sie können ein "RecordSet"-Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="d8245-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="d8245-108">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d8245-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d8245-109">Der Datensatzsatz wird nicht aktualisiert, wenn er seit dem Abrufen des lokalen "RecordSet"-Objekts in Azure Private DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8245-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="d8245-110">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="d8245-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="d8245-111">Sie können dieses Verhalten mit dem Parameter "Overwrite" unterdrücken, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d8245-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d8245-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8245-112">EXAMPLES</span></span>

### <span data-ttu-id="d8245-113">Beispiel 1: Aktualisieren eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="d8245-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d8245-114">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variable.</span><span class="sxs-lookup"><span data-stu-id="d8245-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d8245-115">Der zweite und dritte Befehl sind Off-Line-Vorgänge, um dem Datensatzsatz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d8245-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="d8245-116">Der letzte Befehl verwendet das Set-AzPrivateDnsRecordSet cmdlet, um das Update zu commiten.</span><span class="sxs-lookup"><span data-stu-id="d8245-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="d8245-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="d8245-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d8245-118">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variable.</span><span class="sxs-lookup"><span data-stu-id="d8245-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d8245-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d8245-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="d8245-120">Der letzte Befehl verwendet das Set-AzPrivateDnsRecordSet Cmdlet, um das Update in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d8245-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d8245-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8245-121">PARAMETERS</span></span>

### <span data-ttu-id="d8245-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8245-122">-DefaultProfile</span></span>
<span data-ttu-id="d8245-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8245-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8245-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d8245-124">-Overwrite</span></span>
<span data-ttu-id="d8245-125">Verwenden Sie das Feld "ETag" des Parameters "RecordSet" nicht für optimistische Parallelitätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="d8245-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="d8245-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d8245-126">-RecordSet</span></span>
<span data-ttu-id="d8245-127">Der Datensatzsatz, in dem der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8245-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="d8245-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8245-128">-Confirm</span></span>
<span data-ttu-id="d8245-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8245-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8245-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d8245-130">-WhatIf</span></span>
<span data-ttu-id="d8245-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8245-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8245-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8245-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8245-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8245-133">CommonParameters</span></span>
<span data-ttu-id="d8245-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8245-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8245-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8245-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8245-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8245-136">INPUTS</span></span>

### <span data-ttu-id="d8245-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d8245-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d8245-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8245-138">OUTPUTS</span></span>

### <span data-ttu-id="d8245-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d8245-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d8245-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8245-140">NOTES</span></span>

## <span data-ttu-id="d8245-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8245-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 68e55ae6a0c563ecc72e74fc127360ddb35f73f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936123"
---
# <span data-ttu-id="ca6af-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca6af-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ca6af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca6af-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6af-103">Aktualisiert/Legt einen Datensatzsatz in einer privaten DNS-Zone fest.</span><span class="sxs-lookup"><span data-stu-id="ca6af-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="ca6af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca6af-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca6af-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6af-106">Das Set-AzPrivateDnsRecordSet-Cmdlet aktualisiert einen Datensatzsatz im Azure Private DNS-Dienst aus einem lokalen RecordSet-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ca6af-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="ca6af-107">Sie können ein RecordSet-Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="ca6af-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="ca6af-108">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ca6af-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="ca6af-109">Der Datensatzsatz wird nicht aktualisiert, wenn er seit dem Abrufen des lokalen RecordSet-Objekts in Azure Private DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca6af-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="ca6af-110">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="ca6af-111">Sie können dieses Verhalten mit dem Parameter Überschreiben unterdrücken, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ca6af-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ca6af-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca6af-112">EXAMPLES</span></span>

### <span data-ttu-id="ca6af-113">Beispiel 1: Aktualisieren eines Datensatzsatzs</span><span class="sxs-lookup"><span data-stu-id="ca6af-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="ca6af-114">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ca6af-115">Der zweite und dritte Befehl sind off-line-Vorgänge, um dem Datensatzsatz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="ca6af-116">Der letzte Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update zu commiten.</span><span class="sxs-lookup"><span data-stu-id="ca6af-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="ca6af-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="ca6af-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="ca6af-118">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ca6af-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ca6af-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="ca6af-120">Der letzte Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ca6af-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ca6af-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ca6af-121">PARAMETERS</span></span>

### <span data-ttu-id="ca6af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6af-122">-DefaultProfile</span></span>
<span data-ttu-id="ca6af-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca6af-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca6af-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ca6af-124">-Overwrite</span></span>
<span data-ttu-id="ca6af-125">Verwenden Sie nicht das ETag-Feld des Parameters RecordSet für optimistische Parallelitätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="ca6af-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ca6af-126">-RecordSet</span></span>
<span data-ttu-id="ca6af-127">Der Datensatzsatz, in dem der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca6af-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="ca6af-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca6af-128">-Confirm</span></span>
<span data-ttu-id="ca6af-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca6af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca6af-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6af-130">-WhatIf</span></span>
<span data-ttu-id="ca6af-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca6af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca6af-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca6af-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6af-133">CommonParameters</span></span>
<span data-ttu-id="ca6af-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6af-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6af-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6af-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca6af-136">INPUTS</span></span>

### <span data-ttu-id="ca6af-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca6af-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ca6af-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca6af-138">OUTPUTS</span></span>

### <span data-ttu-id="ca6af-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca6af-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ca6af-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ca6af-140">NOTES</span></span>

## <span data-ttu-id="ca6af-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ca6af-141">RELATED LINKS</span></span>

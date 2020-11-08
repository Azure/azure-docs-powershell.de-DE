---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995707"
---
# <span data-ttu-id="7bb5a-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7bb5a-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="7bb5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb5a-103">Aktualisiert/legt einen Daten Satz Satz in einer privaten DNS-Zone fest.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="7bb5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb5a-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bb5a-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb5a-106">Das Set-AzPrivateDnsRecordSet-Cmdlet aktualisiert einen Daten Satz Satz im Azure private DNS-Dienst von einem lokalen Recordset-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="7bb5a-107">Sie können ein Recordset-Objekt als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="7bb5a-108">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="7bb5a-109">Der Daten Satz Satz wird nicht aktualisiert, wenn er in Azure private DNS geändert wurde, seit das lokale Recordset-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="7bb5a-110">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="7bb5a-111">Sie können dieses Verhalten mithilfe des overwrite-Parameters unterdrücken, wodurch der Daten Satz Satz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="7bb5a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bb5a-112">EXAMPLES</span></span>

### <span data-ttu-id="7bb5a-113">Beispiel 1: Aktualisieren eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="7bb5a-113">Example 1: Update a record set</span></span>
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

<span data-ttu-id="7bb5a-114">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="7bb5a-115">Der zweite und der dritte Befehl sind Offlinevorgänge, um dem Daten Satz Satz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="7bb5a-116">Der endgültige Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="7bb5a-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="7bb5a-117">Example 2: Update an SOA record</span></span>
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

<span data-ttu-id="7bb5a-118">Der erste Befehl verwendet das Get-AzPrivateDnsRecordSet-Cmdlet, um den angegebenen Daten Satz Satz abzurufen, und speichert ihn dann in der Variablen $Recordset.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="7bb5a-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $Recordset.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="7bb5a-120">Der endgültige Befehl verwendet das Set-AzPrivateDnsRecordSet-Cmdlet, um das Update in $Recordset zu propagieren.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="7bb5a-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb5a-121">PARAMETERS</span></span>

### <span data-ttu-id="7bb5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb5a-122">-DefaultProfile</span></span>
<span data-ttu-id="7bb5a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb5a-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7bb5a-124">-Overwrite</span></span>
<span data-ttu-id="7bb5a-125">Verwenden Sie das ETag-Feld des Recordset-Parameters nicht für Prüfungen mit vollständigen Parallelität.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="7bb5a-126">-Recordset</span><span class="sxs-lookup"><span data-stu-id="7bb5a-126">-RecordSet</span></span>
<span data-ttu-id="7bb5a-127">Die Datensatzgruppe, in der der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="7bb5a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bb5a-128">-Confirm</span></span>
<span data-ttu-id="7bb5a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb5a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb5a-130">-WhatIf</span></span>
<span data-ttu-id="7bb5a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb5a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb5a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb5a-133">CommonParameters</span></span>
<span data-ttu-id="7bb5a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb5a-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb5a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb5a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bb5a-136">INPUTS</span></span>

### <span data-ttu-id="7bb5a-137">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7bb5a-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="7bb5a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bb5a-138">OUTPUTS</span></span>

### <span data-ttu-id="7bb5a-139">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7bb5a-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="7bb5a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bb5a-140">NOTES</span></span>

## <span data-ttu-id="7bb5a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bb5a-141">RELATED LINKS</span></span>

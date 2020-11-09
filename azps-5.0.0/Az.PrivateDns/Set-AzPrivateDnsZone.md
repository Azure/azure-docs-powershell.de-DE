---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303394"
---
# <span data-ttu-id="ad4ec-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="ad4ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4ec-103">Aktualisiert eine private DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="ad4ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad4ec-104">SYNTAX</span></span>

### <span data-ttu-id="ad4ec-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad4ec-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad4ec-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad4ec-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad4ec-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="ad4ec-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4ec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad4ec-108">DESCRIPTION</span></span>
<span data-ttu-id="ad4ec-109">Das Cmdlet " **Satz-AzPrivateDnsZone** " aktualisiert eine private DNS-Zone (Domain Name System) dauerhaft aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="ad4ec-110">Sie können ein **PrivateDnsZone** -Objekt mithilfe des *PrivateZone* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch den *Namen* und die *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ad4ec-111">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ad4ec-112">Bei der Angabe der Zone mithilfe eines **PrivateDnsZone** -Objekts (das über den Pipeline-oder *Zone* -Parameter übergeben wird) wird die Zone nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, da das lokale **PrivateDnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze in der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="ad4ec-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="ad4ec-113">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ad4ec-114">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="ad4ec-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad4ec-115">EXAMPLES</span></span>

### <span data-ttu-id="ad4ec-116">Beispiel 1: Aktualisieren einer privaten Zone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="ad4ec-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad4ec-117">PARAMETERS</span></span>

### <span data-ttu-id="ad4ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4ec-118">-DefaultProfile</span></span>
<span data-ttu-id="ad4ec-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ad4ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad4ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ad4ec-120">-Name</span></span>
<span data-ttu-id="ad4ec-121">Gibt den Namen der privaten DNS-Zone an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="ad4ec-122">Sie müssen auch den *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ad4ec-123">Alternativ können Sie die private DNS-Zone mithilfe des *Zone* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ad4ec-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ad4ec-124">-Overwrite</span></span>
<span data-ttu-id="ad4ec-125">Bei der Angabe der Zone mithilfe eines **PrivateDnsZone** -Objekts (das über den Pipeline-oder *Zone* -Parameter übergeben wird) wird die Zone nicht aktualisiert, wenn Sie in Azure DNS geändert wurde, da das lokale **dnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze in der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="ad4ec-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="ad4ec-126">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ad4ec-127">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ec-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-128">-PrivateZone</span></span>
<span data-ttu-id="ad4ec-129">Das zu bestimmende Zonenobjekt.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-129">The zone object to set.</span></span>

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

### <span data-ttu-id="ad4ec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4ec-130">-ResourceGroupName</span></span>
<span data-ttu-id="ad4ec-131">Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="ad4ec-132">Außerdem müssen Sie den Parameter *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="ad4ec-133">Alternativ können Sie die private DNS-Zone mithilfe eines **dnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ad4ec-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ad4ec-134">-ResourceId</span></span>
<span data-ttu-id="ad4ec-135">Private DNS Zone-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="ad4ec-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad4ec-136">-Tag</span></span>
<span data-ttu-id="ad4ec-137">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ad4ec-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad4ec-138">-Confirm</span></span>
<span data-ttu-id="ad4ec-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ec-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4ec-140">-WhatIf</span></span>
<span data-ttu-id="ad4ec-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4ec-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ec-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4ec-143">CommonParameters</span></span>
<span data-ttu-id="ad4ec-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4ec-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4ec-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4ec-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad4ec-146">INPUTS</span></span>

### <span data-ttu-id="ad4ec-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ad4ec-147">System.String</span></span>

### <span data-ttu-id="ad4ec-148">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="ad4ec-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad4ec-149">OUTPUTS</span></span>

### <span data-ttu-id="ad4ec-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="ad4ec-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad4ec-151">NOTES</span></span>

## <span data-ttu-id="ad4ec-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad4ec-152">RELATED LINKS</span></span>

[<span data-ttu-id="ad4ec-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="ad4ec-154">Neu – AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="ad4ec-155">Satz-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ad4ec-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)

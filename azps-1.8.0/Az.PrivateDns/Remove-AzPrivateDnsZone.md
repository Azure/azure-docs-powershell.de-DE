---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659973"
---
# <span data-ttu-id="4105d-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4105d-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="4105d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4105d-102">SYNOPSIS</span></span>
<span data-ttu-id="4105d-103">Entfernt eine private DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4105d-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="4105d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4105d-104">SYNTAX</span></span>

### <span data-ttu-id="4105d-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="4105d-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4105d-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="4105d-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4105d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4105d-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4105d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4105d-108">DESCRIPTION</span></span>
<span data-ttu-id="4105d-109">Das Cmdlet **Remove-AzPrivateDnsZone** löscht endgültig eine Private Domain Name System (DNS)-Zone aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4105d-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="4105d-110">Alle in der Zone enthaltenen Daten Satz Sätze werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4105d-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="4105d-111">Sie können ein **PrivateDnsZone** -Objekt mithilfe des *PrivateZone* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch den *Namen* und die *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4105d-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4105d-112">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="4105d-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4105d-113">Wenn Sie die Zone mithilfe eines **PrivateDnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **PrivateDnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="4105d-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4105d-114">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4105d-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4105d-115">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="4105d-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="4105d-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4105d-116">EXAMPLES</span></span>

### <span data-ttu-id="4105d-117">Beispiel 1: Entfernen einer privaten Zone</span><span class="sxs-lookup"><span data-stu-id="4105d-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4105d-118">Mit diesem Befehl wird die Zone mit dem Namen MyZone.com aus der Ressourcengruppe myresourcegroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="4105d-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4105d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4105d-119">PARAMETERS</span></span>

### <span data-ttu-id="4105d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4105d-120">-DefaultProfile</span></span>
<span data-ttu-id="4105d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4105d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4105d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4105d-122">-Name</span></span>
<span data-ttu-id="4105d-123">Gibt den Namen der privaten DNS-Zone an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4105d-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="4105d-124">Sie müssen auch den *ResourceGroupName* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4105d-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4105d-125">Alternativ können Sie die DNS-Zone mithilfe des *Zone* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="4105d-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4105d-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4105d-126">-Overwrite</span></span>
<span data-ttu-id="4105d-127">Wenn Sie die Zone mithilfe eines **PrivateDnsZone** -Objekts angeben (das über den Pipeline-oder *Zone* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, da das lokale **PrivateDnsZone** -Objekt abgerufen wurde (nur Vorgänge, die direkt in der DNS-Zonen Ressource ausgeführt werden, als Änderungen, Operationen für Daten Satz Sätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="4105d-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4105d-128">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4105d-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4105d-129">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="4105d-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4105d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4105d-130">-PassThru</span></span>
<span data-ttu-id="4105d-131">Wird verwendet, um das Ergebnis (boolescher Wert) des Vorgangs Delete private Zone weiter unten in der Pipeline zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4105d-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="4105d-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="4105d-132">-PrivateZone</span></span>
<span data-ttu-id="4105d-133">Das Private Zone-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4105d-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="4105d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4105d-134">-ResourceGroupName</span></span>
<span data-ttu-id="4105d-135">Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="4105d-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="4105d-136">Außerdem müssen Sie den Parameter *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="4105d-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="4105d-137">Alternativ können Sie die DNS-Zone mithilfe eines **PrivateDnsZone** -Objekts angeben, das entweder über die Pipeline oder den *Zone* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4105d-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4105d-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4105d-138">-ResourceId</span></span>
<span data-ttu-id="4105d-139">Private DNS Zone-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="4105d-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="4105d-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4105d-140">-Confirm</span></span>
<span data-ttu-id="4105d-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4105d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4105d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4105d-142">-WhatIf</span></span>
<span data-ttu-id="4105d-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4105d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4105d-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4105d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4105d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4105d-145">CommonParameters</span></span>
<span data-ttu-id="4105d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4105d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4105d-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4105d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4105d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4105d-148">INPUTS</span></span>

### <span data-ttu-id="4105d-149">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4105d-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="4105d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4105d-150">System.String</span></span>

## <span data-ttu-id="4105d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4105d-151">OUTPUTS</span></span>

### <span data-ttu-id="4105d-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4105d-152">System.Boolean</span></span>

## <span data-ttu-id="4105d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="4105d-153">NOTES</span></span>

## <span data-ttu-id="4105d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4105d-154">RELATED LINKS</span></span>

[<span data-ttu-id="4105d-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4105d-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="4105d-156">Neu – AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4105d-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="4105d-157">Satz-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4105d-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)

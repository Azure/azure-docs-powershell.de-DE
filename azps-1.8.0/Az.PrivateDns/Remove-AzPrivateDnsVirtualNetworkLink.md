---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659977"
---
# <span data-ttu-id="f20a8-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f20a8-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f20a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f20a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f20a8-103">Entfernt einen virtuellen Netzwerk Link aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f20a8-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="f20a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f20a8-104">SYNTAX</span></span>

### <span data-ttu-id="f20a8-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="f20a8-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20a8-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="f20a8-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20a8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f20a8-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f20a8-108">DESCRIPTION</span></span>
<span data-ttu-id="f20a8-109">Mit dem Cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** wird dauerhaft ein privater DNS-Link (Domain Name System) aus einer angegebenen Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f20a8-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="f20a8-110">Sie können ein **PSPrivateDnsVirtualNetworkLink** -Objekt mithilfe des *Link* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *Name* *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f20a8-111">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="f20a8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f20a8-112">Wenn Sie die Verknüpfung mit einem **PSPrivateDnsVirtualNetworkLink** -Objekt angeben (das über den Pipeline-oder *Link* -Parameter übergeben wird), wird der Link nicht gelöscht, wenn er in Azure private DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f20a8-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="f20a8-113">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f20a8-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="f20a8-114">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f20a8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f20a8-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f20a8-115">EXAMPLES</span></span>

### <span data-ttu-id="f20a8-116">Beispiel 1: Entfernen eines Links</span><span class="sxs-lookup"><span data-stu-id="f20a8-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="f20a8-117">Mit diesem Befehl wird der Link MyLink mit Zone myzone.com aus der Ressourcengruppe myresourcegroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="f20a8-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f20a8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f20a8-118">PARAMETERS</span></span>

### <span data-ttu-id="f20a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20a8-119">-DefaultProfile</span></span>
<span data-ttu-id="f20a8-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f20a8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f20a8-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f20a8-121">-InputObject</span></span>
<span data-ttu-id="f20a8-122">Das zu entfernende virtuelle Netzwerk Link-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f20a8-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f20a8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f20a8-123">-Name</span></span>
<span data-ttu-id="f20a8-124">Gibt den Namen des Links an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f20a8-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="f20a8-125">Außerdem müssen Sie den Parameter *ResourceGroupName* und *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="f20a8-126">Sie können den Link auch über den *Link* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f20a8-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f20a8-127">-Overwrite</span></span>
<span data-ttu-id="f20a8-128">Wenn Sie die Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben (das über den Pipeline-oder *Link* -Parameter übergeben wird), wird die Zone nicht gelöscht, wenn Sie in Azure DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f20a8-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="f20a8-129">Dadurch wird der Schutz für gleichzeitige Zonenänderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f20a8-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f20a8-130">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch die Zone unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f20a8-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f20a8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f20a8-131">-PassThru</span></span>
<span data-ttu-id="f20a8-132">Wird verwendet, um das Ergebnis (boolescher Wert) des Vorgangs "virtuellen Netzwerk löschen" weiter unten in der Pipeline zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="f20a8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20a8-133">-ResourceGroupName</span></span>
<span data-ttu-id="f20a8-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="f20a8-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="f20a8-135">Außerdem müssen Sie den Parameter *zonename* und *Name* angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="f20a8-136">Alternativ können Sie die DNS-Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben, das entweder über die Pipeline oder den *Link* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f20a8-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="f20a8-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f20a8-137">-ResourceId</span></span>
<span data-ttu-id="f20a8-138">Gibt die Arm-Ressourcen-ID des Links an.</span><span class="sxs-lookup"><span data-stu-id="f20a8-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="f20a8-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="f20a8-139">-ZoneName</span></span>
<span data-ttu-id="f20a8-140">Gibt den Namen der privaten DNS-Zone an, der der Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f20a8-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="f20a8-141">Außerdem müssen Sie den Parameter *ResourceGroupName* und *Name* angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="f20a8-142">Sie können den Link auch über den *Link* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f20a8-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f20a8-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f20a8-143">-Confirm</span></span>
<span data-ttu-id="f20a8-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f20a8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20a8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20a8-145">-WhatIf</span></span>
<span data-ttu-id="f20a8-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f20a8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20a8-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f20a8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20a8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20a8-148">CommonParameters</span></span>
<span data-ttu-id="f20a8-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f20a8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20a8-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f20a8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20a8-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f20a8-151">INPUTS</span></span>

### <span data-ttu-id="f20a8-152">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f20a8-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="f20a8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f20a8-153">System.String</span></span>

## <span data-ttu-id="f20a8-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f20a8-154">OUTPUTS</span></span>

### <span data-ttu-id="f20a8-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f20a8-155">System.Boolean</span></span>

## <span data-ttu-id="f20a8-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="f20a8-156">NOTES</span></span>

## <span data-ttu-id="f20a8-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f20a8-157">RELATED LINKS</span></span>

[<span data-ttu-id="f20a8-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f20a8-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f20a8-159">Neu – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f20a8-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f20a8-160">Satz-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f20a8-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

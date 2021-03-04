---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925392"
---
# <span data-ttu-id="ccbd8-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ccbd8-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ccbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbd8-103">Entfernt einen virtuellen Netzwerklink aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="ccbd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccbd8-104">SYNTAX</span></span>

### <span data-ttu-id="ccbd8-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccbd8-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbd8-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="ccbd8-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbd8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccbd8-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbd8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccbd8-108">DESCRIPTION</span></span>
<span data-ttu-id="ccbd8-109">Das **Cmdlet Remove-AzPrivateDnsVirtualNetworkLink** löscht dauerhaft einen Link für privates Domain Name System (DNS) aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="ccbd8-110">Sie können ein **PSPrivateDnsVirtualNetworkLink-Objekt** mithilfe des Parameters *Link* oder mithilfe des Pipelineoperators übergeben oder alternativ die Parameter *Name* *ZoneName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ccbd8-111">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ccbd8-112">Wenn Sie den Link mithilfe eines **PSPrivateDnsVirtualNetworkLink-Objekts** angeben (über die Pipeline oder den Linkparameter übergeben), wird der Link nicht gelöscht, wenn er seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** in Azure Private DNS geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="ccbd8-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="ccbd8-113">Dies bietet Schutz für gleichzeitige Zonenänderungen.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="ccbd8-114">Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="ccbd8-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ccbd8-115">EXAMPLES</span></span>

### <span data-ttu-id="ccbd8-116">Beispiel 1: Entfernen eines Links</span><span class="sxs-lookup"><span data-stu-id="ccbd8-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="ccbd8-117">Mit diesem Befehl wird der Link mit dem Namen mylink entfernt, der mit myzone.com der Ressourcengruppe "MyResourceGroup" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ccbd8-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ccbd8-118">PARAMETERS</span></span>

### <span data-ttu-id="ccbd8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbd8-119">-DefaultProfile</span></span>
<span data-ttu-id="ccbd8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ccbd8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccbd8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccbd8-121">-InputObject</span></span>
<span data-ttu-id="ccbd8-122">Das virtuelle Netzwerkverknüpfungsobjekt, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="ccbd8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ccbd8-123">-Name</span></span>
<span data-ttu-id="ccbd8-124">Gibt den Namen des zu löschenden Links an.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="ccbd8-125">Sie müssen auch den *Parameter ResourceGroupName* und *ZoneName* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="ccbd8-126">Alternativ können Sie den Link mit dem Parameter *Link* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="ccbd8-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ccbd8-127">-Overwrite</span></span>
<span data-ttu-id="ccbd8-128">Wenn Sie die Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink-Objekts** (über die Pipeline oder den Link-Parameter übergeben) angeben, wird die Zone nicht gelöscht, wenn sie in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="ccbd8-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="ccbd8-129">Dies bietet Schutz für gleichzeitige Zonenänderungen.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ccbd8-130">Dies kann mit dem Parameter *Überschreiben* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ccbd8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccbd8-131">-PassThru</span></span>
<span data-ttu-id="ccbd8-132">Wird zum Übergeben des Ergebnisses (boolesch) des Vorgangs verwendet, um die virtuelle Netzwerkverbindung weiter unten in der Pipeline zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="ccbd8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbd8-133">-ResourceGroupName</span></span>
<span data-ttu-id="ccbd8-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="ccbd8-135">Sie müssen auch den *Parameter ZoneName* und *Name* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="ccbd8-136">Alternativ können Sie die DNS-Zone mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben, das entweder über die Pipeline oder den *Linkparameter übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="ccbd8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccbd8-137">-ResourceId</span></span>
<span data-ttu-id="ccbd8-138">Gibt die ARM-Ressourcen-ID des Links an.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="ccbd8-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ccbd8-139">-ZoneName</span></span>
<span data-ttu-id="ccbd8-140">Gibt den Namen der privaten DNS-Zone an, der der Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="ccbd8-141">Sie müssen auch den *Parameter ResourceGroupName* und *Name* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="ccbd8-142">Alternativ können Sie den Link mit dem Parameter *Link* angeben.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="ccbd8-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccbd8-143">-Confirm</span></span>
<span data-ttu-id="ccbd8-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbd8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbd8-145">-WhatIf</span></span>
<span data-ttu-id="ccbd8-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbd8-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbd8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbd8-148">CommonParameters</span></span>
<span data-ttu-id="ccbd8-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbd8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbd8-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbd8-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbd8-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ccbd8-151">INPUTS</span></span>

### <span data-ttu-id="ccbd8-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ccbd8-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="ccbd8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ccbd8-153">System.String</span></span>

## <span data-ttu-id="ccbd8-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ccbd8-154">OUTPUTS</span></span>

### <span data-ttu-id="ccbd8-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ccbd8-155">System.Boolean</span></span>

## <span data-ttu-id="ccbd8-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ccbd8-156">NOTES</span></span>

## <span data-ttu-id="ccbd8-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ccbd8-157">RELATED LINKS</span></span>

[<span data-ttu-id="ccbd8-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ccbd8-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ccbd8-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ccbd8-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ccbd8-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ccbd8-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

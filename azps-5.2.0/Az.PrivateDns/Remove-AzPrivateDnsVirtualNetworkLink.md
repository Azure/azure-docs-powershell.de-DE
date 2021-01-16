---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303603"
---
# <span data-ttu-id="f869a-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f869a-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f869a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f869a-102">SYNOPSIS</span></span>
<span data-ttu-id="f869a-103">Entfernt eine virtuelle Netzwerkverknüpfung aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f869a-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="f869a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f869a-104">SYNTAX</span></span>

### <span data-ttu-id="f869a-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="f869a-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f869a-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="f869a-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f869a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f869a-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f869a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f869a-108">DESCRIPTION</span></span>
<span data-ttu-id="f869a-109">Das **Cmdlet "Remove-AzPrivateDnsVirtualNetworkLink"** löscht einen Privaten Domain Name System (DNS)-Link endgültig aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f869a-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="f869a-110">Sie können ein **PSPrivateDnsVirtualNetworkLink-Objekt** mit dem *Parameter "Link"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name* *ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f869a-111">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f869a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f869a-112">Wenn Sie den Link mithilfe eines **PSPrivateDnsVirtualNetworkLink-Objekts** angeben (das über die Pipeline oder den Linkparameter übergeben wird), wird der Link nicht gelöscht, wenn er im privaten Azure-DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="f869a-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="f869a-113">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="f869a-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="f869a-114">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="f869a-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f869a-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f869a-115">EXAMPLES</span></span>

### <span data-ttu-id="f869a-116">Beispiel 1: Entfernen eines Links</span><span class="sxs-lookup"><span data-stu-id="f869a-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="f869a-117">Mit diesem Befehl wird der Link mit dem Namen "mylink" aus der myzone.com "MyResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f869a-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f869a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f869a-118">PARAMETERS</span></span>

### <span data-ttu-id="f869a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f869a-119">-DefaultProfile</span></span>
<span data-ttu-id="f869a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f869a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f869a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f869a-121">-InputObject</span></span>
<span data-ttu-id="f869a-122">Das zu entfernende virtuelle Netzwerkverknüpfungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f869a-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="f869a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f869a-123">-Name</span></span>
<span data-ttu-id="f869a-124">Gibt den Namen des zu löschenden Links an.</span><span class="sxs-lookup"><span data-stu-id="f869a-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="f869a-125">Sie müssen auch den Parameter *"ResourceGroupName"* und *"ZoneName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="f869a-126">Alternativ können Sie den Link mit dem Parameter *"Link"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f869a-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f869a-127">-Overwrite</span></span>
<span data-ttu-id="f869a-128">Wenn Sie die Zone mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben (das über die Pipeline oder den Linkparameter übergeben wird), wird die Zone nicht gelöscht, wenn sie in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="f869a-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="f869a-129">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="f869a-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f869a-130">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="f869a-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f869a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f869a-131">-PassThru</span></span>
<span data-ttu-id="f869a-132">Wird verwendet, um das Ergebnis (boolesch) des Vorgangs weiter unten in der Pipeline zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f869a-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="f869a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f869a-133">-ResourceGroupName</span></span>
<span data-ttu-id="f869a-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="f869a-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="f869a-135">Sie müssen auch den *Parameter "ZoneName"* und *"Name"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="f869a-136">Alternativ können Sie die DNS-Zone mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben, das über die Pipeline oder den Parameter *"Link" übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="f869a-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="f869a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f869a-137">-ResourceId</span></span>
<span data-ttu-id="f869a-138">Gibt die ARM ressourcen-ID des Links an.</span><span class="sxs-lookup"><span data-stu-id="f869a-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="f869a-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="f869a-139">-ZoneName</span></span>
<span data-ttu-id="f869a-140">Gibt den Namen der privaten DNS-Zone an, der der Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f869a-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="f869a-141">Sie müssen auch den Parameter *"ResourceGroupName"* und *"Name"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="f869a-142">Alternativ können Sie den Link mit dem Parameter *"Link"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f869a-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="f869a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f869a-143">-Confirm</span></span>
<span data-ttu-id="f869a-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f869a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f869a-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f869a-145">-WhatIf</span></span>
<span data-ttu-id="f869a-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f869a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f869a-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f869a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f869a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f869a-148">CommonParameters</span></span>
<span data-ttu-id="f869a-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f869a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f869a-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f869a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f869a-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f869a-151">INPUTS</span></span>

### <span data-ttu-id="f869a-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f869a-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="f869a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f869a-153">System.String</span></span>

## <span data-ttu-id="f869a-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f869a-154">OUTPUTS</span></span>

### <span data-ttu-id="f869a-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f869a-155">System.Boolean</span></span>

## <span data-ttu-id="f869a-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f869a-156">NOTES</span></span>

## <span data-ttu-id="f869a-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f869a-157">RELATED LINKS</span></span>

[<span data-ttu-id="f869a-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f869a-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f869a-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f869a-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f869a-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f869a-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

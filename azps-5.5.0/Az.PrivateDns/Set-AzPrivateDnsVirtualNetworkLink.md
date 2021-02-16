---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146249"
---
# <span data-ttu-id="e983a-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e983a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e983a-102">SYNOPSIS</span></span>
<span data-ttu-id="e983a-103">Aktualisiert/legt eine virtuelle Netzwerkverknüpfung fest, die einer privaten Zone und einer Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e983a-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="e983a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e983a-104">SYNTAX</span></span>

### <span data-ttu-id="e983a-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="e983a-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e983a-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="e983a-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e983a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e983a-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e983a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e983a-108">DESCRIPTION</span></span>
<span data-ttu-id="e983a-109">Das **Cmdlet "Set-AzPrivateDnsVirtualNetworkLink"** aktualisiert eine Verknüpfung, die einer Zone aus einer angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e983a-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="e983a-110">Sie können ein **PSPrivateDnsVirtualNetworkLink-Objekt** mit dem *Parameter "Link"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name* *ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e983a-111">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="e983a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e983a-112">Wenn Sie die Zone mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben (das über die Pipeline oder den Linkparameter übergeben wird), wird der Link nicht aktualisiert, wenn er in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="e983a-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="e983a-113">Dies bietet Schutz für gleichzeitige Verknüpfungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="e983a-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="e983a-114">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der den Link unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e983a-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="e983a-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e983a-115">EXAMPLES</span></span>

### <span data-ttu-id="e983a-116">Beispiel 1: Festlegen einer Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="e983a-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="e983a-117">Mit diesem Befehl wird "IsRegistrationEnabled" für den Link namens "mylink", der mit der Zone namens "myzone.com" der Ressourcengruppe "MyResourceGroup" verknüpft ist, auf "True" setzt.</span><span class="sxs-lookup"><span data-stu-id="e983a-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e983a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e983a-118">PARAMETERS</span></span>

### <span data-ttu-id="e983a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e983a-119">-DefaultProfile</span></span>
<span data-ttu-id="e983a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e983a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e983a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e983a-121">-InputObject</span></span>
<span data-ttu-id="e983a-122">Das festgelegte virtuelle Netzwerkverknüpfungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e983a-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="e983a-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="e983a-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="e983a-124">Boolesch, der darstellt, ob die Registrierung für die virtuelle Netzwerkverknüpfung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e983a-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e983a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e983a-125">-Name</span></span>
<span data-ttu-id="e983a-126">Gibt den Namen der Verknüpfung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e983a-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="e983a-127">Sie müssen auch den Parameter *"ResourceGroupName"* und *"ZoneName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="e983a-128">Alternativ können Sie den privaten DNS-Link mithilfe des *Linkparameters* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="e983a-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e983a-129">-Overwrite</span></span>
<span data-ttu-id="e983a-130">Wenn Sie den Link mithilfe eines **PSPrivateDnsVirtualNetworkLink-Objekts** angeben (über die Pipeline oder den Linkparameter übergeben), wird der Link nicht gelöscht, wenn er in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="e983a-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="e983a-131">Dies bietet Schutz für gleichzeitige Verknüpfungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="e983a-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="e983a-132">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, wodurch der Link unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e983a-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e983a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e983a-133">-ResourceGroupName</span></span>
<span data-ttu-id="e983a-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="e983a-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="e983a-135">Sie müssen auch den *Parameter "ZoneName"* und *"Name"* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="e983a-136">Alternativ können Sie den virtuellen Netzwerklink mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben, das über die Pipeline oder den *Linkparameter übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="e983a-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="e983a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e983a-137">-ResourceId</span></span>
<span data-ttu-id="e983a-138">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="e983a-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="e983a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e983a-139">-Tag</span></span>
<span data-ttu-id="e983a-140">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="e983a-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e983a-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="e983a-141">-ZoneName</span></span>
<span data-ttu-id="e983a-142">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e983a-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="e983a-143">Sie müssen auch den Parameter *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e983a-144">Alternativ können Sie den privaten DNS-Link mithilfe des *Linkparameters* angeben.</span><span class="sxs-lookup"><span data-stu-id="e983a-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="e983a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e983a-145">-Confirm</span></span>
<span data-ttu-id="e983a-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e983a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e983a-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e983a-147">-WhatIf</span></span>
<span data-ttu-id="e983a-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e983a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e983a-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e983a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e983a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e983a-150">CommonParameters</span></span>
<span data-ttu-id="e983a-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e983a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e983a-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e983a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e983a-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e983a-153">INPUTS</span></span>

### <span data-ttu-id="e983a-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="e983a-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e983a-155">System.String</span></span>

## <span data-ttu-id="e983a-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e983a-156">OUTPUTS</span></span>

### <span data-ttu-id="e983a-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e983a-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e983a-158">NOTES</span></span>

## <span data-ttu-id="e983a-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e983a-159">RELATED LINKS</span></span>

[<span data-ttu-id="e983a-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e983a-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e983a-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e983a-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

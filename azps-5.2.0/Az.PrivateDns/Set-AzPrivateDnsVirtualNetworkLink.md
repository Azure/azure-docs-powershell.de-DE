---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298976"
---
# <span data-ttu-id="8f352-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="8f352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f352-102">SYNOPSIS</span></span>
<span data-ttu-id="8f352-103">Aktualisiert/legt eine virtuelle Netzwerkverknüpfung fest, die einer privaten Zone und einer Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f352-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="8f352-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f352-104">SYNTAX</span></span>

### <span data-ttu-id="8f352-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f352-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f352-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="8f352-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f352-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f352-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f352-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f352-108">DESCRIPTION</span></span>
<span data-ttu-id="8f352-109">Das **Cmdlet "Set-AzPrivateDnsVirtualNetworkLink"** aktualisiert eine Verknüpfung, die einer Zone aus einer angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f352-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="8f352-110">Sie können ein **PSPrivateDnsVirtualNetworkLink-Objekt** mit dem *Parameter "Link"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name* *ZoneName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8f352-111">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8f352-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8f352-112">Wenn Sie die Zone mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben (das über die Pipeline oder den Linkparameter übergeben wird), wird der Link nicht aktualisiert, wenn er in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="8f352-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="8f352-113">Dies bietet Schutz für gleichzeitige Verknüpfungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="8f352-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="8f352-114">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der den Link unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8f352-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="8f352-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f352-115">EXAMPLES</span></span>

### <span data-ttu-id="8f352-116">Beispiel 1: Festlegen einer Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="8f352-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="8f352-117">Mit diesem Befehl wird "IsRegistrationEnabled" für den Link namens "mylink", der mit der Zone namens "myzone.com aus der Ressourcengruppe "MyResourceGroup" verknüpft ist, auf "True" setzt.</span><span class="sxs-lookup"><span data-stu-id="8f352-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8f352-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f352-118">PARAMETERS</span></span>

### <span data-ttu-id="8f352-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f352-119">-DefaultProfile</span></span>
<span data-ttu-id="8f352-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f352-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f352-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f352-121">-InputObject</span></span>
<span data-ttu-id="8f352-122">Das festgelegte virtuelle Netzwerkverknüpfungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="8f352-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="8f352-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="8f352-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="8f352-124">Boolesch, der darstellt, ob die Registrierung für die virtuelle Netzwerkverknüpfung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8f352-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="8f352-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8f352-125">-Name</span></span>
<span data-ttu-id="8f352-126">Gibt den Namen der Verknüpfung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8f352-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="8f352-127">Sie müssen auch den Parameter *"ResourceGroupName"* und *"ZoneName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="8f352-128">Alternativ können Sie den privaten DNS-Link mithilfe des *Linkparameters* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="8f352-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8f352-129">-Overwrite</span></span>
<span data-ttu-id="8f352-130">Wenn Sie den Link mithilfe eines **PSPrivateDnsVirtualNetworkLink-Objekts** angeben (über die Pipeline oder den Linkparameter übergeben), wird der Link nicht gelöscht, wenn er in Azure DNS seit dem Abrufen des lokalen **PSPrivateDnsVirtualNetworkLink-Objekts** geändert wurde. </span><span class="sxs-lookup"><span data-stu-id="8f352-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="8f352-131">Dies bietet Schutz für gleichzeitige Verknüpfungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="8f352-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="8f352-132">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, wodurch der Link unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8f352-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="8f352-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f352-133">-ResourceGroupName</span></span>
<span data-ttu-id="8f352-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="8f352-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="8f352-135">Sie müssen auch den *Parameter "ZoneName"* und *"Name"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="8f352-136">Alternativ können Sie den virtuellen Netzwerklink mit einem **PSPrivateDnsVirtualNetworkLink-Objekt** angeben, das über die Pipeline oder den *Linkparameter übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="8f352-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="8f352-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f352-137">-ResourceId</span></span>
<span data-ttu-id="8f352-138">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="8f352-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="8f352-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f352-139">-Tag</span></span>
<span data-ttu-id="8f352-140">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f352-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8f352-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="8f352-141">-ZoneName</span></span>
<span data-ttu-id="8f352-142">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8f352-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="8f352-143">Sie müssen auch den Parameter *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="8f352-144">Alternativ können Sie den privaten DNS-Link mithilfe des *Linkparameters* angeben.</span><span class="sxs-lookup"><span data-stu-id="8f352-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="8f352-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f352-145">-Confirm</span></span>
<span data-ttu-id="8f352-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f352-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f352-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f352-147">-WhatIf</span></span>
<span data-ttu-id="8f352-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f352-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f352-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f352-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f352-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f352-150">CommonParameters</span></span>
<span data-ttu-id="8f352-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f352-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f352-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f352-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f352-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f352-153">INPUTS</span></span>

### <span data-ttu-id="8f352-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="8f352-155">System.String</span><span class="sxs-lookup"><span data-stu-id="8f352-155">System.String</span></span>

## <span data-ttu-id="8f352-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f352-156">OUTPUTS</span></span>

### <span data-ttu-id="8f352-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="8f352-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f352-158">NOTES</span></span>

## <span data-ttu-id="8f352-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f352-159">RELATED LINKS</span></span>

[<span data-ttu-id="8f352-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="8f352-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="8f352-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="8f352-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

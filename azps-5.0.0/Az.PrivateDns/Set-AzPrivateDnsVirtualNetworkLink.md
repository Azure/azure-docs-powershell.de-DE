---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301270"
---
# <span data-ttu-id="7f043-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="7f043-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f043-102">SYNOPSIS</span></span>
<span data-ttu-id="7f043-103">Aktualisiert/legt einen virtuellen Netzwerk Link fest, der einer privaten Zone und einer Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7f043-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="7f043-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f043-104">SYNTAX</span></span>

### <span data-ttu-id="7f043-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f043-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f043-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="7f043-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f043-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f043-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f043-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f043-108">DESCRIPTION</span></span>
<span data-ttu-id="7f043-109">Das Cmdlet " **Satz-AzPrivateDnsVirtualNetworkLink** " aktualisiert einen Link, der einer Zone einer bestimmten Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7f043-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="7f043-110">Sie können ein **PSPrivateDnsVirtualNetworkLink** -Objekt mithilfe des *Link* -Parameters oder mithilfe des Pipelineoperators übergeben, oder Sie können auch die Parameter *Name* *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7f043-111">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="7f043-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7f043-112">Wenn Sie die Zone mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben (das über den Pipeline-oder *Link* -Parameter übergeben wird), wird der Link nicht aktualisiert, wenn er in Azure DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7f043-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="7f043-113">Dadurch wird der Schutz für gleichzeitige Link Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7f043-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="7f043-114">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch der Link unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7f043-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="7f043-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f043-115">EXAMPLES</span></span>

### <span data-ttu-id="7f043-116">Beispiel 1: Einrichten eines Links</span><span class="sxs-lookup"><span data-stu-id="7f043-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="7f043-117">Mit diesem Befehl wird IsRegistrationEnabled für den Link "MyLink" auf "true" festgelegt, der mit Zone mit dem Namen MyZone.com aus der Ressourcengruppe "myresourcegroup" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7f043-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7f043-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f043-118">PARAMETERS</span></span>

### <span data-ttu-id="7f043-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f043-119">-DefaultProfile</span></span>
<span data-ttu-id="7f043-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7f043-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f043-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f043-121">-InputObject</span></span>
<span data-ttu-id="7f043-122">Das zu bestimmende virtuelle Netzwerk Link-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f043-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="7f043-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="7f043-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="7f043-124">Boolescher Wert, der darstellt, ob die Registrierung für den virtuellen Netzwerk Link aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7f043-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="7f043-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7f043-125">-Name</span></span>
<span data-ttu-id="7f043-126">Gibt den Namen des Links an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f043-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="7f043-127">Außerdem müssen Sie den Parameter *ResourceGroupName* und *zonename* angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="7f043-128">Alternativ können Sie den privaten DNS-Link über den *Link* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="7f043-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7f043-129">-Overwrite</span></span>
<span data-ttu-id="7f043-130">Wenn Sie die Verknüpfung mit einem **PSPrivateDnsVirtualNetworkLink** -Objekt angeben (über den Pipeline-oder *Link* -Parameter übergeben), wird der Link nicht gelöscht, wenn er in Azure DNS geändert wurde, nachdem das lokale **PSPrivateDnsVirtualNetworkLink** -Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7f043-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="7f043-131">Dadurch wird der Schutz für gleichzeitige Link Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7f043-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="7f043-132">Dies kann mithilfe des *overwrite* -Parameters unterdrückt werden, wodurch der Link unabhängig von gleichzeitigen Änderungen gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7f043-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="7f043-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f043-133">-ResourceGroupName</span></span>
<span data-ttu-id="7f043-134">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Link enthält.</span><span class="sxs-lookup"><span data-stu-id="7f043-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="7f043-135">Außerdem müssen Sie den Parameter *zonename* und *Name* angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="7f043-136">Alternativ können Sie den virtuellen Netzwerk Link mithilfe eines **PSPrivateDnsVirtualNetworkLink** -Objekts angeben, das entweder über die Pipeline oder den *Link* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f043-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="7f043-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f043-137">-ResourceId</span></span>
<span data-ttu-id="7f043-138">Private DNS Zone-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="7f043-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="7f043-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f043-139">-Tag</span></span>
<span data-ttu-id="7f043-140">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f043-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7f043-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="7f043-141">-ZoneName</span></span>
<span data-ttu-id="7f043-142">Gibt den Namen der DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7f043-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="7f043-143">Außerdem müssen Sie den Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7f043-144">Alternativ können Sie den privaten DNS-Link über den *Link* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7f043-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="7f043-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f043-145">-Confirm</span></span>
<span data-ttu-id="7f043-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f043-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f043-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f043-147">-WhatIf</span></span>
<span data-ttu-id="7f043-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f043-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f043-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f043-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f043-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f043-150">CommonParameters</span></span>
<span data-ttu-id="7f043-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f043-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f043-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f043-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f043-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f043-153">INPUTS</span></span>

### <span data-ttu-id="7f043-154">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="7f043-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7f043-155">System.String</span></span>

## <span data-ttu-id="7f043-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f043-156">OUTPUTS</span></span>

### <span data-ttu-id="7f043-157">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="7f043-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f043-158">NOTES</span></span>

## <span data-ttu-id="7f043-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f043-159">RELATED LINKS</span></span>

[<span data-ttu-id="7f043-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="7f043-161">Neu – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="7f043-162">Satz-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="7f043-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

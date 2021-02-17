---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169345"
---
# <span data-ttu-id="b3c90-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b3c90-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="b3c90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c90-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c90-103">Erstellt einen neuen privaten virtuellen DNS-Netzwerklink.</span><span class="sxs-lookup"><span data-stu-id="b3c90-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="b3c90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3c90-104">SYNTAX</span></span>

### <span data-ttu-id="b3c90-105">VirtualNetworkId (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3c90-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="b3c90-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3c90-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b3c90-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3c90-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3c90-108">DESCRIPTION</span></span>
<span data-ttu-id="b3c90-109">Das **Cmdlet "New-AzPrivateDnsVirtualNetworkLink"** erstellt eine neue virtuelle Netzwerkverknüpfung (Private Domain Name System, DNS) in der angegebenen Ressourcengruppe und privaten Zone.</span><span class="sxs-lookup"><span data-stu-id="b3c90-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="b3c90-110">Sie müssen einen eindeutigen Linknamen für den *Parameter "Name" angeben,* da das Cmdlet einen Fehler zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="b3c90-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="b3c90-111">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b3c90-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3c90-112">EXAMPLES</span></span>

### <span data-ttu-id="b3c90-113">Beispiel 1: Erstellen eines links für ein privates dns-virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b3c90-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

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

<span data-ttu-id="b3c90-114">Dieser Befehl erstellt eine neue virtuelle Netzwerkverknüpfung, die der privaten DNS-Zone mit dem Namen myzone.com und dem virtuellen Netzwerk "myvirtualnetwork" (das bereits in der Ressourcengruppe erstellt wurde) in der angegebenen Ressourcengruppe zugeordnet ist, und speichert sie dann in der $Link-Variable.</span><span class="sxs-lookup"><span data-stu-id="b3c90-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="b3c90-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3c90-115">PARAMETERS</span></span>

### <span data-ttu-id="b3c90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c90-116">-DefaultProfile</span></span>
<span data-ttu-id="b3c90-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3c90-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c90-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="b3c90-118">-EnableRegistration</span></span>
<span data-ttu-id="b3c90-119">Parameter wechseln, der darstellt, ob die Registrierung für den Link aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3c90-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="b3c90-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b3c90-120">-Name</span></span>
<span data-ttu-id="b3c90-121">Gibt den Namen der zu erstellenden virtuellen Netzwerkverknüpfung an.</span><span class="sxs-lookup"><span data-stu-id="b3c90-121">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b3c90-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="b3c90-123">Die Ressourcen-ID des virtuellen Netzwerks in einem anderen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="b3c90-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c90-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3c90-125">Gibt die Ressourcengruppe an, in der die Verknüpfung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3c90-125">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3c90-126">-Tag</span></span>
<span data-ttu-id="b3c90-127">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3c90-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b3c90-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3c90-128">-VirtualNetwork</span></span>
<span data-ttu-id="b3c90-129">Das virtuelle Netzwerkobjekt, das dem Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b3c90-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b3c90-130">-VirtualNetworkId</span></span>
<span data-ttu-id="b3c90-131">Die Ressourcen-ID des virtuellen Netzwerks, das dem Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b3c90-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b3c90-132">-ZoneName</span></span>
<span data-ttu-id="b3c90-133">Gibt den Namen der Zone an, die mit der Virtuellen Netzwerkverknüpfung verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="b3c90-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c90-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3c90-134">-Confirm</span></span>
<span data-ttu-id="b3c90-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c90-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3c90-136">-WhatIf</span></span>
<span data-ttu-id="b3c90-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3c90-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3c90-138">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3c90-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3c90-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3c90-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c90-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c90-140">CommonParameters</span></span>
<span data-ttu-id="b3c90-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c90-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c90-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3c90-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c90-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3c90-143">INPUTS</span></span>

### <span data-ttu-id="b3c90-144">Keine</span><span class="sxs-lookup"><span data-stu-id="b3c90-144">None</span></span>

## <span data-ttu-id="b3c90-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3c90-145">OUTPUTS</span></span>

### <span data-ttu-id="b3c90-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b3c90-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="b3c90-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3c90-147">NOTES</span></span>

## <span data-ttu-id="b3c90-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3c90-148">RELATED LINKS</span></span>

[<span data-ttu-id="b3c90-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b3c90-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b3c90-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b3c90-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b3c90-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b3c90-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

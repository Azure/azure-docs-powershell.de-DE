---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 7d2a9a399e6582e2ff3815447570548ac62f6676
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659987"
---
# <span data-ttu-id="1bbeb-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="1bbeb-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="1bbeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bbeb-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbeb-103">Erstellt einen neuen privaten virtuellen DNS-Netzwerk Link.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="1bbeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bbeb-104">SYNTAX</span></span>

### <span data-ttu-id="1bbeb-105">VirtualNetworkId (Standard)</span><span class="sxs-lookup"><span data-stu-id="1bbeb-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbeb-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="1bbeb-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbeb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bbeb-107">DESCRIPTION</span></span>
<span data-ttu-id="1bbeb-108">Das Cmdlet **New-AzPrivateDnsVirtualNetworkLink** erstellt einen neuen privaten DNS-Netzwerk Link (Private Domain Name System) in der angegebenen Ressourcengruppe und privaten Zone.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-108">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="1bbeb-109">Sie müssen einen eindeutigen Verknüpfungsnamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-109">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="1bbeb-110">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-110">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1bbeb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bbeb-111">EXAMPLES</span></span>

### <span data-ttu-id="1bbeb-112">Beispiel 1: Erstellen eines privaten virtuellen DNS-Netzwerk Links</span><span class="sxs-lookup"><span data-stu-id="1bbeb-112">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="1bbeb-113">Dieser Befehl erstellt einen neuen virtuellen Netzwerk Link, der der privaten DNS-Zone mit dem Namen MyZone.com und dem virtuellen Netzwerk "myvirtualnetwork" (das bereits in der Ressourcengruppe erstellt wurde) in der angegebenen Ressourcengruppe zugeordnet ist, und speichert Sie dann in der $Link-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-113">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="1bbeb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bbeb-114">PARAMETERS</span></span>

### <span data-ttu-id="1bbeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbeb-115">-DefaultProfile</span></span>
<span data-ttu-id="1bbeb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1bbeb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bbeb-117">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="1bbeb-117">-EnableRegistration</span></span>
<span data-ttu-id="1bbeb-118">Switch-Parameter, der darstellt, ob der Link Registrierung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-118">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="1bbeb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1bbeb-119">-Name</span></span>
<span data-ttu-id="1bbeb-120">Gibt den Namen des zu erstellendes virtuellen Netzwerk Links an.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-120">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="1bbeb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bbeb-121">-ResourceGroupName</span></span>
<span data-ttu-id="1bbeb-122">Gibt die Ressourcengruppe an, in der der Link erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-122">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="1bbeb-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bbeb-123">-Tag</span></span>
<span data-ttu-id="1bbeb-124">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-124">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1bbeb-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1bbeb-125">-VirtualNetwork</span></span>
<span data-ttu-id="1bbeb-126">Das virtuelle Netzwerkobjekt, das dem Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-126">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="1bbeb-127">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1bbeb-127">-VirtualNetworkId</span></span>
<span data-ttu-id="1bbeb-128">Die Ressourcen-ID des virtuellen Netzwerks, das dem Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-128">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="1bbeb-129">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="1bbeb-129">-ZoneName</span></span>
<span data-ttu-id="1bbeb-130">Gibt den Namen der Zone an, die mit dem virtuellen Netzwerk verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-130">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="1bbeb-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bbeb-131">-Confirm</span></span>
<span data-ttu-id="1bbeb-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbeb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbeb-133">-WhatIf</span></span>
<span data-ttu-id="1bbeb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bbeb-135">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bbeb-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbeb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbeb-137">CommonParameters</span></span>
<span data-ttu-id="1bbeb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bbeb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbeb-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bbeb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbeb-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bbeb-140">INPUTS</span></span>

### <span data-ttu-id="1bbeb-141">Keine</span><span class="sxs-lookup"><span data-stu-id="1bbeb-141">None</span></span>

## <span data-ttu-id="1bbeb-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bbeb-142">OUTPUTS</span></span>

### <span data-ttu-id="1bbeb-143">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="1bbeb-143">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="1bbeb-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bbeb-144">NOTES</span></span>

## <span data-ttu-id="1bbeb-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bbeb-145">RELATED LINKS</span></span>

[<span data-ttu-id="1bbeb-146">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="1bbeb-146">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="1bbeb-147">Satz-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="1bbeb-147">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="1bbeb-148">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="1bbeb-148">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

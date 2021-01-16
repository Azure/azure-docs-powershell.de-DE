---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307331"
---
# <span data-ttu-id="b298e-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b298e-101">New-AzPeering</span></span>

## <span data-ttu-id="b298e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b298e-102">SYNOPSIS</span></span>
<span data-ttu-id="b298e-103">Erstellt ein neues Peering ARM Ressource</span><span class="sxs-lookup"><span data-stu-id="b298e-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="b298e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b298e-104">SYNTAX</span></span>

### <span data-ttu-id="b298e-105">Exchange (Standard)</span><span class="sxs-lookup"><span data-stu-id="b298e-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b298e-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="b298e-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b298e-107">Direkt</span><span class="sxs-lookup"><span data-stu-id="b298e-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b298e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b298e-108">DESCRIPTION</span></span>
<span data-ttu-id="b298e-109">Erstellt ein ARM Peering für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b298e-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="b298e-110">Weitere Informationen zum Erstellen eines Verbindungsobjekts finden Sie unter ["New-AzPeeringDirectConnectionObject"](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) oder ["New-AzPeeringExchangeConnectionObject".](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject)</span><span class="sxs-lookup"><span data-stu-id="b298e-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="b298e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b298e-111">EXAMPLES</span></span>

### <span data-ttu-id="b298e-112">Erstellen eines neuen direkten Peerings</span><span class="sxs-lookup"><span data-stu-id="b298e-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="b298e-113">Erstellen eines neuen direkten Peerings mit einer einzelnen Verbindung in der Einrichtung in Seattle mithilfe von PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="b298e-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="b298e-114">Erstellen eines neuen Exchange-Peerings</span><span class="sxs-lookup"><span data-stu-id="b298e-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="b298e-115">Erstellen eines neuen Exchange-Peerings</span><span class="sxs-lookup"><span data-stu-id="b298e-115">Create a new exchange peering</span></span>

### <span data-ttu-id="b298e-116">Konvertieren von älterem Peering in ARM Peering</span><span class="sxs-lookup"><span data-stu-id="b298e-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="b298e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b298e-117">PARAMETERS</span></span>

### <span data-ttu-id="b298e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b298e-118">-AsJob</span></span>
<span data-ttu-id="b298e-119">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b298e-119">Run in the background.</span></span>

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

### <span data-ttu-id="b298e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b298e-120">-DefaultProfile</span></span>
<span data-ttu-id="b298e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b298e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b298e-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="b298e-122">-DirectConnection</span></span>
<span data-ttu-id="b298e-123">Erstellen Sie neue direkte Verbindungen, indem Sie New-AzExchangePeeringConnection und das Pipe zu diesem Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="b298e-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b298e-124">-ExchangeConnection</span></span>
<span data-ttu-id="b298e-125">Erstellen Sie neue Exchange-Verbindungen, indem Sie New-AzExchangePeeringConnection und das Pipe an diesen Befehl weiter ausführen.</span><span class="sxs-lookup"><span data-stu-id="b298e-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b298e-126">-InputObject</span></span>
<span data-ttu-id="b298e-127">Verwenden sie Get-AzLegacyPeering, um dieses Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b298e-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="b298e-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="b298e-129">Wählen Sie das Microsoft-Netzwerk aus, mit dem Sie peeren möchten.</span><span class="sxs-lookup"><span data-stu-id="b298e-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b298e-130">-Name</span></span>
<span data-ttu-id="b298e-131">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b298e-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="b298e-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="b298e-133">Die Peer-Asn-Ressourcen-ID. Verwenden Sie Get-AzPeerAsn, um die ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b298e-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b298e-134">-PeeringLocation</span></span>
<span data-ttu-id="b298e-135">Der physische Standort ist anders als in der Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="b298e-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="b298e-136">Verwenden Get-AzPeeringLocation "-Kind" \<kind\> den Namen "Ort" als Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b298e-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b298e-137">-ResourceGroupName</span></span>
<span data-ttu-id="b298e-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b298e-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="b298e-139">-Sku</span></span>
<span data-ttu-id="b298e-140">Wählen Sie Basic_Direct_Free oder Premium_Direct_Free aus, es sei denn, Sie müssen explizit eine andere Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="b298e-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="b298e-141">-Tag</span></span>
<span data-ttu-id="b298e-142">Die Tags, die dem Microsoft-Peeringdienst zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b298e-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="b298e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b298e-143">-Confirm</span></span>
<span data-ttu-id="b298e-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b298e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b298e-145">-WhatIf</span></span>
<span data-ttu-id="b298e-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b298e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b298e-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b298e-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b298e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b298e-148">CommonParameters</span></span>
<span data-ttu-id="b298e-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b298e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b298e-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b298e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b298e-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b298e-151">INPUTS</span></span>

### <span data-ttu-id="b298e-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="b298e-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b298e-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b298e-153">OUTPUTS</span></span>

### <span data-ttu-id="b298e-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="b298e-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="b298e-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b298e-155">NOTES</span></span>

## <span data-ttu-id="b298e-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b298e-156">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 341e2b4ad820b3a18e5515b54388ce517762d0ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824015"
---
# <span data-ttu-id="3fa3a-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="3fa3a-101">New-AzPeering</span></span>

## <span data-ttu-id="3fa3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fa3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa3a-103">Erstellt eine neue Peering-Arm-Ressource</span><span class="sxs-lookup"><span data-stu-id="3fa3a-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="3fa3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fa3a-104">SYNTAX</span></span>

### <span data-ttu-id="3fa3a-105">Exchange (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fa3a-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa3a-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="3fa3a-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa3a-107">Direkt</span><span class="sxs-lookup"><span data-stu-id="3fa3a-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa3a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fa3a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fa3a-109">Erstellt einen Arm-Peering für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="3fa3a-110">Weitere Informationen zum Erstellen eines Connection-Objekts finden Sie unter [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) oder [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="3fa3a-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="3fa3a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fa3a-111">EXAMPLES</span></span>

### <span data-ttu-id="3fa3a-112">Erstellen eines neuen direkten Peerings</span><span class="sxs-lookup"><span data-stu-id="3fa3a-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="3fa3a-113">Erstellen eines neuen direkten Peerings mit einer einzelnen Verbindung am Standort Seattle mithilfe von PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="3fa3a-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="3fa3a-114">Erstellen eines neuen Exchange-Peerings</span><span class="sxs-lookup"><span data-stu-id="3fa3a-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="3fa3a-115">Erstellen eines neuen Exchange-Peerings</span><span class="sxs-lookup"><span data-stu-id="3fa3a-115">Create a new exchange peering</span></span>

### <span data-ttu-id="3fa3a-116">Konvertieren von Legacy-Peering in Arm-Peering</span><span class="sxs-lookup"><span data-stu-id="3fa3a-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="3fa3a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa3a-117">PARAMETERS</span></span>

### <span data-ttu-id="3fa3a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fa3a-118">-AsJob</span></span>
<span data-ttu-id="3fa3a-119">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-119">Run in the background.</span></span>

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

### <span data-ttu-id="3fa3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa3a-120">-DefaultProfile</span></span>
<span data-ttu-id="3fa3a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa3a-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="3fa3a-122">-DirectConnection</span></span>
<span data-ttu-id="3fa3a-123">Erstellen Sie eine neue direkte Verbindung mithilfe der New-AzExchangePeeringConnection und der Pipe an diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="3fa3a-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="3fa3a-124">-ExchangeConnection</span></span>
<span data-ttu-id="3fa3a-125">Erstellen Sie eine neue Exchange-Verbindung mithilfe der New-AzExchangePeeringConnection und der Pipe an diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="3fa3a-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fa3a-126">-InputObject</span></span>
<span data-ttu-id="3fa3a-127">Verwenden Sie Get-AzLegacyPeering, um dieses Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="3fa3a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3fa3a-128">-Name</span></span>
<span data-ttu-id="3fa3a-129">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-129">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3fa3a-130">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa3a-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="3fa3a-131">Die Peer-ASN-Ressourcen-ID. verwenden Sie Get-AzPeerAsn, um die ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="3fa3a-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3fa3a-132">-PeeringLocation</span></span>
<span data-ttu-id="3fa3a-133">Der physikalische Standort, der sich vom Azure-Bereich unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="3fa3a-134">Verwenden Sie Get-AzPeeringLocation freundliche \< Art \> , um den Namen der Stadt als Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="3fa3a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa3a-135">-ResourceGroupName</span></span>
<span data-ttu-id="3fa3a-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-136">The resource group name.</span></span>

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

### <span data-ttu-id="3fa3a-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="3fa3a-137">-Sku</span></span>
<span data-ttu-id="3fa3a-138">Wählen Sie Basic_Direct_Free oder Premium_Direct_Free aus, es sei denn, es wird explizit eine andere Option ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="3fa3a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fa3a-139">-Tag</span></span>
<span data-ttu-id="3fa3a-140">Die Tags, die dem Microsoft Peering-Dienst zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-140">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="3fa3a-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fa3a-141">-Confirm</span></span>
<span data-ttu-id="3fa3a-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa3a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa3a-143">-WhatIf</span></span>
<span data-ttu-id="3fa3a-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fa3a-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa3a-146">CommonParameters</span></span>
<span data-ttu-id="3fa3a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa3a-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fa3a-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa3a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fa3a-149">INPUTS</span></span>

### <span data-ttu-id="3fa3a-150">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="3fa3a-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3fa3a-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fa3a-151">OUTPUTS</span></span>

### <span data-ttu-id="3fa3a-152">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="3fa3a-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3fa3a-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fa3a-153">NOTES</span></span>

## <span data-ttu-id="3fa3a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fa3a-154">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0824693c2d9f849b80f36065814f8dc57209a2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937552"
---
# <span data-ttu-id="2a6e8-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2a6e8-101">Update-AzPeering</span></span>

## <span data-ttu-id="2a6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2a6e8-103">Legt das Peering fest.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-103">Sets the Peering.</span></span> <span data-ttu-id="2a6e8-104">Verwenden Sie diesen Befehl in Verbindung mit `Set-AzDirectPeeringConnectionObject` oder `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="2a6e8-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="2a6e8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a6e8-105">SYNTAX</span></span>

### <span data-ttu-id="2a6e8-106">DefaultExchange (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a6e8-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6e8-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="2a6e8-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6e8-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="2a6e8-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6e8-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="2a6e8-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6e8-110">Direct</span><span class="sxs-lookup"><span data-stu-id="2a6e8-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a6e8-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="2a6e8-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a6e8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a6e8-112">DESCRIPTION</span></span>
<span data-ttu-id="2a6e8-113">Legt das PSPeering-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="2a6e8-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a6e8-114">EXAMPLES</span></span>

### <span data-ttu-id="2a6e8-115">Aktualisieren des Md5-Authentifizierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="2a6e8-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="2a6e8-116">Legt den Md5-Authentifizierungsschlüssel fest</span><span class="sxs-lookup"><span data-stu-id="2a6e8-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="2a6e8-117">Aktualisieren von UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2a6e8-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="2a6e8-118">Legt die Kennzeichnung Für Peeringdienst verwenden fest</span><span class="sxs-lookup"><span data-stu-id="2a6e8-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="2a6e8-119">Aktualisieren der IPv4-Adresse für Exchange-Peering</span><span class="sxs-lookup"><span data-stu-id="2a6e8-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="2a6e8-120">Legt die Ipv4-Adresse für ein Exchange-Peering mithilfe von ResourceId fest.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="2a6e8-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2a6e8-121">PARAMETERS</span></span>

### <span data-ttu-id="2a6e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a6e8-122">-DefaultProfile</span></span>
<span data-ttu-id="2a6e8-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a6e8-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="2a6e8-124">-DirectConnection</span></span>
<span data-ttu-id="2a6e8-125">Erstellen Sie neue Direkte Verbindungen mit New-AzDirectPeeringConnectionObject und Pipe zu diesem Befehl.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="2a6e8-126">-ExchangeConnection</span></span>
<span data-ttu-id="2a6e8-127">Erstellen Sie eine neue Exchange-Verbindung mit New-AzExchangePeeringConnectionObject und Pipe zu diesem Befehl.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a6e8-128">-InputObject</span></span>
<span data-ttu-id="2a6e8-129">Das Peeringobjekt</span><span class="sxs-lookup"><span data-stu-id="2a6e8-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2a6e8-130">-Name</span></span>
<span data-ttu-id="2a6e8-131">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a6e8-132">-ResourceGroupName</span></span>
<span data-ttu-id="2a6e8-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a6e8-134">-ResourceId</span></span>
<span data-ttu-id="2a6e8-135">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a6e8-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a6e8-136">-Confirm</span></span>
<span data-ttu-id="2a6e8-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a6e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a6e8-138">-WhatIf</span></span>
<span data-ttu-id="2a6e8-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a6e8-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a6e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a6e8-141">CommonParameters</span></span>
<span data-ttu-id="2a6e8-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a6e8-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a6e8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a6e8-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a6e8-144">INPUTS</span></span>

### <span data-ttu-id="2a6e8-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2a6e8-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="2a6e8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2a6e8-146">System.String</span></span>

## <span data-ttu-id="2a6e8-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a6e8-147">OUTPUTS</span></span>

### <span data-ttu-id="2a6e8-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2a6e8-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2a6e8-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2a6e8-149">NOTES</span></span>

## <span data-ttu-id="2a6e8-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2a6e8-150">RELATED LINKS</span></span>

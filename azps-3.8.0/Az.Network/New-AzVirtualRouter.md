---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003428"
---
# <span data-ttu-id="ed6c8-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ed6c8-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="ed6c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6c8-103">Erstellt eine Azure-VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="ed6c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed6c8-104">SYNTAX</span></span>

### <span data-ttu-id="ed6c8-105">HostedGatewayParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed6c8-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed6c8-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed6c8-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed6c8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed6c8-107">DESCRIPTION</span></span>
<span data-ttu-id="ed6c8-108">Das Cmdlet " **New-AzVirtualRouter** " erstellt ein Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ed6c8-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="ed6c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed6c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ed6c8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed6c8-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="ed6c8-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed6c8-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="ed6c8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed6c8-112">PARAMETERS</span></span>

### <span data-ttu-id="ed6c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed6c8-113">-AsJob</span></span>
<span data-ttu-id="ed6c8-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ed6c8-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6c8-115">-DefaultProfile</span></span>
<span data-ttu-id="ed6c8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ed6c8-117">-Force</span></span>
<span data-ttu-id="ed6c8-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="ed6c8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="ed6c8-119">-HostedGateway</span></span>
<span data-ttu-id="ed6c8-120">Das Gateway, in dem virtueller Router gehostet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="ed6c8-121">-HostedGatewayId</span></span>
<span data-ttu-id="ed6c8-122">Die ID des Gateways, in dem virtueller Router gehostet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="ed6c8-123">-Location</span></span>
<span data-ttu-id="ed6c8-124">Die Position.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ed6c8-125">-Name</span></span>
<span data-ttu-id="ed6c8-126">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed6c8-128">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed6c8-129">-Tag</span></span>
<span data-ttu-id="ed6c8-130">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed6c8-131">-Confirm</span></span>
<span data-ttu-id="ed6c8-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed6c8-133">-WhatIf</span></span>
<span data-ttu-id="ed6c8-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed6c8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6c8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6c8-136">CommonParameters</span></span>
<span data-ttu-id="ed6c8-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6c8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed6c8-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6c8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6c8-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed6c8-139">INPUTS</span></span>

### <span data-ttu-id="ed6c8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ed6c8-140">System.String</span></span>

### <span data-ttu-id="ed6c8-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6c8-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ed6c8-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ed6c8-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed6c8-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed6c8-143">OUTPUTS</span></span>

### <span data-ttu-id="ed6c8-144">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ed6c8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ed6c8-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed6c8-145">NOTES</span></span>

## <span data-ttu-id="ed6c8-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed6c8-146">RELATED LINKS</span></span>

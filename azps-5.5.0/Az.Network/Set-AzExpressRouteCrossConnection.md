---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156756"
---
# <span data-ttu-id="1a83a-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1a83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a83a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a83a-103">Ändert eine ExpressRoute-Kreuzverbindung.</span><span class="sxs-lookup"><span data-stu-id="1a83a-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1a83a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a83a-104">SYNTAX</span></span>

### <span data-ttu-id="1a83a-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="1a83a-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a83a-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1a83a-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a83a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a83a-107">DESCRIPTION</span></span>
<span data-ttu-id="1a83a-108">Das **Cmdlet Set-AzExpressRouteCrossConnection** speichert die geänderte ExpressRoute-Querverbindung mit Azure.</span><span class="sxs-lookup"><span data-stu-id="1a83a-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="1a83a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a83a-109">EXAMPLES</span></span>

### <span data-ttu-id="1a83a-110">Beispiel 1: Ändern des Bereitstellungsstatus eines Dienstanbieters für eine ExpressRoute-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="1a83a-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="1a83a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a83a-111">PARAMETERS</span></span>

### <span data-ttu-id="1a83a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a83a-112">-AsJob</span></span>
<span data-ttu-id="1a83a-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a83a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a83a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a83a-114">-DefaultProfile</span></span>
<span data-ttu-id="1a83a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a83a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a83a-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1a83a-117">Gibt das **ExpressRouteCrossConnection-Objekt** an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1a83a-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1a83a-118">-Force</span></span>
<span data-ttu-id="1a83a-119">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1a83a-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1a83a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1a83a-120">-Name</span></span>
<span data-ttu-id="1a83a-121">Der Name der Expressrouten-Kreuzverbindung.</span><span class="sxs-lookup"><span data-stu-id="1a83a-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="1a83a-122">-Peerings</span></span>
<span data-ttu-id="1a83a-123">Die Liste der Peerings für die Querverbindung</span><span class="sxs-lookup"><span data-stu-id="1a83a-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a83a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a83a-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="1a83a-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="1a83a-127">Die Hinweise des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="1a83a-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1a83a-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="1a83a-129">Der Dienstanbieterbereitstellungszustand, der festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="1a83a-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a83a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a83a-130">-Confirm</span></span>
<span data-ttu-id="1a83a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a83a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a83a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1a83a-132">-WhatIf</span></span>
<span data-ttu-id="1a83a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a83a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a83a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a83a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a83a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a83a-135">CommonParameters</span></span>
<span data-ttu-id="1a83a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a83a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a83a-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a83a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a83a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a83a-138">INPUTS</span></span>

### <span data-ttu-id="1a83a-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="1a83a-140">Der Parameter 'ExpressRouteCrossConnection' akzeptiert den Wert des Typs 'PSExpressRouteCrossConnection' aus der Pipeline</span><span class="sxs-lookup"><span data-stu-id="1a83a-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="1a83a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a83a-141">OUTPUTS</span></span>

### <span data-ttu-id="1a83a-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1a83a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a83a-143">NOTES</span></span>

## <span data-ttu-id="1a83a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a83a-144">RELATED LINKS</span></span>

[<span data-ttu-id="1a83a-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1a83a-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)

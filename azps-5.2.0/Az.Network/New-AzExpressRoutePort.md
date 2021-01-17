---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303083"
---
# <span data-ttu-id="87d8d-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="87d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="87d8d-103">Erstellt einen Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="87d8d-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="87d8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87d8d-104">SYNTAX</span></span>

### <span data-ttu-id="87d8d-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87d8d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d8d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d8d-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87d8d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87d8d-107">DESCRIPTION</span></span>
<span data-ttu-id="87d8d-108">Das **Cmdlet "New-AzExpressRoutePort"** erstellt einen Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="87d8d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87d8d-109">EXAMPLES</span></span>

### <span data-ttu-id="87d8d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87d8d-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="87d8d-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="87d8d-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="87d8d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87d8d-112">PARAMETERS</span></span>

### <span data-ttu-id="87d8d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87d8d-113">-AsJob</span></span>
<span data-ttu-id="87d8d-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87d8d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87d8d-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="87d8d-115">-BandwidthInGbps</span></span>
<span data-ttu-id="87d8d-116">Bandbreite der in Gbps verfügbaren ports</span><span class="sxs-lookup"><span data-stu-id="87d8d-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d8d-117">-DefaultProfile</span></span>
<span data-ttu-id="87d8d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87d8d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d8d-119">-Kapselung</span><span class="sxs-lookup"><span data-stu-id="87d8d-119">-Encapsulation</span></span>
<span data-ttu-id="87d8d-120">Kapselungsmethode für physische Ports.</span><span class="sxs-lookup"><span data-stu-id="87d8d-120">Encapsulation method on physical ports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="87d8d-121">-Force</span></span>
<span data-ttu-id="87d8d-122">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="87d8d-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="87d8d-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="87d8d-123">-Identity</span></span>
<span data-ttu-id="87d8d-124">Vom Benutzer zugewiesene Identität zum Lesen der MacSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="87d8d-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-125">-Link</span><span class="sxs-lookup"><span data-stu-id="87d8d-125">-Link</span></span>
<span data-ttu-id="87d8d-126">Die Gruppe physischer Verknüpfungen der "ExpressRoutePort"-Ressource</span><span class="sxs-lookup"><span data-stu-id="87d8d-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="87d8d-127">-Location</span></span>
<span data-ttu-id="87d8d-128">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="87d8d-128">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="87d8d-129">-Name</span></span>
<span data-ttu-id="87d8d-130">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="87d8d-130">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="87d8d-131">-PeeringLocation</span></span>
<span data-ttu-id="87d8d-132">Der Name des Peeringstandorts, dem der ExpressRoutePort physisch zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87d8d-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d8d-133">-ResourceGroupName</span></span>
<span data-ttu-id="87d8d-134">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="87d8d-134">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87d8d-135">-ResourceId</span></span>
<span data-ttu-id="87d8d-136">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="87d8d-136">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="87d8d-137">-Tag</span></span>
<span data-ttu-id="87d8d-138">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="87d8d-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d8d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87d8d-139">-Confirm</span></span>
<span data-ttu-id="87d8d-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87d8d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d8d-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="87d8d-141">-WhatIf</span></span>
<span data-ttu-id="87d8d-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87d8d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d8d-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87d8d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d8d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d8d-144">CommonParameters</span></span>
<span data-ttu-id="87d8d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d8d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d8d-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d8d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d8d-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87d8d-147">INPUTS</span></span>

### <span data-ttu-id="87d8d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="87d8d-148">System.String</span></span>

### <span data-ttu-id="87d8d-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="87d8d-149">System.Int32</span></span>

### <span data-ttu-id="87d8d-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="87d8d-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="87d8d-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="87d8d-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="87d8d-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87d8d-152">OUTPUTS</span></span>

### <span data-ttu-id="87d8d-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="87d8d-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87d8d-154">NOTES</span></span>

## <span data-ttu-id="87d8d-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87d8d-155">RELATED LINKS</span></span>

[<span data-ttu-id="87d8d-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="87d8d-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="87d8d-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="87d8d-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)

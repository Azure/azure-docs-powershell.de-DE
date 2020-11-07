---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 7f6b68b02644b8244459398028680c9872fffa84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660552"
---
# <span data-ttu-id="1c983-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="1c983-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c983-102">SYNOPSIS</span></span>
<span data-ttu-id="1c983-103">Erstellt eine Azure-ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="1c983-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="1c983-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c983-104">SYNTAX</span></span>

### <span data-ttu-id="1c983-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c983-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c983-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c983-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c983-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c983-107">DESCRIPTION</span></span>
<span data-ttu-id="1c983-108">Das Cmdlet " **New-AzExpressRoutePort** " erstellt ein Azure-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="1c983-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c983-109">EXAMPLES</span></span>

### <span data-ttu-id="1c983-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c983-110">Example 1</span></span>
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

### <span data-ttu-id="1c983-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1c983-111">Example 2</span></span>
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

## <span data-ttu-id="1c983-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c983-112">PARAMETERS</span></span>

### <span data-ttu-id="1c983-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c983-113">-AsJob</span></span>
<span data-ttu-id="1c983-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1c983-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c983-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="1c983-115">-BandwidthInGbps</span></span>
<span data-ttu-id="1c983-116">Bandbreite der beschafften Anschlüsse in Gbit/s</span><span class="sxs-lookup"><span data-stu-id="1c983-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="1c983-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c983-117">-DefaultProfile</span></span>
<span data-ttu-id="1c983-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c983-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c983-119">-Kapselung</span><span class="sxs-lookup"><span data-stu-id="1c983-119">-Encapsulation</span></span>
<span data-ttu-id="1c983-120">Kapselungsmethode für physikalische Ports</span><span class="sxs-lookup"><span data-stu-id="1c983-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="1c983-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1c983-121">-Force</span></span>
<span data-ttu-id="1c983-122">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1c983-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1c983-123">-Link</span><span class="sxs-lookup"><span data-stu-id="1c983-123">-Link</span></span>
<span data-ttu-id="1c983-124">Der Satz physikalischer Links der ExpressRoutePort-Ressource</span><span class="sxs-lookup"><span data-stu-id="1c983-124">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="1c983-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="1c983-125">-Location</span></span>
<span data-ttu-id="1c983-126">Die Position.</span><span class="sxs-lookup"><span data-stu-id="1c983-126">The location.</span></span>

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

### <span data-ttu-id="1c983-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1c983-127">-Name</span></span>
<span data-ttu-id="1c983-128">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="1c983-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="1c983-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="1c983-129">-PeeringLocation</span></span>
<span data-ttu-id="1c983-130">Der Name des Peering-Standorts, dem die ExpressRoutePort physisch zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1c983-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="1c983-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c983-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c983-132">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="1c983-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="1c983-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1c983-133">-ResourceId</span></span>
<span data-ttu-id="1c983-134">Die Quelle des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="1c983-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="1c983-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c983-135">-Tag</span></span>
<span data-ttu-id="1c983-136">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c983-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1c983-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c983-137">-Confirm</span></span>
<span data-ttu-id="1c983-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c983-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c983-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c983-139">-WhatIf</span></span>
<span data-ttu-id="1c983-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c983-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c983-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c983-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c983-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c983-142">CommonParameters</span></span>
<span data-ttu-id="1c983-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c983-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c983-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c983-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c983-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c983-145">INPUTS</span></span>

### <span data-ttu-id="1c983-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1c983-146">System.String</span></span>

### <span data-ttu-id="1c983-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1c983-147">System.Int32</span></span>

### <span data-ttu-id="1c983-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c983-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1c983-149">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="1c983-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="1c983-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c983-150">OUTPUTS</span></span>

### <span data-ttu-id="1c983-151">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="1c983-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c983-152">NOTES</span></span>

## <span data-ttu-id="1c983-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c983-153">RELATED LINKS</span></span>

[<span data-ttu-id="1c983-154">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-154">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="1c983-155">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-155">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="1c983-156">Satz-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1c983-156">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)

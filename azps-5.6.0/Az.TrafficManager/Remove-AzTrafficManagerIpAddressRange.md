---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: f427407ad966fd9680646e1d8b7551624231229d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936443"
---
# <span data-ttu-id="c3a98-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c3a98-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="c3a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3a98-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a98-103">Entfernt einen Adressbereich oder ein Subnetz aus einem lokalen Traffic Manager-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3a98-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="c3a98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3a98-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3a98-105">DESCRIPTION</span></span>
<span data-ttu-id="c3a98-106">Das **Cmdlet Remove-AzTrafficManagerIpAddressRange** entfernt einen IP-Adressbereich aus einem lokalen Azure Traffic Manager-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3a98-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="c3a98-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="c3a98-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="c3a98-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3a98-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="c3a98-109">Sie können Ihre Änderungen mithilfe des cmdlets "Set-AzTrafficManagerEndpoint" am Endpunkt für Traffic Manager festlegen.</span><span class="sxs-lookup"><span data-stu-id="c3a98-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="c3a98-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3a98-110">EXAMPLES</span></span>

### <span data-ttu-id="c3a98-111">Beispiel 1: Entfernen von IP-Adressbereichen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c3a98-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="c3a98-112">Der erste Befehl ruft den Azure-Endpunkt "contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="c3a98-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="c3a98-113">Mit dem zweiten Befehl wird ein IP-Adressbereich aus dem Endpunkt entfernt, der in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c3a98-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c3a98-114">Der letzte Befehl aktualisiert den Endpunkt in Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c3a98-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="c3a98-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3a98-115">PARAMETERS</span></span>

### <span data-ttu-id="c3a98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a98-116">-DefaultProfile</span></span>
<span data-ttu-id="c3a98-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3a98-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3a98-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3a98-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c3a98-119">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c3a98-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="c3a98-120">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3a98-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c3a98-121">Um ein **TrafficManagerEndpoint-Objekt zu** erhalten, verwenden Sie das cmdlet Get-AzTrafficManagerEndpoint oder New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3a98-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3a98-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3a98-122">-Confirm</span></span>
<span data-ttu-id="c3a98-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3a98-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a98-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a98-124">-WhatIf</span></span>
<span data-ttu-id="c3a98-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3a98-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3a98-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3a98-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a98-127">-First</span><span class="sxs-lookup"><span data-stu-id="c3a98-127">-First</span></span>
<span data-ttu-id="c3a98-128">Gibt die erste IP-Adresse im zu entfernenden Bereich an.</span><span class="sxs-lookup"><span data-stu-id="c3a98-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="c3a98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a98-129">CommonParameters</span></span>
<span data-ttu-id="c3a98-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a98-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a98-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a98-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3a98-132">INPUTS</span></span>

### <span data-ttu-id="c3a98-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3a98-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c3a98-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3a98-134">OUTPUTS</span></span>

### <span data-ttu-id="c3a98-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3a98-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c3a98-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3a98-136">NOTES</span></span>

## <span data-ttu-id="c3a98-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3a98-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3a98-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c3a98-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="c3a98-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3a98-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c3a98-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3a98-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c3a98-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3a98-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

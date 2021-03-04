---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936467"
---
# <span data-ttu-id="e336c-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="e336c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e336c-102">SYNOPSIS</span></span>
<span data-ttu-id="e336c-103">Entfernt benutzerdefinierte Kopfzeileninformationen aus einem lokalen Traffic Manager-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="e336c-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="e336c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e336c-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e336c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e336c-105">DESCRIPTION</span></span>
<span data-ttu-id="e336c-106">Das **Cmdlet Remove-AzTrafficManagerCustomHeaderFromEndpoint** entfernt benutzerdefinierte Kopfzeileninformationen aus einem lokalen Azure Traffic Manager-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="e336c-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e336c-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="e336c-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e336c-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="e336c-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e336c-109">Sie können Ihre Änderungen mithilfe des cmdlets "Set-AzTrafficManagerEndpoint" am Endpunkt für Traffic Manager festlegen.</span><span class="sxs-lookup"><span data-stu-id="e336c-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e336c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e336c-110">EXAMPLES</span></span>

### <span data-ttu-id="e336c-111">Beispiel 1: Entfernen benutzerdefinierter Subnetzinformationen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e336c-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e336c-112">Der erste Befehl ruft den Azure-Endpunkt "contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="e336c-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e336c-113">Mit dem zweiten Befehl werden benutzerdefinierte Kopfzeileninformationen aus dem endpunkt entfernt, der in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e336c-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e336c-114">Der letzte Befehl aktualisiert den Endpunkt in Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e336c-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e336c-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e336c-115">PARAMETERS</span></span>

### <span data-ttu-id="e336c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e336c-116">-DefaultProfile</span></span>
<span data-ttu-id="e336c-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e336c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e336c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e336c-118">-Name</span></span>
<span data-ttu-id="e336c-119">Gibt den Namen der zu entfernenden benutzerdefinierten Kopfzeileninformationen an.</span><span class="sxs-lookup"><span data-stu-id="e336c-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="e336c-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e336c-121">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e336c-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e336c-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="e336c-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e336c-123">Um ein **TrafficManagerEndpoint-Objekt zu** erhalten, verwenden Sie das cmdlet Get-AzTrafficManagerEndpoint oder New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e336c-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e336c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e336c-124">-Confirm</span></span>
<span data-ttu-id="e336c-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e336c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e336c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e336c-126">-WhatIf</span></span>
<span data-ttu-id="e336c-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e336c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e336c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e336c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e336c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e336c-129">CommonParameters</span></span>
<span data-ttu-id="e336c-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e336c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e336c-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e336c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e336c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e336c-132">INPUTS</span></span>

### <span data-ttu-id="e336c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e336c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e336c-134">OUTPUTS</span></span>

### <span data-ttu-id="e336c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e336c-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e336c-136">NOTES</span></span>

## <span data-ttu-id="e336c-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e336c-137">RELATED LINKS</span></span>

[<span data-ttu-id="e336c-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="e336c-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e336c-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e336c-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e336c-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e336c-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

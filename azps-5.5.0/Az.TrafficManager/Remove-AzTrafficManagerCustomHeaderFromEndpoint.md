---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165473"
---
# <span data-ttu-id="9684d-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="9684d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9684d-102">SYNOPSIS</span></span>
<span data-ttu-id="9684d-103">Entfernt benutzerdefinierte Headerinformationen aus einem lokalen Endpunktobjekt für den Datenverkehrs-Manager.</span><span class="sxs-lookup"><span data-stu-id="9684d-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="9684d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9684d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9684d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9684d-105">DESCRIPTION</span></span>
<span data-ttu-id="9684d-106">Das **Cmdlet "Remove-AzTrafficManagerCustomHeaderFromEndpoint"** entfernt benutzerdefinierte Headerinformationen aus einem lokalen Azure Traffic Manager-Endpunktobjekt.</span><span class="sxs-lookup"><span data-stu-id="9684d-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="9684d-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="9684d-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="9684d-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="9684d-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="9684d-109">Sie können Ihre Änderungen am Endpunkt für Verkehrs-Manager mithilfe des cmdlets Set-AzTrafficManagerEndpoint festlegen.</span><span class="sxs-lookup"><span data-stu-id="9684d-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9684d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9684d-110">EXAMPLES</span></span>

### <span data-ttu-id="9684d-111">Beispiel 1: Entfernen von benutzerdefinierten Subnetzinformationen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="9684d-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9684d-112">Der erste Befehl ruft den Azure-Endpunkt "contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint Variable.</span><span class="sxs-lookup"><span data-stu-id="9684d-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="9684d-113">Mit dem zweiten Befehl werden benutzerdefinierte Kopfzeileninformationen vom Endpunkt entfernt, der in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9684d-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="9684d-114">Der letzte Befehl aktualisiert den Endpunkt im Verkehrs-Manager so, dass er dem lokalen Wert in der $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9684d-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9684d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9684d-115">PARAMETERS</span></span>

### <span data-ttu-id="9684d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9684d-116">-DefaultProfile</span></span>
<span data-ttu-id="9684d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9684d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9684d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9684d-118">-Name</span></span>
<span data-ttu-id="9684d-119">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9684d-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="9684d-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9684d-121">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9684d-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9684d-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="9684d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9684d-123">Verwenden Sie zum **Abrufen eines TrafficManagerEndpoint-Objekts** das cmdlet Get-AzTrafficManagerEndpoint New-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9684d-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="9684d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9684d-124">-Confirm</span></span>
<span data-ttu-id="9684d-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9684d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9684d-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9684d-126">-WhatIf</span></span>
<span data-ttu-id="9684d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9684d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9684d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9684d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9684d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9684d-129">CommonParameters</span></span>
<span data-ttu-id="9684d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9684d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9684d-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9684d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9684d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9684d-132">INPUTS</span></span>

### <span data-ttu-id="9684d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9684d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9684d-134">OUTPUTS</span></span>

### <span data-ttu-id="9684d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9684d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9684d-136">NOTES</span></span>

## <span data-ttu-id="9684d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9684d-137">RELATED LINKS</span></span>

[<span data-ttu-id="9684d-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="9684d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9684d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9684d-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9684d-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9684d-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

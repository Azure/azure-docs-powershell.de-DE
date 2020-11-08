---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003259"
---
# <span data-ttu-id="5d2e8-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="5d2e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2e8-103">Entfernt benutzerdefinierte Headerinformationen aus einem lokalen Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="5d2e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d2e8-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d2e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d2e8-105">DESCRIPTION</span></span>
<span data-ttu-id="5d2e8-106">Das Cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** entfernt benutzerdefinierte Headerinformationen aus einem lokalen Azure Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="5d2e8-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="5d2e8-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="5d2e8-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="5d2e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d2e8-110">EXAMPLES</span></span>

### <span data-ttu-id="5d2e8-111">Beispiel 1: Entfernen benutzerdefinierter Subnetz-Informationen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5d2e8-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="5d2e8-112">Der erste Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="5d2e8-113">Der zweite Befehl entfernt benutzerdefinierte Headerinformationen aus dem in $TrafficManagerEndpoint gespeicherten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5d2e8-114">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="5d2e8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d2e8-115">PARAMETERS</span></span>

### <span data-ttu-id="5d2e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e8-116">-DefaultProfile</span></span>
<span data-ttu-id="5d2e8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d2e8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5d2e8-118">-Name</span></span>
<span data-ttu-id="5d2e8-119">Gibt den Namen der benutzerdefinierten Headerinformationen an, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="5d2e8-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5d2e8-121">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="5d2e8-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5d2e8-123">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzTrafficManagerEndpoint-oder New-AzTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="5d2e8-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d2e8-124">-Confirm</span></span>
<span data-ttu-id="5d2e8-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d2e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d2e8-126">-WhatIf</span></span>
<span data-ttu-id="5d2e8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d2e8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d2e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2e8-129">CommonParameters</span></span>
<span data-ttu-id="5d2e8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d2e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2e8-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2e8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2e8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d2e8-132">INPUTS</span></span>

### <span data-ttu-id="5d2e8-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5d2e8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d2e8-134">OUTPUTS</span></span>

### <span data-ttu-id="5d2e8-135">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5d2e8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d2e8-136">NOTES</span></span>

## <span data-ttu-id="5d2e8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d2e8-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d2e8-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="5d2e8-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e8-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5d2e8-140">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5d2e8-141">Satz-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d2e8-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

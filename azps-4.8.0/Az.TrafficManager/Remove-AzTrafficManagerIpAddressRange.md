---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173351"
---
# <span data-ttu-id="54d6c-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="54d6c-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="54d6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="54d6c-103">Entfernt einen Adressbereich oder ein Subnetz aus einem lokalen Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="54d6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54d6c-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="54d6c-106">Das Cmdlet **Remove-AzTrafficManagerIpAddressRange** entfernt einen IP-Adressbereich aus einem lokalen Azure Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="54d6c-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="54d6c-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="54d6c-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="54d6c-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="54d6c-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="54d6c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54d6c-110">EXAMPLES</span></span>

### <span data-ttu-id="54d6c-111">Beispiel 1: Entfernen von IP-Adressbereichen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="54d6c-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="54d6c-112">Der erste Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="54d6c-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="54d6c-113">Der zweite Befehl entfernt einen IP-Adressbereich aus dem in $TrafficManagerEndpoint gespeicherten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="54d6c-114">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="54d6c-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="54d6c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="54d6c-115">PARAMETERS</span></span>

### <span data-ttu-id="54d6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d6c-116">-DefaultProfile</span></span>
<span data-ttu-id="54d6c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54d6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d6c-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54d6c-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="54d6c-119">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="54d6c-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="54d6c-120">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="54d6c-121">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzTrafficManagerEndpoint-oder New-AzTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d6c-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="54d6c-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54d6c-122">-Confirm</span></span>
<span data-ttu-id="54d6c-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54d6c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d6c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d6c-124">-WhatIf</span></span>
<span data-ttu-id="54d6c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d6c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d6c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54d6c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d6c-127">-First</span><span class="sxs-lookup"><span data-stu-id="54d6c-127">-First</span></span>
<span data-ttu-id="54d6c-128">Gibt die erste IP-Adresse in dem Bereich an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54d6c-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="54d6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d6c-129">CommonParameters</span></span>
<span data-ttu-id="54d6c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d6c-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d6c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d6c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54d6c-132">INPUTS</span></span>

### <span data-ttu-id="54d6c-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54d6c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="54d6c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54d6c-134">OUTPUTS</span></span>

### <span data-ttu-id="54d6c-135">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54d6c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="54d6c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="54d6c-136">NOTES</span></span>

## <span data-ttu-id="54d6c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54d6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="54d6c-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="54d6c-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="54d6c-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54d6c-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="54d6c-140">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54d6c-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="54d6c-141">Satz-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54d6c-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

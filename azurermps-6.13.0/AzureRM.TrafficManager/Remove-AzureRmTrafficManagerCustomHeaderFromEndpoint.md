---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477578"
---
# <span data-ttu-id="8cd0a-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="8cd0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd0a-103">Entfernt benutzerdefinierte Headerinformationen aus einem lokalen Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cd0a-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cd0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cd0a-105">DESCRIPTION</span></span>
<span data-ttu-id="8cd0a-106">Das Cmdlet **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** entfernt benutzerdefinierte Headerinformationen aus einem lokalen Azure Traffic Manager-Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="8cd0a-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzureRmTrafficManagerEndpoint oder Get-AzureRmTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="8cd0a-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="8cd0a-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8cd0a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cd0a-110">EXAMPLES</span></span>

### <span data-ttu-id="8cd0a-111">Beispiel 1: Entfernen benutzerdefinierter Subnetz-Informationen von einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="8cd0a-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="8cd0a-112">Der erste Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="8cd0a-113">Der zweite Befehl entfernt benutzerdefinierte Headerinformationen aus dem in $TrafficManagerEndpoint gespeicherten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8cd0a-114">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="8cd0a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cd0a-115">PARAMETERS</span></span>

### <span data-ttu-id="8cd0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd0a-116">-DefaultProfile</span></span>
<span data-ttu-id="8cd0a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd0a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8cd0a-118">-Name</span></span>
<span data-ttu-id="8cd0a-119">Gibt den Namen der benutzerdefinierten Headerinformationen an, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="8cd0a-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8cd0a-121">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="8cd0a-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8cd0a-123">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzureRmTrafficManagerEndpoint-oder New-AzureRmTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8cd0a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cd0a-124">-Confirm</span></span>
<span data-ttu-id="8cd0a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cd0a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cd0a-126">-WhatIf</span></span>
<span data-ttu-id="8cd0a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cd0a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cd0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd0a-129">CommonParameters</span></span>
<span data-ttu-id="8cd0a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd0a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd0a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd0a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cd0a-132">INPUTS</span></span>

### <span data-ttu-id="8cd0a-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="8cd0a-134">Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="8cd0a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cd0a-135">OUTPUTS</span></span>

### <span data-ttu-id="8cd0a-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="8cd0a-137">Dieses Cmdlet gibt ein geändertes TrafficManagerEndpoint-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8cd0a-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="8cd0a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cd0a-138">NOTES</span></span>

## <span data-ttu-id="8cd0a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cd0a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8cd0a-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="8cd0a-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cd0a-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8cd0a-142">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8cd0a-143">Satz-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cd0a-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)

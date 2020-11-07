---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827068"
---
# <span data-ttu-id="3030d-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3030d-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="3030d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3030d-102">SYNOPSIS</span></span>
<span data-ttu-id="3030d-103">Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3030d-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="3030d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3030d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3030d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3030d-105">DESCRIPTION</span></span>
<span data-ttu-id="3030d-106">Das Cmdlet **Remove-AzTrafficManagerEndpointConfig** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3030d-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3030d-107">Sie können ein Profil mithilfe des Get-AzTrafficManagerProfile-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="3030d-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="3030d-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3030d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3030d-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3030d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="3030d-110">Verwenden Sie das Remove-AzTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu entfernen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="3030d-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3030d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3030d-111">EXAMPLES</span></span>

### <span data-ttu-id="3030d-112">Beispiel 1: Entfernen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="3030d-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3030d-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="3030d-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3030d-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="3030d-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="3030d-115">Der zweite Befehl entfernt einen Azure-Endpunkt namens Contoso aus dem Profil, das in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3030d-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3030d-116">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="3030d-116">This command changes only the local object.</span></span>

<span data-ttu-id="3030d-117">Der endgültige Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="3030d-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3030d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3030d-118">PARAMETERS</span></span>

### <span data-ttu-id="3030d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-119">-DefaultProfile</span></span>
<span data-ttu-id="3030d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3030d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3030d-121">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="3030d-121">-EndpointName</span></span>
<span data-ttu-id="3030d-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="3030d-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3030d-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="3030d-124">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3030d-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3030d-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="3030d-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3030d-126">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3030d-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3030d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3030d-127">CommonParameters</span></span>
<span data-ttu-id="3030d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3030d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3030d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3030d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3030d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3030d-130">INPUTS</span></span>

### <span data-ttu-id="3030d-131">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3030d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3030d-132">OUTPUTS</span></span>

### <span data-ttu-id="3030d-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3030d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3030d-134">NOTES</span></span>

## <span data-ttu-id="3030d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3030d-135">RELATED LINKS</span></span>

[<span data-ttu-id="3030d-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3030d-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3030d-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3030d-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3030d-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3030d-139">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3030d-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



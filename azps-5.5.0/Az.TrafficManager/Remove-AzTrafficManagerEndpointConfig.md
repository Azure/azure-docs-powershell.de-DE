---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157764"
---
# <span data-ttu-id="5dcaa-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5dcaa-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="5dcaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcaa-103">Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="5dcaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5dcaa-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dcaa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5dcaa-105">DESCRIPTION</span></span>
<span data-ttu-id="5dcaa-106">Das **Cmdlet "Remove-AzTrafficManagerEndpointConfig"** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="5dcaa-107">Sie können ein Profil mithilfe des cmdlets Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="5dcaa-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="5dcaa-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5dcaa-110">Verwenden Sie zum Entfernen eines Endpunkts und Zum Commit von Änderungen in einem einzigen Vorgang das Remove-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="5dcaa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5dcaa-111">EXAMPLES</span></span>

### <span data-ttu-id="5dcaa-112">Beispiel 1: Entfernen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="5dcaa-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="5dcaa-113">Der erste Befehl ruft mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ein Azure Traffic -Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="5dcaa-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="5dcaa-115">Mit dem zweiten Befehl wird ein Azure-Endpunkt namens "contoso" aus dem profil entfernt, das in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="5dcaa-116">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-116">This command changes only the local object.</span></span>

<span data-ttu-id="5dcaa-117">Der letzte Befehl aktualisiert das Datenverkehrs-Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="5dcaa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dcaa-118">PARAMETERS</span></span>

### <span data-ttu-id="5dcaa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-119">-DefaultProfile</span></span>
<span data-ttu-id="5dcaa-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dcaa-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5dcaa-121">-EndpointName</span></span>
<span data-ttu-id="5dcaa-122">Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5dcaa-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="5dcaa-124">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5dcaa-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5dcaa-126">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile **TrafficManagerProfile,** um ein TrafficManagerProfile-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="5dcaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcaa-127">CommonParameters</span></span>
<span data-ttu-id="5dcaa-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dcaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcaa-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dcaa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcaa-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5dcaa-130">INPUTS</span></span>

### <span data-ttu-id="5dcaa-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5dcaa-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5dcaa-132">OUTPUTS</span></span>

### <span data-ttu-id="5dcaa-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5dcaa-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5dcaa-134">NOTES</span></span>

## <span data-ttu-id="5dcaa-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5dcaa-135">RELATED LINKS</span></span>

[<span data-ttu-id="5dcaa-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5dcaa-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5dcaa-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5dcaa-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5dcaa-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5dcaa-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5dcaa-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936456"
---
# <span data-ttu-id="12e19-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="12e19-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="12e19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e19-102">SYNOPSIS</span></span>
<span data-ttu-id="12e19-103">Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="12e19-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="12e19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e19-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e19-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e19-105">DESCRIPTION</span></span>
<span data-ttu-id="12e19-106">Das **Cmdlet Remove-AzTrafficManagerEndpointConfig** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="12e19-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="12e19-107">Sie können ein Profil über das cmdlet Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="12e19-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="12e19-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="12e19-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="12e19-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="12e19-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="12e19-110">Um einen Endpunkt zu entfernen und Änderungen in einem einzelnen Vorgang zu commiten, verwenden Sie das Remove-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e19-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="12e19-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e19-111">EXAMPLES</span></span>

### <span data-ttu-id="12e19-112">Beispiel 1: Entfernen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="12e19-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="12e19-113">Der erste Befehl ruft mithilfe des **Get-AzTrafficManagerProfile-Cmdlets ein Azure Traffic Manager-Profil** ab.</span><span class="sxs-lookup"><span data-stu-id="12e19-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="12e19-114">Mit dem Befehl wird das lokale Profil in der $TrafficManagerProfile gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12e19-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="12e19-115">Mit dem zweiten Befehl wird ein Azure-Endpunkt namens contoso aus dem profil entfernt, das in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="12e19-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="12e19-116">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="12e19-116">This command changes only the local object.</span></span>

<span data-ttu-id="12e19-117">Der letzte Befehl aktualisiert das Traffic Manager-Profil namens ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="12e19-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="12e19-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12e19-118">PARAMETERS</span></span>

### <span data-ttu-id="12e19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-119">-DefaultProfile</span></span>
<span data-ttu-id="12e19-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e19-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12e19-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="12e19-121">-EndpointName</span></span>
<span data-ttu-id="12e19-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="12e19-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12e19-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="12e19-124">Gibt ein lokales **TrafficManagerProfile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="12e19-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="12e19-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="12e19-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="12e19-126">Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e19-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="12e19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e19-127">CommonParameters</span></span>
<span data-ttu-id="12e19-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e19-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e19-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e19-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e19-130">INPUTS</span></span>

### <span data-ttu-id="12e19-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="12e19-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e19-132">OUTPUTS</span></span>

### <span data-ttu-id="12e19-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="12e19-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12e19-134">NOTES</span></span>

## <span data-ttu-id="12e19-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12e19-135">RELATED LINKS</span></span>

[<span data-ttu-id="12e19-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="12e19-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="12e19-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="12e19-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12e19-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="12e19-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12e19-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



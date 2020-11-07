---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662256"
---
# <span data-ttu-id="bd149-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bd149-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="bd149-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd149-102">SYNOPSIS</span></span>
<span data-ttu-id="bd149-103">Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="bd149-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd149-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd149-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd149-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd149-105">DESCRIPTION</span></span>
<span data-ttu-id="bd149-106">Das Cmdlet **Remove-AzureRmTrafficManagerEndpointConfig** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="bd149-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="bd149-107">Sie können ein Profil mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="bd149-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="bd149-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="bd149-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="bd149-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bd149-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="bd149-110">Verwenden Sie das Remove-AzureRmTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu entfernen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bd149-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="bd149-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd149-111">EXAMPLES</span></span>

### <span data-ttu-id="bd149-112">Beispiel 1: Entfernen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="bd149-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="bd149-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzureRmTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="bd149-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="bd149-114">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="bd149-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="bd149-115">Der zweite Befehl entfernt einen Azure-Endpunkt namens Contoso aus dem Profil, das in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bd149-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="bd149-116">Mit diesem Befehl wird nur das lokale Objekt geändert.</span><span class="sxs-lookup"><span data-stu-id="bd149-116">This command changes only the local object.</span></span>

<span data-ttu-id="bd149-117">Der endgültige Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="bd149-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="bd149-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd149-118">PARAMETERS</span></span>

### <span data-ttu-id="bd149-119">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="bd149-119">-EndpointName</span></span>
<span data-ttu-id="bd149-120">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="bd149-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd149-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="bd149-122">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bd149-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="bd149-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd149-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bd149-124">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd149-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bd149-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-125">-DefaultProfile</span></span>
<span data-ttu-id="bd149-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd149-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd149-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd149-127">CommonParameters</span></span>
<span data-ttu-id="bd149-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd149-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd149-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd149-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd149-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd149-130">INPUTS</span></span>

### <span data-ttu-id="bd149-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bd149-132">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd149-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="bd149-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd149-133">OUTPUTS</span></span>

### <span data-ttu-id="bd149-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bd149-135">Dieses Cmdlet gibt ein geändertes TrafficManagerProfile-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="bd149-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="bd149-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd149-136">NOTES</span></span>

## <span data-ttu-id="bd149-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd149-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd149-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bd149-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="bd149-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bd149-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd149-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bd149-141">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd149-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



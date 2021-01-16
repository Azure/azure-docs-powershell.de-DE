---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470251"
---
# <span data-ttu-id="b95ec-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="b95ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b95ec-103">Aktualisiert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b95ec-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="b95ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b95ec-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b95ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b95ec-105">DESCRIPTION</span></span>
<span data-ttu-id="b95ec-106">Das **Cmdlet "Set-AzTrafficManagerProfile"** aktualisiert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b95ec-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b95ec-107">Dieses Cmdlet aktualisiert die Einstellungen des Profils aus einem lokalen Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="b95ec-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="b95ec-108">Sie können das Profilobjekt entweder mit dem Parameter *"TrafficManagerProfile"* oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="b95ec-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="b95ec-109">Sie können ein lokales Objekt, das ein Profil darstellt, mithilfe des Get-AzTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="b95ec-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b95ec-110">Ändern Sie das Objekt lokal, und verwenden Sie **dann "Set-AzTrafficManagerProfile",** um Ihre Änderungen zu commiten.</span><span class="sxs-lookup"><span data-stu-id="b95ec-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="b95ec-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b95ec-111">EXAMPLES</span></span>

### <span data-ttu-id="b95ec-112">Beispiel 1: Aktualisieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="b95ec-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b95ec-113">Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des cmdlets Get-AzTrafficManagerProfile ab.</span><span class="sxs-lookup"><span data-stu-id="b95ec-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b95ec-114">Der Befehl speichert das Profil lokal in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="b95ec-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b95ec-115">Mit dem zweiten Befehl wird dieses Profil lokal geändert.</span><span class="sxs-lookup"><span data-stu-id="b95ec-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="b95ec-116">Mit diesem Befehl wird das Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b95ec-116">This command disables the profile.</span></span>

<span data-ttu-id="b95ec-117">Mit dem dritten Befehl wird das Datenverkehrs-Manager-Profil namens "ContosoProfile" so aktualisiert, dass es mit dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b95ec-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b95ec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95ec-118">PARAMETERS</span></span>

### <span data-ttu-id="b95ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-119">-DefaultProfile</span></span>
<span data-ttu-id="b95ec-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95ec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95ec-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="b95ec-122">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="b95ec-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b95ec-123">Mit diesem Cmdlet wird der Datenverkehrs-Manager so aktualisiert, dass er diesem lokalen Objekt entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="b95ec-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="b95ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95ec-124">CommonParameters</span></span>
<span data-ttu-id="b95ec-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95ec-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95ec-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b95ec-127">INPUTS</span></span>

### <span data-ttu-id="b95ec-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b95ec-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b95ec-129">OUTPUTS</span></span>

### <span data-ttu-id="b95ec-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b95ec-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b95ec-131">NOTES</span></span>

## <span data-ttu-id="b95ec-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b95ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="b95ec-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b95ec-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b95ec-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b95ec-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b95ec-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b95ec-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b95ec-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b95ec-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)



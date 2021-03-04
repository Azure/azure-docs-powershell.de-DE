---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936424"
---
# <span data-ttu-id="fa70a-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="fa70a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa70a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa70a-103">Aktualisiert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="fa70a-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="fa70a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa70a-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa70a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa70a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa70a-106">Das **Cmdlet Set-AzTrafficManagerProfile** aktualisiert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="fa70a-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fa70a-107">Dieses Cmdlet aktualisiert die Einstellungen des Profils aus einem lokalen Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="fa70a-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="fa70a-108">Sie können das Profilobjekt entweder mithilfe des *Parameters TrafficManagerProfile* oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="fa70a-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="fa70a-109">Sie können ein lokales Objekt abrufen, das ein Profil darstellt, indem Sie das cmdlet Get-AzTrafficManagerProfile verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa70a-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="fa70a-110">Ändern Sie das Objekt lokal, und verwenden Sie **dann Set-AzTrafficManagerProfile,** um Ihre Änderungen zu commiten.</span><span class="sxs-lookup"><span data-stu-id="fa70a-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="fa70a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa70a-111">EXAMPLES</span></span>

### <span data-ttu-id="fa70a-112">Beispiel 1: Aktualisieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="fa70a-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="fa70a-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mithilfe des cmdlets Get-AzTrafficManagerProfile ab.</span><span class="sxs-lookup"><span data-stu-id="fa70a-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="fa70a-114">Der Befehl speichert das Profil lokal in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fa70a-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="fa70a-115">Mit dem zweiten Befehl wird dieses Profil lokal geändert.</span><span class="sxs-lookup"><span data-stu-id="fa70a-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="fa70a-116">Mit diesem Befehl wird das Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa70a-116">This command disables the profile.</span></span>

<span data-ttu-id="fa70a-117">Der dritte Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fa70a-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="fa70a-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa70a-118">PARAMETERS</span></span>

### <span data-ttu-id="fa70a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-119">-DefaultProfile</span></span>
<span data-ttu-id="fa70a-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa70a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa70a-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="fa70a-122">Gibt ein lokales **TrafficManagerProfile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="fa70a-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fa70a-123">Dieses Cmdlet aktualisiert Traffic Manager so, dass es mit diesem lokalen Objekt übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="fa70a-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="fa70a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa70a-124">CommonParameters</span></span>
<span data-ttu-id="fa70a-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa70a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa70a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa70a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa70a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa70a-127">INPUTS</span></span>

### <span data-ttu-id="fa70a-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fa70a-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa70a-129">OUTPUTS</span></span>

### <span data-ttu-id="fa70a-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fa70a-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa70a-131">NOTES</span></span>

## <span data-ttu-id="fa70a-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa70a-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa70a-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="fa70a-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="fa70a-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fa70a-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="fa70a-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="fa70a-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="fa70a-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa70a-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)



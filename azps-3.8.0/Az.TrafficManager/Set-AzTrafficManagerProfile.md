---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003250"
---
# <span data-ttu-id="29816-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="29816-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29816-102">SYNOPSIS</span></span>
<span data-ttu-id="29816-103">Aktualisiert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="29816-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="29816-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29816-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29816-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29816-105">DESCRIPTION</span></span>
<span data-ttu-id="29816-106">Das Cmdlet " **Satz-AzTrafficManagerProfile** " aktualisiert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="29816-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="29816-107">Dieses Cmdlet aktualisiert die Einstellungen des Profils von einem lokalen Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="29816-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="29816-108">Sie können das Profilobjekt entweder mithilfe des *TrafficManagerProfile* -Parameters oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="29816-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="29816-109">Sie können ein lokales Objekt, das ein Profil darstellt, mithilfe des Get-AzTrafficManagerProfile-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="29816-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="29816-110">Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzTrafficManagerProfile** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="29816-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="29816-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29816-111">EXAMPLES</span></span>

### <span data-ttu-id="29816-112">Beispiel 1: Aktualisieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="29816-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="29816-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mithilfe des Get-AzTrafficManagerProfile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="29816-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="29816-114">Der Befehl speichert das Profil lokal in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29816-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="29816-115">Der zweite Befehl ändert das Profil lokal.</span><span class="sxs-lookup"><span data-stu-id="29816-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="29816-116">Mit diesem Befehl wird das Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="29816-116">This command disables the profile.</span></span>

<span data-ttu-id="29816-117">Der dritte Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="29816-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="29816-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="29816-118">PARAMETERS</span></span>

### <span data-ttu-id="29816-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29816-119">-DefaultProfile</span></span>
<span data-ttu-id="29816-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29816-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29816-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="29816-122">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="29816-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="29816-123">Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="29816-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="29816-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29816-124">CommonParameters</span></span>
<span data-ttu-id="29816-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29816-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29816-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29816-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29816-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29816-127">INPUTS</span></span>

### <span data-ttu-id="29816-128">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="29816-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29816-129">OUTPUTS</span></span>

### <span data-ttu-id="29816-130">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="29816-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="29816-131">NOTES</span></span>

## <span data-ttu-id="29816-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29816-132">RELATED LINKS</span></span>

[<span data-ttu-id="29816-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="29816-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="29816-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="29816-135">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="29816-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="29816-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="29816-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29816-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)



---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e8baf033131442f23a0db63339673018b209f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663286"
---
# <span data-ttu-id="2e5a8-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="2e5a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5a8-103">Aktualisiert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e5a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e5a8-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e5a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e5a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5a8-106">Das Cmdlet " **Satz-AzureRmTrafficManagerProfile** " aktualisiert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2e5a8-107">Dieses Cmdlet aktualisiert die Einstellungen des Profils von einem lokalen Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="2e5a8-108">Sie können das Profilobjekt entweder mithilfe des *TrafficManagerProfile* -Parameters oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="2e5a8-109">Sie können ein lokales Objekt, das ein Profil darstellt, mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2e5a8-110">Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzureRmTrafficManagerProfile** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="2e5a8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e5a8-111">EXAMPLES</span></span>

### <span data-ttu-id="2e5a8-112">Beispiel 1: Aktualisieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="2e5a8-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2e5a8-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2e5a8-114">Der Befehl speichert das Profil lokal in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="2e5a8-115">Der zweite Befehl ändert das Profil lokal.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="2e5a8-116">Mit diesem Befehl wird das Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-116">This command disables the profile.</span></span>

<span data-ttu-id="2e5a8-117">Der dritte Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2e5a8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e5a8-118">PARAMETERS</span></span>

### <span data-ttu-id="2e5a8-119">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-119">-TrafficManagerProfile</span></span>
<span data-ttu-id="2e5a8-120">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-120">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2e5a8-121">Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="2e5a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-122">-DefaultProfile</span></span>
<span data-ttu-id="2e5a8-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e5a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5a8-124">CommonParameters</span></span>
<span data-ttu-id="2e5a8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5a8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5a8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e5a8-127">INPUTS</span></span>

### <span data-ttu-id="2e5a8-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2e5a8-129">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2e5a8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e5a8-130">OUTPUTS</span></span>

### <span data-ttu-id="2e5a8-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2e5a8-132">Dieses Cmdlet gibt ein **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2e5a8-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2e5a8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e5a8-133">NOTES</span></span>

## <span data-ttu-id="2e5a8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e5a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e5a8-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2e5a8-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2e5a8-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2e5a8-137">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2e5a8-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2e5a8-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2e5a8-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e5a8-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)



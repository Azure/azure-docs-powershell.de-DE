---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501306"
---
# <span data-ttu-id="75588-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="75588-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75588-102">SYNOPSIS</span></span>
<span data-ttu-id="75588-103">Aktualisiert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="75588-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75588-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75588-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75588-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75588-105">DESCRIPTION</span></span>
<span data-ttu-id="75588-106">Das Cmdlet " **Satz-AzureRmTrafficManagerProfile** " aktualisiert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="75588-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="75588-107">Dieses Cmdlet aktualisiert die Einstellungen des Profils von einem lokalen Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="75588-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="75588-108">Sie können das Profilobjekt entweder mithilfe des *TrafficManagerProfile* -Parameters oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="75588-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="75588-109">Sie können ein lokales Objekt, das ein Profil darstellt, mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="75588-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="75588-110">Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzureRmTrafficManagerProfile** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="75588-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="75588-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75588-111">EXAMPLES</span></span>

### <span data-ttu-id="75588-112">Beispiel 1: Aktualisieren eines Profils</span><span class="sxs-lookup"><span data-stu-id="75588-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="75588-113">Der erste Befehl ruft ein Azure Traffic Manager-Profil mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="75588-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="75588-114">Der Befehl speichert das Profil lokal in der $TrafficManagerProfile-Variablen.</span><span class="sxs-lookup"><span data-stu-id="75588-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="75588-115">Der zweite Befehl ändert das Profil lokal.</span><span class="sxs-lookup"><span data-stu-id="75588-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="75588-116">Mit diesem Befehl wird das Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="75588-116">This command disables the profile.</span></span>

<span data-ttu-id="75588-117">Der dritte Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="75588-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="75588-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="75588-118">PARAMETERS</span></span>

### <span data-ttu-id="75588-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75588-119">-DefaultProfile</span></span>
<span data-ttu-id="75588-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75588-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75588-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="75588-122">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75588-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="75588-123">Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="75588-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75588-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75588-124">CommonParameters</span></span>
<span data-ttu-id="75588-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75588-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75588-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75588-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75588-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75588-127">INPUTS</span></span>

### <span data-ttu-id="75588-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="75588-129">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="75588-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="75588-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75588-130">OUTPUTS</span></span>

### <span data-ttu-id="75588-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="75588-132">Dieses Cmdlet gibt ein **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75588-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="75588-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="75588-133">NOTES</span></span>

## <span data-ttu-id="75588-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75588-134">RELATED LINKS</span></span>

[<span data-ttu-id="75588-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="75588-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="75588-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="75588-137">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="75588-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="75588-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="75588-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75588-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)



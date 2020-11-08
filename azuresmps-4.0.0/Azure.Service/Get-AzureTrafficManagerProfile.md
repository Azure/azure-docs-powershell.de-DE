---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005742"
---
# <span data-ttu-id="7a239-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="7a239-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a239-102">SYNOPSIS</span></span>
<span data-ttu-id="7a239-103">Ruft die Details eines Traffic Manager-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="7a239-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="7a239-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a239-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a239-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a239-105">DESCRIPTION</span></span>
<span data-ttu-id="7a239-106">Das Cmdlet " **Get-AzureTrafficManagerProfile** " Ruft die Details eines Microsoft Azure Traffic Manager-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="7a239-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7a239-107">Wenn Sie den Parameter *Name* nicht angeben, listet das Cmdlet die Datenverkehrs-Manager-Profile im aktuellen Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="7a239-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="7a239-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a239-108">EXAMPLES</span></span>

### <span data-ttu-id="7a239-109">Beispiel 1: Abrufen der Liste der Datenverkehrs-Manager-Profile in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="7a239-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="7a239-110">Dieser Befehl ruft die Liste der Datenverkehrs-Manager-Profile in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7a239-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="7a239-111">Beispiel 2: Abrufen eines Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="7a239-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="7a239-112">Dieser Befehl ruft das Traffic Manager-Profil mit dem Namen "myProfile" ab.</span><span class="sxs-lookup"><span data-stu-id="7a239-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="7a239-113">Beispiel 3: Hinzufügen eines Endpunkts zu einem Traffic Manager-Profil</span><span class="sxs-lookup"><span data-stu-id="7a239-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="7a239-114">Mit diesem Befehl wird ein Endpunkt zu einem Traffic Manager-Profil hinzugefügt und dann das Profil gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7a239-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="7a239-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a239-115">PARAMETERS</span></span>

### <span data-ttu-id="7a239-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7a239-116">-Name</span></span>
<span data-ttu-id="7a239-117">Gibt den Namen des abzurufenden Traffic Manager-Profils an.</span><span class="sxs-lookup"><span data-stu-id="7a239-117">Specifies the name of the Traffic Manager profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a239-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="7a239-118">-Profile</span></span>
<span data-ttu-id="7a239-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7a239-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7a239-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7a239-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a239-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a239-121">CommonParameters</span></span>
<span data-ttu-id="7a239-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a239-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a239-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a239-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a239-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a239-124">INPUTS</span></span>

## <span data-ttu-id="7a239-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a239-125">OUTPUTS</span></span>

### <span data-ttu-id="7a239-126">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="7a239-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="7a239-127">Dieses Cmdlet generiert ein Profilobjekt oder Objekte des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="7a239-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="7a239-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a239-128">NOTES</span></span>

## <span data-ttu-id="7a239-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a239-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a239-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a239-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="7a239-131">Deaktivieren-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="7a239-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="7a239-133">Neu – AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="7a239-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="7a239-135">Satz-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a239-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)



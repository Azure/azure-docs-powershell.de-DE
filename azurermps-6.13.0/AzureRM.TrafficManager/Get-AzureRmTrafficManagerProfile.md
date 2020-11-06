---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477590"
---
# <span data-ttu-id="2aaef-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="2aaef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2aaef-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaef-103">Ruft ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="2aaef-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aaef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aaef-104">SYNTAX</span></span>

### <span data-ttu-id="2aaef-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aaef-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2aaef-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aaef-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aaef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2aaef-107">DESCRIPTION</span></span>
<span data-ttu-id="2aaef-108">Das Cmdlet " **Get-AzureRmTrafficManagerProfile** " Ruft ein Azure Traffic Manager-Profil ab und gibt ein Objekt zurück, das dieses Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="2aaef-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="2aaef-109">Geben Sie ein Profil mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2aaef-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="2aaef-110">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets vornehmen.</span><span class="sxs-lookup"><span data-stu-id="2aaef-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="2aaef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2aaef-111">EXAMPLES</span></span>

### <span data-ttu-id="2aaef-112">Beispiel 1: Abrufen eines Profils</span><span class="sxs-lookup"><span data-stu-id="2aaef-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2aaef-113">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2aaef-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="2aaef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aaef-114">PARAMETERS</span></span>

### <span data-ttu-id="2aaef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-115">-DefaultProfile</span></span>
<span data-ttu-id="2aaef-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2aaef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aaef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2aaef-117">-Name</span></span>
<span data-ttu-id="2aaef-118">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2aaef-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaef-119">-ResourceGroupName</span></span>
<span data-ttu-id="2aaef-120">Gibt den Namen einer Ressourcengruppe an, die das Datenverkehrs-Manager-Profil enthält, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2aaef-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaef-121">CommonParameters</span></span>
<span data-ttu-id="2aaef-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaef-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aaef-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaef-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2aaef-124">INPUTS</span></span>

### <span data-ttu-id="2aaef-125">Keine</span><span class="sxs-lookup"><span data-stu-id="2aaef-125">None</span></span>
<span data-ttu-id="2aaef-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2aaef-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2aaef-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2aaef-127">OUTPUTS</span></span>

### <span data-ttu-id="2aaef-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2aaef-129">Dieses Cmdlet gibt ein **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2aaef-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2aaef-130">Sie können dieses Objekt ändern und dann Änderungen auf Traffic Manager mithilfe von " **AzureRmTrafficManagerProfile** " anwenden.</span><span class="sxs-lookup"><span data-stu-id="2aaef-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="2aaef-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2aaef-131">NOTES</span></span>

## <span data-ttu-id="2aaef-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2aaef-132">RELATED LINKS</span></span>

[<span data-ttu-id="2aaef-133">Deaktivieren-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2aaef-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2aaef-135">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2aaef-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2aaef-137">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2aaef-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500342"
---
# <span data-ttu-id="3efdb-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="3efdb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3efdb-102">SYNOPSIS</span></span>
<span data-ttu-id="3efdb-103">Ruft ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="3efdb-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3efdb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3efdb-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3efdb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3efdb-105">DESCRIPTION</span></span>
<span data-ttu-id="3efdb-106">Das Cmdlet " **Get-AzureRmTrafficManagerProfile** " Ruft ein Azure Traffic Manager-Profil ab und gibt ein Objekt zurück, das dieses Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="3efdb-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="3efdb-107">Geben Sie ein Profil mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3efdb-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="3efdb-108">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3efdb-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3efdb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3efdb-109">EXAMPLES</span></span>

### <span data-ttu-id="3efdb-110">Beispiel 1: Abrufen eines Profils</span><span class="sxs-lookup"><span data-stu-id="3efdb-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3efdb-111">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="3efdb-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="3efdb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3efdb-112">PARAMETERS</span></span>

### <span data-ttu-id="3efdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-113">-DefaultProfile</span></span>
<span data-ttu-id="3efdb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3efdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3efdb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3efdb-115">-Name</span></span>
<span data-ttu-id="3efdb-116">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3efdb-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3efdb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3efdb-117">-ResourceGroupName</span></span>
<span data-ttu-id="3efdb-118">Gibt den Namen einer Ressourcengruppe an, die das Datenverkehrs-Manager-Profil enthält, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3efdb-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3efdb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efdb-119">CommonParameters</span></span>
<span data-ttu-id="3efdb-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3efdb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efdb-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3efdb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efdb-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3efdb-122">INPUTS</span></span>

### <span data-ttu-id="3efdb-123">Keine</span><span class="sxs-lookup"><span data-stu-id="3efdb-123">None</span></span>
<span data-ttu-id="3efdb-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3efdb-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3efdb-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3efdb-125">OUTPUTS</span></span>

### <span data-ttu-id="3efdb-126">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3efdb-127">Dieses Cmdlet gibt ein **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3efdb-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3efdb-128">Sie können dieses Objekt ändern und dann Änderungen auf Traffic Manager mithilfe von " **AzureRmTrafficManagerProfile** " anwenden.</span><span class="sxs-lookup"><span data-stu-id="3efdb-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="3efdb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3efdb-129">NOTES</span></span>

## <span data-ttu-id="3efdb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3efdb-130">RELATED LINKS</span></span>

[<span data-ttu-id="3efdb-131">Deaktivieren-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3efdb-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3efdb-133">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3efdb-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3efdb-135">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3efdb-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



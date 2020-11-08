---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007645"
---
# <span data-ttu-id="91668-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="91668-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91668-102">SYNOPSIS</span></span>
<span data-ttu-id="91668-103">Ruft ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="91668-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="91668-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91668-104">SYNTAX</span></span>

### <span data-ttu-id="91668-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="91668-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91668-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91668-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91668-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91668-107">DESCRIPTION</span></span>
<span data-ttu-id="91668-108">Das Cmdlet " **Get-AzTrafficManagerProfile** " Ruft ein Azure Traffic Manager-Profil ab und gibt ein Objekt zurück, das dieses Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="91668-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="91668-109">Geben Sie ein Profil mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="91668-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="91668-110">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzTrafficManagerProfile-Cmdlets vornehmen.</span><span class="sxs-lookup"><span data-stu-id="91668-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="91668-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91668-111">EXAMPLES</span></span>

### <span data-ttu-id="91668-112">Beispiel 1: Abrufen eines Profils</span><span class="sxs-lookup"><span data-stu-id="91668-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="91668-113">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="91668-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="91668-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="91668-114">PARAMETERS</span></span>

### <span data-ttu-id="91668-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91668-115">-DefaultProfile</span></span>
<span data-ttu-id="91668-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91668-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91668-117">-Name</span><span class="sxs-lookup"><span data-stu-id="91668-117">-Name</span></span>
<span data-ttu-id="91668-118">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="91668-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="91668-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91668-119">-ResourceGroupName</span></span>
<span data-ttu-id="91668-120">Gibt den Namen einer Ressourcengruppe an, die das Datenverkehrs-Manager-Profil enthält, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="91668-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="91668-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91668-121">CommonParameters</span></span>
<span data-ttu-id="91668-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91668-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91668-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91668-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91668-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91668-124">INPUTS</span></span>

### <span data-ttu-id="91668-125">System. String</span><span class="sxs-lookup"><span data-stu-id="91668-125">System.String</span></span>

## <span data-ttu-id="91668-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91668-126">OUTPUTS</span></span>

### <span data-ttu-id="91668-127">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="91668-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="91668-128">NOTES</span></span>

## <span data-ttu-id="91668-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91668-129">RELATED LINKS</span></span>

[<span data-ttu-id="91668-130">Deaktivieren-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="91668-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="91668-132">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="91668-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="91668-134">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91668-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



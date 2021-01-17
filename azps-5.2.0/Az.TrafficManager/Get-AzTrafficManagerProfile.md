---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291082"
---
# <span data-ttu-id="22f2a-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="22f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="22f2a-103">Ruft ein Datenverkehrs-Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="22f2a-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="22f2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22f2a-104">SYNTAX</span></span>

### <span data-ttu-id="22f2a-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="22f2a-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22f2a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22f2a-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22f2a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="22f2a-108">Das **Cmdlet "Get-AzTrafficManagerProfile"** ruft ein Azure Traffic Manager-Profil ab und gibt ein Objekt zurück, das dieses Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="22f2a-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="22f2a-109">Geben Sie ein Profil nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="22f2a-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="22f2a-110">Sie können dieses Objekt lokal ändern und dann änderungen am Profil mithilfe des Set-AzTrafficManagerProfile anwenden.</span><span class="sxs-lookup"><span data-stu-id="22f2a-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="22f2a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22f2a-111">EXAMPLES</span></span>

### <span data-ttu-id="22f2a-112">Beispiel 1: Profil erhalten</span><span class="sxs-lookup"><span data-stu-id="22f2a-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="22f2a-113">Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="22f2a-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="22f2a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f2a-114">PARAMETERS</span></span>

### <span data-ttu-id="22f2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-115">-DefaultProfile</span></span>
<span data-ttu-id="22f2a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22f2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22f2a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="22f2a-117">-Name</span></span>
<span data-ttu-id="22f2a-118">Gibt den Namen des Traffic-Manager-Profils an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="22f2a-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="22f2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="22f2a-120">Gibt den Namen einer Ressourcengruppe an, die das Datenverkehrs-Manager-Profil enthält, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="22f2a-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="22f2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f2a-121">CommonParameters</span></span>
<span data-ttu-id="22f2a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f2a-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22f2a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f2a-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22f2a-124">INPUTS</span></span>

### <span data-ttu-id="22f2a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="22f2a-125">System.String</span></span>

## <span data-ttu-id="22f2a-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22f2a-126">OUTPUTS</span></span>

### <span data-ttu-id="22f2a-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="22f2a-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22f2a-128">NOTES</span></span>

## <span data-ttu-id="22f2a-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22f2a-129">RELATED LINKS</span></span>

[<span data-ttu-id="22f2a-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="22f2a-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="22f2a-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="22f2a-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="22f2a-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



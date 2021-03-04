---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: 3d843729a9ab51e5a4e1ecf1952f778537e8bf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936475"
---
# <span data-ttu-id="0a4ff-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="0a4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4ff-103">Ruft ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="0a4ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a4ff-104">SYNTAX</span></span>

### <span data-ttu-id="0a4ff-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a4ff-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a4ff-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a4ff-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a4ff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a4ff-107">DESCRIPTION</span></span>
<span data-ttu-id="0a4ff-108">Das **Get-AzTrafficManagerProfile-Cmdlet** ruft ein Azure Traffic Manager-Profil ab und gibt ein -Objekt zurück, das dieses Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="0a4ff-109">Geben Sie ein Profil nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="0a4ff-110">Sie können dieses Objekt lokal ändern und dann Änderungen auf das Profil anwenden, indem Sie das cmdlet Set-AzTrafficManagerProfile verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="0a4ff-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a4ff-111">EXAMPLES</span></span>

### <span data-ttu-id="0a4ff-112">Beispiel 1: Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="0a4ff-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0a4ff-113">Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="0a4ff-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0a4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="0a4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="0a4ff-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a4ff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0a4ff-117">-Name</span></span>
<span data-ttu-id="0a4ff-118">Gibt den Namen des Traffic Manager-Profils an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a4ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a4ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a4ff-120">Gibt den Namen einer Ressourcengruppe an, die das Traffic Manager-Profil enthält, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a4ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4ff-121">CommonParameters</span></span>
<span data-ttu-id="0a4ff-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4ff-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a4ff-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4ff-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a4ff-124">INPUTS</span></span>

### <span data-ttu-id="0a4ff-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0a4ff-125">System.String</span></span>

## <span data-ttu-id="0a4ff-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a4ff-126">OUTPUTS</span></span>

### <span data-ttu-id="0a4ff-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0a4ff-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0a4ff-128">NOTES</span></span>

## <span data-ttu-id="0a4ff-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0a4ff-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a4ff-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a4ff-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a4ff-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a4ff-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a4ff-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4ff-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



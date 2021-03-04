---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: 40bfe0d68df65b7535ec40a3cb27da1501f915c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936496"
---
# <span data-ttu-id="06d40-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="06d40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d40-102">SYNOPSIS</span></span>
<span data-ttu-id="06d40-103">Aktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="06d40-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="06d40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06d40-104">SYNTAX</span></span>

### <span data-ttu-id="06d40-105">Felder</span><span class="sxs-lookup"><span data-stu-id="06d40-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d40-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="06d40-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d40-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06d40-107">DESCRIPTION</span></span>
<span data-ttu-id="06d40-108">Das **Cmdlet Enable-AzTrafficManagerProfile** aktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="06d40-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="06d40-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="06d40-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="06d40-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="06d40-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="06d40-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06d40-111">EXAMPLES</span></span>

### <span data-ttu-id="06d40-112">Beispiel 1: Aktivieren eines nach Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="06d40-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="06d40-113">Mit diesem Befehl wird das Profil "ContosoProfile" in "ResourceGroup11" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="06d40-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="06d40-114">Beispiel 2: Aktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="06d40-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="06d40-115">Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="06d40-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="06d40-116">Der Befehl übergibt dieses Profil dann mithilfe des Pipelineoperators an das **Cmdlet Enable-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="06d40-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06d40-117">Dieses Cmdlet ermöglicht dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="06d40-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="06d40-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="06d40-118">PARAMETERS</span></span>

### <span data-ttu-id="06d40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-119">-DefaultProfile</span></span>
<span data-ttu-id="06d40-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06d40-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d40-121">-Name</span><span class="sxs-lookup"><span data-stu-id="06d40-121">-Name</span></span>
<span data-ttu-id="06d40-122">Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="06d40-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d40-123">-ResourceGroupName</span></span>
<span data-ttu-id="06d40-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="06d40-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="06d40-125">Dieses Cmdlet aktiviert ein Traffic Manager-Profil in der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="06d40-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d40-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="06d40-127">Gibt ein **TrafficManagerProfile-Objekt an,** das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06d40-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="06d40-128">Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06d40-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d40-129">CommonParameters</span></span>
<span data-ttu-id="06d40-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d40-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d40-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d40-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06d40-132">INPUTS</span></span>

### <span data-ttu-id="06d40-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="06d40-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06d40-134">OUTPUTS</span></span>

### <span data-ttu-id="06d40-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06d40-135">System.Boolean</span></span>

## <span data-ttu-id="06d40-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="06d40-136">NOTES</span></span>

## <span data-ttu-id="06d40-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="06d40-137">RELATED LINKS</span></span>

[<span data-ttu-id="06d40-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="06d40-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="06d40-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="06d40-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="06d40-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d40-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



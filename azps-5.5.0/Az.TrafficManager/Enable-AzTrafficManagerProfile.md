---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165489"
---
# <span data-ttu-id="9566d-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="9566d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9566d-102">SYNOPSIS</span></span>
<span data-ttu-id="9566d-103">Aktiviert ein Datenverkehrs-Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9566d-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="9566d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9566d-104">SYNTAX</span></span>

### <span data-ttu-id="9566d-105">Felder</span><span class="sxs-lookup"><span data-stu-id="9566d-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9566d-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="9566d-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9566d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9566d-107">DESCRIPTION</span></span>
<span data-ttu-id="9566d-108">Das **Cmdlet "Enable-AzTrafficManagerProfile"** aktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9566d-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9566d-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="9566d-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="9566d-110">Alternativ können Sie das Profil mit den Parametern *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="9566d-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="9566d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9566d-111">EXAMPLES</span></span>

### <span data-ttu-id="9566d-112">Beispiel 1: Aktivieren eines profils angegebenen Namens</span><span class="sxs-lookup"><span data-stu-id="9566d-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9566d-113">Mit diesem Befehl wird das Profil "ContosoProfile" in ResourceGroup11 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9566d-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="9566d-114">Beispiel 2: Aktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="9566d-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="9566d-115">Dieser Befehl ruft das Profil "ContosoProfile in ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="9566d-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9566d-116">Der Befehl übergibt dieses Profil dann mithilfe des Pipelineoperators an das **Cmdlet "Enable-AzTrafficManagerProfile".**</span><span class="sxs-lookup"><span data-stu-id="9566d-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9566d-117">Dieses Cmdlet aktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="9566d-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="9566d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9566d-118">PARAMETERS</span></span>

### <span data-ttu-id="9566d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-119">-DefaultProfile</span></span>
<span data-ttu-id="9566d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9566d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9566d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9566d-121">-Name</span></span>
<span data-ttu-id="9566d-122">Gibt den Namen des Datenverkehrs-Manager-Profils an, das von diesem Cmdlet aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9566d-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="9566d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9566d-123">-ResourceGroupName</span></span>
<span data-ttu-id="9566d-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9566d-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9566d-125">Dieses Cmdlet aktiviert ein Traffic -Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9566d-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9566d-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="9566d-127">Gibt ein zu **aktivierender "TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9566d-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="9566d-128">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile **TrafficManagerProfile,** um ein TrafficManagerProfile-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9566d-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9566d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9566d-129">CommonParameters</span></span>
<span data-ttu-id="9566d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9566d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9566d-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9566d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9566d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9566d-132">INPUTS</span></span>

### <span data-ttu-id="9566d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9566d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9566d-134">OUTPUTS</span></span>

### <span data-ttu-id="9566d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9566d-135">System.Boolean</span></span>

## <span data-ttu-id="9566d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9566d-136">NOTES</span></span>

## <span data-ttu-id="9566d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9566d-137">RELATED LINKS</span></span>

[<span data-ttu-id="9566d-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9566d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9566d-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="9566d-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="9566d-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9566d-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



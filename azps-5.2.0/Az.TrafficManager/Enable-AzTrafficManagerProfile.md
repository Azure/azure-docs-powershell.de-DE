---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291089"
---
# <span data-ttu-id="bf399-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="bf399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf399-102">SYNOPSIS</span></span>
<span data-ttu-id="bf399-103">Aktiviert ein Datenverkehrs-Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="bf399-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="bf399-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf399-104">SYNTAX</span></span>

### <span data-ttu-id="bf399-105">Felder</span><span class="sxs-lookup"><span data-stu-id="bf399-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf399-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="bf399-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf399-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf399-107">DESCRIPTION</span></span>
<span data-ttu-id="bf399-108">Das **Cmdlet "Enable-AzTrafficManagerProfile"** aktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="bf399-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bf399-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="bf399-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="bf399-110">Alternativ können Sie das Profil mit den Parametern *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="bf399-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bf399-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf399-111">EXAMPLES</span></span>

### <span data-ttu-id="bf399-112">Beispiel 1: Aktivieren eines profils angegebenen Namens</span><span class="sxs-lookup"><span data-stu-id="bf399-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="bf399-113">Mit diesem Befehl wird das Profil "ContosoProfile" in "ResourceGroup11" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf399-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="bf399-114">Beispiel 2: Aktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf399-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="bf399-115">Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="bf399-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bf399-116">Der Befehl übergibt dieses Profil dann mithilfe des Pipelineoperators an das **Cmdlet "Enable-AzTrafficManagerProfile".**</span><span class="sxs-lookup"><span data-stu-id="bf399-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf399-117">Dieses Cmdlet aktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="bf399-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="bf399-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf399-118">PARAMETERS</span></span>

### <span data-ttu-id="bf399-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-119">-DefaultProfile</span></span>
<span data-ttu-id="bf399-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf399-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf399-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bf399-121">-Name</span></span>
<span data-ttu-id="bf399-122">Gibt den Namen des Datenverkehrs-Manager-Profils an, das von diesem Cmdlet aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="bf399-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="bf399-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf399-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf399-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bf399-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bf399-125">Dieses Cmdlet aktiviert ein Traffic -Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf399-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf399-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="bf399-127">Gibt ein zu **aktivierendes "TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="bf399-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="bf399-128">Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf399-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bf399-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf399-129">CommonParameters</span></span>
<span data-ttu-id="bf399-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf399-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf399-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf399-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf399-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf399-132">INPUTS</span></span>

### <span data-ttu-id="bf399-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="bf399-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf399-134">OUTPUTS</span></span>

### <span data-ttu-id="bf399-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf399-135">System.Boolean</span></span>

## <span data-ttu-id="bf399-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf399-136">NOTES</span></span>

## <span data-ttu-id="bf399-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf399-137">RELATED LINKS</span></span>

[<span data-ttu-id="bf399-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf399-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf399-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf399-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf399-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf399-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



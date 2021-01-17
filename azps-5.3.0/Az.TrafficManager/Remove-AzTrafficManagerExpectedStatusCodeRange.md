---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382792"
---
# <span data-ttu-id="1394d-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="1394d-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="1394d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1394d-102">SYNOPSIS</span></span>
<span data-ttu-id="1394d-103">Entfernt einen erwarteten Statuscodebereich aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="1394d-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="1394d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1394d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1394d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1394d-105">DESCRIPTION</span></span>
<span data-ttu-id="1394d-106">Das **Cmdlet "Remove-AzTrafficManagerExpectedStatusCodeRange"** entfernt einen Bereich erwarteter Statuscodes aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="1394d-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1394d-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="1394d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="1394d-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="1394d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1394d-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="1394d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="1394d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1394d-110">EXAMPLES</span></span>

### <span data-ttu-id="1394d-111">Beispiel 1: Entfernen eines erwarteten Statuscodebereichs aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="1394d-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1394d-112">Der erste Befehl ruft mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ein Azure Traffic -Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="1394d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1394d-113">Der zweite Befehl entfernt einen erwarteten Statuscodebereich aus dem profil, das in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1394d-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1394d-114">Der letzte Befehl aktualisiert das Profil im Verkehrs-Manager so, dass es dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1394d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1394d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1394d-115">PARAMETERS</span></span>

### <span data-ttu-id="1394d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-116">-DefaultProfile</span></span>
<span data-ttu-id="1394d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1394d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1394d-118">-Min</span><span class="sxs-lookup"><span data-stu-id="1394d-118">-Min</span></span>
<span data-ttu-id="1394d-119">Gibt den niedrigsten Wert im Zu entfernenden Statuscodebereich an.</span><span class="sxs-lookup"><span data-stu-id="1394d-119">Specifies the lowest value in the status code range to be removed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1394d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="1394d-121">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1394d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1394d-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="1394d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1394d-123">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile **TrafficManagerProfile,** um ein TrafficManagerProfile-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1394d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1394d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1394d-124">-Confirm</span></span>
<span data-ttu-id="1394d-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1394d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1394d-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1394d-126">-WhatIf</span></span>
<span data-ttu-id="1394d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1394d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1394d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1394d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1394d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1394d-129">CommonParameters</span></span>
<span data-ttu-id="1394d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1394d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1394d-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1394d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1394d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1394d-132">INPUTS</span></span>

### <span data-ttu-id="1394d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1394d-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1394d-134">OUTPUTS</span></span>

### <span data-ttu-id="1394d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1394d-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1394d-136">NOTES</span></span>

## <span data-ttu-id="1394d-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1394d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1394d-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="1394d-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="1394d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1394d-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1394d-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

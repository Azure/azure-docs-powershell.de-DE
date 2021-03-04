---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936451"
---
# <span data-ttu-id="45349-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="45349-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="45349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45349-102">SYNOPSIS</span></span>
<span data-ttu-id="45349-103">Entfernt einen erwarteten Statuscodebereich aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="45349-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="45349-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45349-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45349-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45349-105">DESCRIPTION</span></span>
<span data-ttu-id="45349-106">Das **Cmdlet Remove-AzTrafficManagerExpectedStatusCodeRange** entfernt einen Bereich von erwarteten Statuscodes aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="45349-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="45349-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="45349-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="45349-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="45349-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="45349-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="45349-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="45349-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45349-110">EXAMPLES</span></span>

### <span data-ttu-id="45349-111">Beispiel 1: Entfernen eines erwarteten Statuscodebereichs aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="45349-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="45349-112">Der erste Befehl ruft mithilfe des **Get-AzTrafficManagerProfile-Cmdlets ein Azure Traffic Manager-Profil** ab.</span><span class="sxs-lookup"><span data-stu-id="45349-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="45349-113">Mit dem zweiten Befehl wird ein erwarteter Statuscodebereich aus dem profil entfernt, das in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="45349-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="45349-114">Der letzte Befehl aktualisiert das Profil in Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="45349-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="45349-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="45349-115">PARAMETERS</span></span>

### <span data-ttu-id="45349-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45349-116">-DefaultProfile</span></span>
<span data-ttu-id="45349-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45349-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45349-118">-Min</span><span class="sxs-lookup"><span data-stu-id="45349-118">-Min</span></span>
<span data-ttu-id="45349-119">Gibt den niedrigsten Wert im zu entfernenden Statuscodebereich an.</span><span class="sxs-lookup"><span data-stu-id="45349-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="45349-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45349-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="45349-121">Gibt ein lokales **TrafficManagerProfile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="45349-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="45349-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="45349-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="45349-123">Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45349-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="45349-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45349-124">-Confirm</span></span>
<span data-ttu-id="45349-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45349-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45349-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45349-126">-WhatIf</span></span>
<span data-ttu-id="45349-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45349-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45349-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45349-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45349-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45349-129">CommonParameters</span></span>
<span data-ttu-id="45349-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45349-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45349-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45349-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45349-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45349-132">INPUTS</span></span>

### <span data-ttu-id="45349-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45349-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="45349-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45349-134">OUTPUTS</span></span>

### <span data-ttu-id="45349-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45349-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="45349-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="45349-136">NOTES</span></span>

## <span data-ttu-id="45349-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="45349-137">RELATED LINKS</span></span>

[<span data-ttu-id="45349-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="45349-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="45349-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45349-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="45349-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45349-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

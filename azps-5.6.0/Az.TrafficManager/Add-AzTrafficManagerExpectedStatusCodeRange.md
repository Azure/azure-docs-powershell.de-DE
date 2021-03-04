---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 88755e6830342dc7636bdb0b338269c47bc23398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936520"
---
# <span data-ttu-id="a248c-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a248c-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="a248c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a248c-102">SYNOPSIS</span></span>
<span data-ttu-id="a248c-103">Fügt einem lokalen Traffic Manager-Profilobjekt einen erwarteten Statuscodebereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="a248c-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="a248c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a248c-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a248c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a248c-105">DESCRIPTION</span></span>
<span data-ttu-id="a248c-106">Das **Add-AzTrafficManagerExpectedStatusCodeRange-Cmdlet** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Bereich von erwarteten Statuscodes hinzu.</span><span class="sxs-lookup"><span data-stu-id="a248c-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a248c-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="a248c-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="a248c-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="a248c-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a248c-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="a248c-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a248c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a248c-110">EXAMPLES</span></span>

### <span data-ttu-id="a248c-111">Beispiel 1: Hinzufügen eines erwarteten Statuscodebereichs zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="a248c-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a248c-112">Der erste Befehl ruft mithilfe des **Get-AzTrafficManagerProfile-Cmdlets ein Azure Traffic Manager-Profil** ab.</span><span class="sxs-lookup"><span data-stu-id="a248c-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a248c-113">Mit dem Befehl wird das lokale Profil in der $TrafficManagerProfile gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a248c-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="a248c-114">Mit dem zweiten Befehl wird dem profil gespeicherten Profil ein erwarteter Statuscodebereich $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a248c-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a248c-115">Der letzte Befehl aktualisiert das Profil in Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a248c-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a248c-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a248c-116">PARAMETERS</span></span>

### <span data-ttu-id="a248c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-117">-DefaultProfile</span></span>
<span data-ttu-id="a248c-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a248c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a248c-119">-Max</span><span class="sxs-lookup"><span data-stu-id="a248c-119">-Max</span></span>
<span data-ttu-id="a248c-120">Gibt den höchsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a248c-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="a248c-121">-Min</span><span class="sxs-lookup"><span data-stu-id="a248c-121">-Min</span></span>
<span data-ttu-id="a248c-122">Gibt den niedrigsten Wert im statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a248c-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="a248c-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="a248c-124">Gibt ein lokales **TrafficManagerProfile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a248c-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a248c-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="a248c-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a248c-126">Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a248c-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a248c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a248c-127">-Confirm</span></span>
<span data-ttu-id="a248c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a248c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a248c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a248c-129">-WhatIf</span></span>
<span data-ttu-id="a248c-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a248c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a248c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a248c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a248c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a248c-132">CommonParameters</span></span>
<span data-ttu-id="a248c-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a248c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a248c-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a248c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a248c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a248c-135">INPUTS</span></span>

### <span data-ttu-id="a248c-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a248c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a248c-137">OUTPUTS</span></span>

### <span data-ttu-id="a248c-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a248c-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a248c-139">NOTES</span></span>

## <span data-ttu-id="a248c-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a248c-140">RELATED LINKS</span></span>

[<span data-ttu-id="a248c-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a248c-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="a248c-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a248c-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a248c-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

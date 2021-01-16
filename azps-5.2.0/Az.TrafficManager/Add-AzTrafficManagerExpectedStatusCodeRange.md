---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360575"
---
# <span data-ttu-id="9a377-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9a377-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="9a377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a377-102">SYNOPSIS</span></span>
<span data-ttu-id="9a377-103">Fügt einem lokalen Traffic-Manager-Profilobjekt einen erwarteten Statuscodebereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a377-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="9a377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a377-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a377-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a377-105">DESCRIPTION</span></span>
<span data-ttu-id="9a377-106">Das **Cmdlet "Add-AzTrafficManagerExpectedStatusCodeRange"** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Bereich erwarteter Statuscodes hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a377-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9a377-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="9a377-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9a377-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a377-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9a377-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="9a377-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9a377-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a377-110">EXAMPLES</span></span>

### <span data-ttu-id="9a377-111">Beispiel 1: Hinzufügen eines erwarteten Statuscodebereichs zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="9a377-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9a377-112">Der erste Befehl ruft mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ein Azure Traffic -Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="9a377-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9a377-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="9a377-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="9a377-114">Mit dem zweiten Befehl wird dem in der Datei gespeicherten Profil ein erwarteter Statuscodebereich $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9a377-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9a377-115">Der letzte Befehl aktualisiert das Profil in Traffic Manager so, dass es dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9a377-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9a377-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a377-116">PARAMETERS</span></span>

### <span data-ttu-id="9a377-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-117">-DefaultProfile</span></span>
<span data-ttu-id="9a377-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a377-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a377-119">-Max</span><span class="sxs-lookup"><span data-stu-id="9a377-119">-Max</span></span>
<span data-ttu-id="9a377-120">Gibt den höchsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a377-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9a377-121">-Min</span><span class="sxs-lookup"><span data-stu-id="9a377-121">-Min</span></span>
<span data-ttu-id="9a377-122">Gibt den niedrigsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a377-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9a377-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="9a377-124">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9a377-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9a377-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="9a377-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9a377-126">Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a377-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9a377-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a377-127">-Confirm</span></span>
<span data-ttu-id="9a377-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a377-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a377-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9a377-129">-WhatIf</span></span>
<span data-ttu-id="9a377-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a377-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a377-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a377-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a377-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a377-132">CommonParameters</span></span>
<span data-ttu-id="9a377-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a377-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a377-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a377-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a377-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a377-135">INPUTS</span></span>

### <span data-ttu-id="9a377-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9a377-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a377-137">OUTPUTS</span></span>

### <span data-ttu-id="9a377-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9a377-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9a377-139">NOTES</span></span>

## <span data-ttu-id="9a377-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9a377-140">RELATED LINKS</span></span>

[<span data-ttu-id="9a377-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9a377-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="9a377-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9a377-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9a377-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

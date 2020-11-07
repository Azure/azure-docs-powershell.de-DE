---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: c2758304f0140f5737a01611b18acf1449d0bb77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824604"
---
# <span data-ttu-id="9b3ad-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9b3ad-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="9b3ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3ad-103">Fügt einen erwarteten Statuscodebereich zu einem lokalen Traffic Manager-Profilobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="9b3ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b3ad-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b3ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3ad-106">Das Cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Bereich von erwarteten Statuscodes hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9b3ad-107">Sie können ein Profil mithilfe der Cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9b3ad-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9b3ad-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9b3ad-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b3ad-110">EXAMPLES</span></span>

### <span data-ttu-id="9b3ad-111">Beispiel 1: Hinzufügen eines erwarteten Statuscode Bereichs zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="9b3ad-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9b3ad-112">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9b3ad-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="9b3ad-114">Mit dem zweiten Befehl wird dem in $TrafficManagerProfile gespeicherten Profil ein erwarteter Statuscodebereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9b3ad-115">Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9b3ad-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b3ad-116">PARAMETERS</span></span>

### <span data-ttu-id="9b3ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-117">-DefaultProfile</span></span>
<span data-ttu-id="9b3ad-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b3ad-119">-Max</span><span class="sxs-lookup"><span data-stu-id="9b3ad-119">-Max</span></span>
<span data-ttu-id="9b3ad-120">Gibt den höchsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9b3ad-121">-Min</span><span class="sxs-lookup"><span data-stu-id="9b3ad-121">-Min</span></span>
<span data-ttu-id="9b3ad-122">Gibt den niedrigsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="9b3ad-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="9b3ad-124">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9b3ad-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9b3ad-126">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9b3ad-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b3ad-127">-Confirm</span></span>
<span data-ttu-id="9b3ad-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3ad-129">-WhatIf</span></span>
<span data-ttu-id="9b3ad-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b3ad-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3ad-132">CommonParameters</span></span>
<span data-ttu-id="9b3ad-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3ad-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3ad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3ad-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b3ad-135">INPUTS</span></span>

### <span data-ttu-id="9b3ad-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9b3ad-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b3ad-137">OUTPUTS</span></span>

### <span data-ttu-id="9b3ad-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9b3ad-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b3ad-139">NOTES</span></span>

## <span data-ttu-id="9b3ad-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b3ad-140">RELATED LINKS</span></span>

[<span data-ttu-id="9b3ad-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9b3ad-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="9b3ad-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9b3ad-143">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ad-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

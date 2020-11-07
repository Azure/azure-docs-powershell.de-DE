---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8f26030f726d472024dd788abb02e55f8eac4c6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827063"
---
# <span data-ttu-id="91431-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="91431-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="91431-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91431-102">SYNOPSIS</span></span>
<span data-ttu-id="91431-103">Entfernt einen erwarteten Statuscodebereich aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="91431-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="91431-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91431-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91431-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91431-105">DESCRIPTION</span></span>
<span data-ttu-id="91431-106">Das Cmdlet **Remove-AzTrafficManagerExpectedStatusCodeRange** entfernt einen Bereich von erwarteten Statuscodes aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="91431-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="91431-107">Sie können ein Profil mithilfe der Cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="91431-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="91431-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="91431-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="91431-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="91431-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="91431-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91431-110">EXAMPLES</span></span>

### <span data-ttu-id="91431-111">Beispiel 1: Entfernen eines erwarteten Statuscode Bereichs aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="91431-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="91431-112">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="91431-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="91431-113">Der zweite Befehl entfernt einen erwarteten Statuscodebereich aus dem Profil, das in $TrafficManagerProfile gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="91431-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="91431-114">Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="91431-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="91431-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="91431-115">PARAMETERS</span></span>

### <span data-ttu-id="91431-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91431-116">-DefaultProfile</span></span>
<span data-ttu-id="91431-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91431-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91431-118">-Min</span><span class="sxs-lookup"><span data-stu-id="91431-118">-Min</span></span>
<span data-ttu-id="91431-119">Gibt den niedrigsten Wert im Statuscodebereich an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91431-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="91431-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91431-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="91431-121">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="91431-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="91431-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="91431-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="91431-123">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91431-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="91431-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91431-124">-Confirm</span></span>
<span data-ttu-id="91431-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91431-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91431-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91431-126">-WhatIf</span></span>
<span data-ttu-id="91431-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91431-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91431-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91431-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91431-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91431-129">CommonParameters</span></span>
<span data-ttu-id="91431-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91431-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91431-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91431-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91431-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91431-132">INPUTS</span></span>

### <span data-ttu-id="91431-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91431-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="91431-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91431-134">OUTPUTS</span></span>

### <span data-ttu-id="91431-135">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91431-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="91431-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="91431-136">NOTES</span></span>

## <span data-ttu-id="91431-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91431-137">RELATED LINKS</span></span>

[<span data-ttu-id="91431-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="91431-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="91431-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91431-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="91431-140">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91431-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

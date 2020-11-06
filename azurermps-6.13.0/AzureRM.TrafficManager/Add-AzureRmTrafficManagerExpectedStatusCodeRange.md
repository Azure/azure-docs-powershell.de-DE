---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475870"
---
# <span data-ttu-id="eb346-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="eb346-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="eb346-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb346-102">SYNOPSIS</span></span>
<span data-ttu-id="eb346-103">Fügt einen erwarteten Statuscodebereich zu einem lokalen Traffic Manager-Profilobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb346-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb346-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb346-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb346-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb346-105">DESCRIPTION</span></span>
<span data-ttu-id="eb346-106">Das Cmdlet **Add-AzureRmTrafficManagerExpectedStatusCodeRange** fügt einem lokalen Azure Traffic Manager-Profilobjekt einen Bereich von erwarteten Statuscodes hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb346-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="eb346-107">Sie können ein Profil mithilfe der Cmdlets New-AzureRmTrafficManagerProfile oder Get-AzureRmTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="eb346-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="eb346-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="eb346-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="eb346-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="eb346-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="eb346-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb346-110">EXAMPLES</span></span>

### <span data-ttu-id="eb346-111">Beispiel 1: Hinzufügen eines erwarteten Statuscode Bereichs zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="eb346-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="eb346-112">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzureRmTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="eb346-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="eb346-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="eb346-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="eb346-114">Mit dem zweiten Befehl wird dem in $TrafficManagerProfile gespeicherten Profil ein erwarteter Statuscodebereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eb346-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="eb346-115">Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="eb346-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="eb346-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb346-116">PARAMETERS</span></span>

### <span data-ttu-id="eb346-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-117">-DefaultProfile</span></span>
<span data-ttu-id="eb346-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb346-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb346-119">-Max</span><span class="sxs-lookup"><span data-stu-id="eb346-119">-Max</span></span>
<span data-ttu-id="eb346-120">Gibt den höchsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb346-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="eb346-121">-Min</span><span class="sxs-lookup"><span data-stu-id="eb346-121">-Min</span></span>
<span data-ttu-id="eb346-122">Gibt den niedrigsten Wert im Statuscodebereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb346-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="eb346-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="eb346-124">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="eb346-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="eb346-125">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb346-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="eb346-126">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb346-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="eb346-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb346-127">-Confirm</span></span>
<span data-ttu-id="eb346-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb346-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb346-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb346-129">-WhatIf</span></span>
<span data-ttu-id="eb346-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb346-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb346-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb346-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb346-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb346-132">CommonParameters</span></span>
<span data-ttu-id="eb346-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb346-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb346-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb346-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb346-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb346-135">INPUTS</span></span>

### <span data-ttu-id="eb346-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="eb346-137">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb346-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="eb346-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb346-138">OUTPUTS</span></span>

### <span data-ttu-id="eb346-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="eb346-140">Dieses Cmdlet gibt ein geändertes **TrafficManagerProfile** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="eb346-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="eb346-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb346-141">NOTES</span></span>

## <span data-ttu-id="eb346-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb346-142">RELATED LINKS</span></span>

[<span data-ttu-id="eb346-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="eb346-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="eb346-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="eb346-145">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eb346-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

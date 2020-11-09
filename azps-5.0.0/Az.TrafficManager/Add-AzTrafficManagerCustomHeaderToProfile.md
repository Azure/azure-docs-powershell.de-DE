---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302873"
---
# <span data-ttu-id="3769f-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="3769f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3769f-102">SYNOPSIS</span></span>
<span data-ttu-id="3769f-103">Fügt benutzerdefinierte Kopfzeileninformationen zu einem lokalen Traffic Manager-Profilobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="3769f-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="3769f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3769f-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3769f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3769f-105">DESCRIPTION</span></span>
<span data-ttu-id="3769f-106">Mit dem Cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** werden benutzerdefinierte Headerinformationen zu einem lokalen Azure Traffic Manager-Profilobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3769f-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3769f-107">Sie können ein Profil mithilfe der Cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile abrufen.</span><span class="sxs-lookup"><span data-stu-id="3769f-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="3769f-108">Dieses Cmdlet funktioniert für das lokale Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="3769f-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3769f-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3769f-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3769f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3769f-110">EXAMPLES</span></span>

### <span data-ttu-id="3769f-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="3769f-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3769f-112">Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.</span><span class="sxs-lookup"><span data-stu-id="3769f-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3769f-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.</span><span class="sxs-lookup"><span data-stu-id="3769f-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="3769f-114">Mit dem zweiten Befehl werden benutzerdefinierte Headerinformationen zu dem in $TrafficManagerProfile gespeicherten Profil hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3769f-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3769f-115">Der endgültige Befehl aktualisiert das Profil im Traffic Manager so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.</span><span class="sxs-lookup"><span data-stu-id="3769f-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3769f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3769f-116">PARAMETERS</span></span>

### <span data-ttu-id="3769f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-117">-DefaultProfile</span></span>
<span data-ttu-id="3769f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3769f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3769f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3769f-119">-Name</span></span>
<span data-ttu-id="3769f-120">Gibt den Namen der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3769f-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3769f-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="3769f-122">Gibt ein lokales **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3769f-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3769f-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="3769f-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3769f-124">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3769f-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3769f-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="3769f-125">-Value</span></span>
<span data-ttu-id="3769f-126">Gibt den Wert der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3769f-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3769f-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3769f-127">-Confirm</span></span>
<span data-ttu-id="3769f-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3769f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3769f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3769f-129">-WhatIf</span></span>
<span data-ttu-id="3769f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3769f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3769f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3769f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3769f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3769f-132">CommonParameters</span></span>
<span data-ttu-id="3769f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3769f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3769f-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3769f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3769f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3769f-135">INPUTS</span></span>

### <span data-ttu-id="3769f-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3769f-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3769f-137">OUTPUTS</span></span>

### <span data-ttu-id="3769f-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3769f-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3769f-139">NOTES</span></span>

## <span data-ttu-id="3769f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3769f-140">RELATED LINKS</span></span>

[<span data-ttu-id="3769f-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="3769f-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3769f-143">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3769f-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

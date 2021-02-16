---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173465"
---
# <span data-ttu-id="f8b8d-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="f8b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b8d-103">Fügt einem lokalen Traffic-Manager-Profilobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f8b8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b8d-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8b8d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b8d-106">Das **Cmdlet "Add-AzTrafficManagerCustomHeaderToProfile"** fügt einem lokalen Azure Traffic Manager-Profilobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f8b8d-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f8b8d-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f8b8d-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f8b8d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8b8d-110">EXAMPLES</span></span>

### <span data-ttu-id="f8b8d-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="f8b8d-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f8b8d-112">Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ab.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f8b8d-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f8b8d-114">Der zweite Befehl fügt dem in der Datei gespeicherten Profil benutzerdefinierte Kopfzeileninformationen $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f8b8d-115">Der letzte Befehl aktualisiert das Profil im Verkehrs-Manager so, dass es dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f8b8d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b8d-116">PARAMETERS</span></span>

### <span data-ttu-id="f8b8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-117">-DefaultProfile</span></span>
<span data-ttu-id="f8b8d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b8d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f8b8d-119">-Name</span></span>
<span data-ttu-id="f8b8d-120">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f8b8d-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f8b8d-122">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f8b8d-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f8b8d-124">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile **TrafficManagerProfile,** um ein TrafficManagerProfile-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f8b8d-125">-Value</span><span class="sxs-lookup"><span data-stu-id="f8b8d-125">-Value</span></span>
<span data-ttu-id="f8b8d-126">Gibt den Wert der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f8b8d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8b8d-127">-Confirm</span></span>
<span data-ttu-id="f8b8d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b8d-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8b8d-129">-WhatIf</span></span>
<span data-ttu-id="f8b8d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8b8d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b8d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b8d-132">CommonParameters</span></span>
<span data-ttu-id="f8b8d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b8d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b8d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b8d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b8d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b8d-135">INPUTS</span></span>

### <span data-ttu-id="f8b8d-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f8b8d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b8d-137">OUTPUTS</span></span>

### <span data-ttu-id="f8b8d-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f8b8d-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8b8d-139">NOTES</span></span>

## <span data-ttu-id="f8b8d-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8b8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="f8b8d-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="f8b8d-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f8b8d-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8b8d-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382806"
---
# <span data-ttu-id="56713-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="56713-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="56713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56713-102">SYNOPSIS</span></span>
<span data-ttu-id="56713-103">Entfernt benutzerdefinierte Headerinformationen aus einem lokalen Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="56713-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="56713-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56713-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56713-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56713-105">DESCRIPTION</span></span>
<span data-ttu-id="56713-106">Das **Cmdlet "Remove-AzTrafficManagerCustomHeaderFromProfile"** entfernt benutzerdefinierte Headerinformationen aus einem lokalen Azure Traffic Manager-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="56713-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="56713-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="56713-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="56713-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="56713-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="56713-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="56713-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="56713-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56713-110">EXAMPLES</span></span>

### <span data-ttu-id="56713-111">Beispiel 1: Entfernen von benutzerdefinierten Kopfzeileninformationen aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="56713-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="56713-112">Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ab.</span><span class="sxs-lookup"><span data-stu-id="56713-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="56713-113">Mit dem zweiten Befehl werden benutzerdefinierte Kopfzeileninformationen aus dem Profil entfernt, das in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56713-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="56713-114">Der letzte Befehl aktualisiert das Profil im Verkehrs-Manager so, dass es dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56713-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="56713-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56713-115">PARAMETERS</span></span>

### <span data-ttu-id="56713-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56713-116">-DefaultProfile</span></span>
<span data-ttu-id="56713-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56713-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56713-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56713-118">-Name</span></span>
<span data-ttu-id="56713-119">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="56713-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="56713-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56713-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="56713-121">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="56713-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="56713-122">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="56713-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="56713-123">Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56713-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="56713-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56713-124">-Confirm</span></span>
<span data-ttu-id="56713-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56713-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56713-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56713-126">-WhatIf</span></span>
<span data-ttu-id="56713-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56713-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56713-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56713-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56713-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56713-129">CommonParameters</span></span>
<span data-ttu-id="56713-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56713-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56713-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56713-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56713-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56713-132">INPUTS</span></span>

### <span data-ttu-id="56713-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56713-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="56713-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56713-134">OUTPUTS</span></span>

### <span data-ttu-id="56713-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56713-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="56713-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56713-136">NOTES</span></span>

## <span data-ttu-id="56713-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56713-137">RELATED LINKS</span></span>

[<span data-ttu-id="56713-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="56713-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="56713-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56713-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="56713-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56713-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382988"
---
# <span data-ttu-id="d99de-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="d99de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d99de-102">SYNOPSIS</span></span>
<span data-ttu-id="d99de-103">Fügt einem lokalen Traffic-Manager-Profilobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d99de-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d99de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d99de-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d99de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d99de-105">DESCRIPTION</span></span>
<span data-ttu-id="d99de-106">Das **Cmdlet "Add-AzTrafficManagerCustomHeaderToProfile"** fügt einem lokalen Azure Traffic Manager-Profilobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d99de-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d99de-107">Sie können ein Profil mithilfe der cmdlets New-AzTrafficManagerProfile oder Get-AzTrafficManagerProfile erhalten.</span><span class="sxs-lookup"><span data-stu-id="d99de-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="d99de-108">Dieses Cmdlet wird für das lokale Profilobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="d99de-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d99de-109">Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.</span><span class="sxs-lookup"><span data-stu-id="d99de-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="d99de-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d99de-110">EXAMPLES</span></span>

### <span data-ttu-id="d99de-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Profil</span><span class="sxs-lookup"><span data-stu-id="d99de-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d99de-112">Der erste Befehl ruft mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ein Azure Traffic -Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="d99de-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d99de-113">Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.</span><span class="sxs-lookup"><span data-stu-id="d99de-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="d99de-114">Der zweite Befehl fügt dem in der Datei gespeicherten Profil benutzerdefinierte Kopfzeileninformationen $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d99de-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d99de-115">Der letzte Befehl aktualisiert das Profil in Traffic Manager so, dass es dem lokalen Wert in der $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d99de-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d99de-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d99de-116">PARAMETERS</span></span>

### <span data-ttu-id="d99de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-117">-DefaultProfile</span></span>
<span data-ttu-id="d99de-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d99de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d99de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d99de-119">-Name</span></span>
<span data-ttu-id="d99de-120">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d99de-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d99de-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="d99de-122">Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d99de-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d99de-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="d99de-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d99de-124">Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d99de-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d99de-125">-Value</span><span class="sxs-lookup"><span data-stu-id="d99de-125">-Value</span></span>
<span data-ttu-id="d99de-126">Gibt den Wert der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d99de-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d99de-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d99de-127">-Confirm</span></span>
<span data-ttu-id="d99de-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d99de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d99de-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d99de-129">-WhatIf</span></span>
<span data-ttu-id="d99de-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d99de-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d99de-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d99de-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d99de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99de-132">CommonParameters</span></span>
<span data-ttu-id="d99de-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d99de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99de-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99de-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99de-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d99de-135">INPUTS</span></span>

### <span data-ttu-id="d99de-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d99de-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d99de-137">OUTPUTS</span></span>

### <span data-ttu-id="d99de-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d99de-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d99de-139">NOTES</span></span>

## <span data-ttu-id="d99de-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d99de-140">RELATED LINKS</span></span>

[<span data-ttu-id="d99de-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="d99de-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d99de-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d99de-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

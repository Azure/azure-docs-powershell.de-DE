---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375820"
---
# <span data-ttu-id="c9807-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c9807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9807-102">SYNOPSIS</span></span>
<span data-ttu-id="c9807-103">Löscht ein Datenverkehrs-Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c9807-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="c9807-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9807-104">SYNTAX</span></span>

### <span data-ttu-id="c9807-105">Felder</span><span class="sxs-lookup"><span data-stu-id="c9807-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9807-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="c9807-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9807-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9807-107">DESCRIPTION</span></span>
<span data-ttu-id="c9807-108">Das **Cmdlet "Remove-AzTrafficManagerProfile"** löscht ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c9807-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c9807-109">Geben Sie das zu löschende Profil mithilfe der *Parameter "Name"* und *"ResourceGroupName"* an.</span><span class="sxs-lookup"><span data-stu-id="c9807-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="c9807-110">Alternativ können Sie ein **"TrafficManagerProfile"-Objekt** mit dem *Parameter "TrafficManagerProfile"* angeben oder die Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9807-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="c9807-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9807-111">EXAMPLES</span></span>

### <span data-ttu-id="c9807-112">Beispiel 1: Löschen eines profils angegebenen Namens</span><span class="sxs-lookup"><span data-stu-id="c9807-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c9807-113">Mit diesem Befehl wird das Profil "ContosoProfile" in "ResourceGroup11" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c9807-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c9807-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c9807-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c9807-115">Beispiel 2: Löschen eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c9807-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="c9807-116">Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="c9807-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c9807-117">Der Befehl übergibt dieses Profil dann mithilfe des Pipelineoperators an das **Cmdlet "Remove-AzTrafficManagerProfile".**</span><span class="sxs-lookup"><span data-stu-id="c9807-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c9807-118">Dieses Cmdlet löscht dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="c9807-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="c9807-119">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="c9807-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c9807-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c9807-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c9807-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9807-121">PARAMETERS</span></span>

### <span data-ttu-id="c9807-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-122">-DefaultProfile</span></span>
<span data-ttu-id="c9807-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9807-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9807-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c9807-124">-Force</span></span>
<span data-ttu-id="c9807-125">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c9807-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c9807-126">-Name</span></span>
<span data-ttu-id="c9807-127">Gibt den Namen des Datenverkehrs-Manager-Profils an, das von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c9807-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9807-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9807-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9807-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c9807-130">Dieses Cmdlet löscht ein Datenverkehrs-Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c9807-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="c9807-132">Gibt ein zu **löschendes "TrafficManagerProfile"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c9807-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="c9807-133">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile **TrafficManagerProfile,** um ein TrafficManagerProfile-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9807-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9807-134">-Confirm</span></span>
<span data-ttu-id="c9807-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9807-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c9807-136">-WhatIf</span></span>
<span data-ttu-id="c9807-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9807-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9807-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9807-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9807-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9807-139">CommonParameters</span></span>
<span data-ttu-id="c9807-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9807-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9807-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9807-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9807-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9807-142">INPUTS</span></span>

### <span data-ttu-id="c9807-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c9807-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9807-144">OUTPUTS</span></span>

### <span data-ttu-id="c9807-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9807-145">System.Boolean</span></span>

## <span data-ttu-id="c9807-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c9807-146">NOTES</span></span>

## <span data-ttu-id="c9807-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c9807-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9807-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c9807-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c9807-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c9807-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c9807-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9807-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



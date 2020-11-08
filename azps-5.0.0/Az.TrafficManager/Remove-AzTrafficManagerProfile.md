---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178646"
---
# <span data-ttu-id="f7780-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f7780-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7780-102">SYNOPSIS</span></span>
<span data-ttu-id="f7780-103">Löscht ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="f7780-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="f7780-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7780-104">SYNTAX</span></span>

### <span data-ttu-id="f7780-105">Felder</span><span class="sxs-lookup"><span data-stu-id="f7780-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7780-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="f7780-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7780-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7780-107">DESCRIPTION</span></span>
<span data-ttu-id="f7780-108">Das Cmdlet **Remove-AzTrafficManagerProfile** löscht ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="f7780-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f7780-109">Geben Sie das zu löschende Profil mithilfe der Parameter *Name* und *ResourceGroupName* an.</span><span class="sxs-lookup"><span data-stu-id="f7780-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f7780-110">Sie können auch ein **TrafficManagerProfile** -Objekt mit dem *TrafficManagerProfile* -Parameter angeben, oder Sie können die Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7780-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="f7780-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7780-111">EXAMPLES</span></span>

### <span data-ttu-id="f7780-112">Beispiel 1: Löschen eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="f7780-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f7780-113">Dieser Befehl löscht das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f7780-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f7780-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="f7780-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f7780-115">Beispiel 2: Löschen eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f7780-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="f7780-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="f7780-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f7780-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Remove-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f7780-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f7780-118">Dieses Cmdlet löscht dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="f7780-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="f7780-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="f7780-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f7780-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f7780-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f7780-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7780-121">PARAMETERS</span></span>

### <span data-ttu-id="f7780-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-122">-DefaultProfile</span></span>
<span data-ttu-id="f7780-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7780-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7780-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f7780-124">-Force</span></span>
<span data-ttu-id="f7780-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f7780-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7780-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f7780-126">-Name</span></span>
<span data-ttu-id="f7780-127">Gibt den Namen des Traffic Manager-Profils an, das vom Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f7780-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f7780-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7780-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7780-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7780-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f7780-130">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe gelöscht, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f7780-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7780-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="f7780-132">Gibt ein **TrafficManagerProfile** -Objekt an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7780-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="f7780-133">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7780-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f7780-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7780-134">-Confirm</span></span>
<span data-ttu-id="f7780-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7780-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7780-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7780-136">-WhatIf</span></span>
<span data-ttu-id="f7780-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7780-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7780-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7780-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7780-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7780-139">CommonParameters</span></span>
<span data-ttu-id="f7780-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7780-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7780-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7780-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7780-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7780-142">INPUTS</span></span>

### <span data-ttu-id="f7780-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f7780-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7780-144">OUTPUTS</span></span>

### <span data-ttu-id="f7780-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7780-145">System.Boolean</span></span>

## <span data-ttu-id="f7780-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7780-146">NOTES</span></span>

## <span data-ttu-id="f7780-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7780-147">RELATED LINKS</span></span>

[<span data-ttu-id="f7780-148">Deaktivieren-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f7780-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f7780-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f7780-151">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="f7780-152">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7780-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



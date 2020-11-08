---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996347"
---
# <span data-ttu-id="8d554-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="8d554-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d554-102">SYNOPSIS</span></span>
<span data-ttu-id="8d554-103">Deaktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="8d554-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="8d554-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d554-104">SYNTAX</span></span>

### <span data-ttu-id="8d554-105">Felder</span><span class="sxs-lookup"><span data-stu-id="8d554-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d554-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="8d554-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d554-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d554-107">DESCRIPTION</span></span>
<span data-ttu-id="8d554-108">Das Cmdlet **Disable-AzTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="8d554-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8d554-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="8d554-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="8d554-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="8d554-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8d554-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d554-111">EXAMPLES</span></span>

### <span data-ttu-id="8d554-112">Beispiel 1: Deaktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="8d554-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8d554-113">Dieser Befehl deaktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8d554-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8d554-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="8d554-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8d554-115">Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8d554-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="8d554-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="8d554-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8d554-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Disable-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="8d554-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8d554-118">Dieses Cmdlet deaktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="8d554-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="8d554-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="8d554-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8d554-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8d554-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8d554-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d554-121">PARAMETERS</span></span>

### <span data-ttu-id="8d554-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-122">-DefaultProfile</span></span>
<span data-ttu-id="8d554-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d554-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d554-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8d554-124">-Force</span></span>
<span data-ttu-id="8d554-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8d554-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d554-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8d554-126">-Name</span></span>
<span data-ttu-id="8d554-127">Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="8d554-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8d554-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d554-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d554-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8d554-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8d554-130">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe deaktiviert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8d554-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d554-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="8d554-132">Gibt ein zu deaktivierenden **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8d554-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="8d554-133">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d554-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8d554-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d554-134">-Confirm</span></span>
<span data-ttu-id="8d554-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d554-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d554-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d554-136">-WhatIf</span></span>
<span data-ttu-id="8d554-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d554-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d554-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d554-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d554-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d554-139">CommonParameters</span></span>
<span data-ttu-id="8d554-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d554-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d554-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d554-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d554-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d554-142">INPUTS</span></span>

### <span data-ttu-id="8d554-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8d554-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d554-144">OUTPUTS</span></span>

### <span data-ttu-id="8d554-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d554-145">System.Boolean</span></span>

## <span data-ttu-id="8d554-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d554-146">NOTES</span></span>

## <span data-ttu-id="8d554-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d554-147">RELATED LINKS</span></span>

[<span data-ttu-id="8d554-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="8d554-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8d554-150">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8d554-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="8d554-152">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8d554-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



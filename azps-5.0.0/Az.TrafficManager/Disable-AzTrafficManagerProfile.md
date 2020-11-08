---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179480"
---
# <span data-ttu-id="cf610-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="cf610-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf610-102">SYNOPSIS</span></span>
<span data-ttu-id="cf610-103">Deaktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="cf610-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="cf610-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf610-104">SYNTAX</span></span>

### <span data-ttu-id="cf610-105">Felder</span><span class="sxs-lookup"><span data-stu-id="cf610-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf610-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="cf610-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf610-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf610-107">DESCRIPTION</span></span>
<span data-ttu-id="cf610-108">Das Cmdlet **Disable-AzTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="cf610-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="cf610-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="cf610-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="cf610-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="cf610-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="cf610-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf610-111">EXAMPLES</span></span>

### <span data-ttu-id="cf610-112">Beispiel 1: Deaktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="cf610-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="cf610-113">Dieser Befehl deaktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cf610-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="cf610-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="cf610-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="cf610-115">Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="cf610-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="cf610-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="cf610-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="cf610-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Disable-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="cf610-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cf610-118">Dieses Cmdlet deaktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="cf610-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="cf610-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="cf610-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cf610-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="cf610-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cf610-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf610-121">PARAMETERS</span></span>

### <span data-ttu-id="cf610-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-122">-DefaultProfile</span></span>
<span data-ttu-id="cf610-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf610-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf610-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cf610-124">-Force</span></span>
<span data-ttu-id="cf610-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cf610-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf610-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cf610-126">-Name</span></span>
<span data-ttu-id="cf610-127">Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="cf610-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="cf610-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf610-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf610-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cf610-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cf610-130">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe deaktiviert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cf610-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf610-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="cf610-132">Gibt ein zu deaktivierenden **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cf610-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="cf610-133">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf610-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="cf610-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf610-134">-Confirm</span></span>
<span data-ttu-id="cf610-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf610-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf610-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf610-136">-WhatIf</span></span>
<span data-ttu-id="cf610-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf610-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf610-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf610-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf610-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf610-139">CommonParameters</span></span>
<span data-ttu-id="cf610-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf610-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf610-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf610-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf610-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf610-142">INPUTS</span></span>

### <span data-ttu-id="cf610-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="cf610-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf610-144">OUTPUTS</span></span>

### <span data-ttu-id="cf610-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf610-145">System.Boolean</span></span>

## <span data-ttu-id="cf610-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf610-146">NOTES</span></span>

## <span data-ttu-id="cf610-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf610-147">RELATED LINKS</span></span>

[<span data-ttu-id="cf610-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="cf610-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="cf610-150">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="cf610-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="cf610-152">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf610-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



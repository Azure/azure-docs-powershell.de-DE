---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: c3a32c6bab916ad4a63db5e528e00fe3948a1d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662762"
---
# <span data-ttu-id="7f6b7-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="7f6b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6b7-103">Deaktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f6b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f6b7-104">SYNTAX</span></span>

### <span data-ttu-id="7f6b7-105">Felder</span><span class="sxs-lookup"><span data-stu-id="7f6b7-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6b7-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="7f6b7-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f6b7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f6b7-107">DESCRIPTION</span></span>
<span data-ttu-id="7f6b7-108">Das Cmdlet **Disable-AzureRmTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7f6b7-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="7f6b7-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7f6b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f6b7-111">EXAMPLES</span></span>

### <span data-ttu-id="7f6b7-112">Beispiel 1: Deaktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="7f6b7-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7f6b7-113">Dieser Befehl deaktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7f6b7-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7f6b7-115">Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7f6b7-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="7f6b7-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7f6b7-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Disable-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="7f6b7-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7f6b7-118">Dieses Cmdlet deaktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="7f6b7-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7f6b7-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f6b7-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6b7-121">PARAMETERS</span></span>

### <span data-ttu-id="7f6b7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7f6b7-122">-Force</span></span>
<span data-ttu-id="7f6b7-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f6b7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7f6b7-124">-Name</span></span>
<span data-ttu-id="7f6b7-125">Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-125">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7f6b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f6b7-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7f6b7-128">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe deaktiviert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-128">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f6b7-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="7f6b7-130">Gibt ein zu deaktivierenden **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-130">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="7f6b7-131">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7f6b7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f6b7-132">-Confirm</span></span>
<span data-ttu-id="7f6b7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6b7-134">-WhatIf</span></span>
<span data-ttu-id="7f6b7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6b7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6b7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-137">-DefaultProfile</span></span>
<span data-ttu-id="7f6b7-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6b7-139">CommonParameters</span></span>
<span data-ttu-id="7f6b7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6b7-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6b7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6b7-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f6b7-142">INPUTS</span></span>

### <span data-ttu-id="7f6b7-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7f6b7-144">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f6b7-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="7f6b7-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f6b7-145">OUTPUTS</span></span>

### <span data-ttu-id="7f6b7-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f6b7-146">System.Boolean</span></span>

## <span data-ttu-id="7f6b7-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f6b7-147">NOTES</span></span>

## <span data-ttu-id="7f6b7-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f6b7-148">RELATED LINKS</span></span>

[<span data-ttu-id="7f6b7-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f6b7-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f6b7-151">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f6b7-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7f6b7-153">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b7-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



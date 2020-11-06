---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482645"
---
# <span data-ttu-id="9db63-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="9db63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9db63-102">SYNOPSIS</span></span>
<span data-ttu-id="9db63-103">Löscht ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9db63-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db63-104">SYNTAX</span></span>

### <span data-ttu-id="9db63-105">Felder</span><span class="sxs-lookup"><span data-stu-id="9db63-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9db63-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="9db63-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db63-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9db63-107">DESCRIPTION</span></span>
<span data-ttu-id="9db63-108">Das Cmdlet **Remove-AzureRmTrafficManagerProfile** löscht ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="9db63-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9db63-109">Geben Sie das zu löschende Profil mithilfe der Parameter *Name* und *ResourceGroupName* an.</span><span class="sxs-lookup"><span data-stu-id="9db63-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9db63-110">Sie können auch ein **TrafficManagerProfile** -Objekt mit dem *TrafficManagerProfile* -Parameter angeben, oder Sie können die Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="9db63-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="9db63-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9db63-111">EXAMPLES</span></span>

### <span data-ttu-id="9db63-112">Beispiel 1: Löschen eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="9db63-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9db63-113">Dieser Befehl löscht das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9db63-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9db63-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="9db63-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9db63-115">Beispiel 2: Löschen eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="9db63-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="9db63-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="9db63-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9db63-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Remove-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9db63-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9db63-118">Dieses Cmdlet löscht dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="9db63-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="9db63-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="9db63-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9db63-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9db63-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9db63-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="9db63-121">PARAMETERS</span></span>

### <span data-ttu-id="9db63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-122">-DefaultProfile</span></span>
<span data-ttu-id="9db63-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9db63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9db63-124">-Force</span></span>
<span data-ttu-id="9db63-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9db63-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9db63-126">-Name</span></span>
<span data-ttu-id="9db63-127">Gibt den Namen des Traffic Manager-Profils an, das vom Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9db63-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db63-128">-ResourceGroupName</span></span>
<span data-ttu-id="9db63-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9db63-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9db63-130">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe gelöscht, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9db63-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="9db63-132">Gibt ein **TrafficManagerProfile** -Objekt an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9db63-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="9db63-133">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9db63-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9db63-134">-Confirm</span></span>
<span data-ttu-id="9db63-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9db63-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db63-136">-WhatIf</span></span>
<span data-ttu-id="9db63-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9db63-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db63-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9db63-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db63-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db63-139">CommonParameters</span></span>
<span data-ttu-id="9db63-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db63-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db63-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db63-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db63-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9db63-142">INPUTS</span></span>

### <span data-ttu-id="9db63-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9db63-144">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9db63-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9db63-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9db63-145">OUTPUTS</span></span>

### <span data-ttu-id="9db63-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="9db63-146">Boolean</span></span>
<span data-ttu-id="9db63-147">Dieses Cmdlet gibt einen Wert von $true zurück, wenn es erfolgreich ist, oder, wenn der Löschvorgang fehlschlägt, den Wert $false.</span><span class="sxs-lookup"><span data-stu-id="9db63-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="9db63-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="9db63-148">NOTES</span></span>

## <span data-ttu-id="9db63-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9db63-149">RELATED LINKS</span></span>

[<span data-ttu-id="9db63-150">Deaktivieren-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9db63-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9db63-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9db63-153">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9db63-154">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db63-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



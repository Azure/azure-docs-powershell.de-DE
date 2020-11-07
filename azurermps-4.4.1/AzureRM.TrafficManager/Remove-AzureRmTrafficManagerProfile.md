---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 01a82084ddcea5fc3a5a3c412b7b6ea20dfcaa02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663287"
---
# <span data-ttu-id="c2479-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="c2479-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2479-102">SYNOPSIS</span></span>
<span data-ttu-id="c2479-103">Löscht ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c2479-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2479-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2479-104">SYNTAX</span></span>

### <span data-ttu-id="c2479-105">Felder</span><span class="sxs-lookup"><span data-stu-id="c2479-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2479-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="c2479-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2479-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2479-107">DESCRIPTION</span></span>
<span data-ttu-id="c2479-108">Das Cmdlet **Remove-AzureRmTrafficManagerProfile** löscht ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c2479-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c2479-109">Geben Sie das zu löschende Profil mithilfe der Parameter *Name* und *ResourceGroupName* an.</span><span class="sxs-lookup"><span data-stu-id="c2479-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="c2479-110">Sie können auch ein **TrafficManagerProfile** -Objekt mit dem *TrafficManagerProfile* -Parameter angeben, oder Sie können die Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2479-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="c2479-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2479-111">EXAMPLES</span></span>

### <span data-ttu-id="c2479-112">Beispiel 1: Löschen eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="c2479-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c2479-113">Dieser Befehl löscht das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c2479-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c2479-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c2479-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c2479-115">Beispiel 2: Löschen eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2479-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="c2479-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="c2479-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c2479-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Remove-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c2479-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c2479-118">Dieses Cmdlet löscht dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="c2479-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="c2479-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="c2479-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c2479-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c2479-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c2479-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2479-121">PARAMETERS</span></span>

### <span data-ttu-id="c2479-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c2479-122">-Force</span></span>
<span data-ttu-id="c2479-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c2479-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2479-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c2479-124">-Name</span></span>
<span data-ttu-id="c2479-125">Gibt den Namen des Traffic Manager-Profils an, das vom Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c2479-125">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c2479-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2479-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2479-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c2479-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c2479-128">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe gelöscht, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c2479-128">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2479-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="c2479-130">Gibt ein **TrafficManagerProfile** -Objekt an, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2479-130">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="c2479-131">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2479-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c2479-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2479-132">-Confirm</span></span>
<span data-ttu-id="c2479-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2479-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2479-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2479-134">-WhatIf</span></span>
<span data-ttu-id="c2479-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2479-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2479-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2479-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2479-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-137">-DefaultProfile</span></span>
<span data-ttu-id="c2479-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2479-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2479-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2479-139">CommonParameters</span></span>
<span data-ttu-id="c2479-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2479-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2479-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2479-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2479-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2479-142">INPUTS</span></span>

### <span data-ttu-id="c2479-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c2479-144">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2479-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="c2479-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2479-145">OUTPUTS</span></span>

### <span data-ttu-id="c2479-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2479-146">Boolean</span></span>
<span data-ttu-id="c2479-147">Dieses Cmdlet gibt einen Wert von $true zurück, wenn es erfolgreich ist, oder, wenn der Löschvorgang fehlschlägt, den Wert $false.</span><span class="sxs-lookup"><span data-stu-id="c2479-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="c2479-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2479-148">NOTES</span></span>

## <span data-ttu-id="c2479-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2479-149">RELATED LINKS</span></span>

[<span data-ttu-id="c2479-150">Deaktivieren-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c2479-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c2479-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c2479-153">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c2479-154">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2479-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



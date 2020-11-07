---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663408"
---
# <span data-ttu-id="822f4-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="822f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="822f4-102">SYNOPSIS</span></span>
<span data-ttu-id="822f4-103">Deaktiviert ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="822f4-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="822f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="822f4-104">SYNTAX</span></span>

### <span data-ttu-id="822f4-105">Felder</span><span class="sxs-lookup"><span data-stu-id="822f4-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822f4-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="822f4-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="822f4-107">DESCRIPTION</span></span>
<span data-ttu-id="822f4-108">Das Cmdlet **Disable-AzureRmTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="822f4-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="822f4-109">Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.</span><span class="sxs-lookup"><span data-stu-id="822f4-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="822f4-110">Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="822f4-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="822f4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="822f4-111">EXAMPLES</span></span>

### <span data-ttu-id="822f4-112">Beispiel 1: Deaktivieren eines durch den Namen angegebenen Profils</span><span class="sxs-lookup"><span data-stu-id="822f4-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="822f4-113">Dieser Befehl deaktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="822f4-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="822f4-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="822f4-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="822f4-115">Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="822f4-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="822f4-116">Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="822f4-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="822f4-117">Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Disable-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="822f4-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="822f4-118">Dieses Cmdlet deaktiviert dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="822f4-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="822f4-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="822f4-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="822f4-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="822f4-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="822f4-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="822f4-121">PARAMETERS</span></span>

### <span data-ttu-id="822f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-122">-DefaultProfile</span></span>
<span data-ttu-id="822f4-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="822f4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822f4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="822f4-124">-Force</span></span>
<span data-ttu-id="822f4-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="822f4-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="822f4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="822f4-126">-Name</span></span>
<span data-ttu-id="822f4-127">Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="822f4-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="822f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="822f4-129">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="822f4-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="822f4-130">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe deaktiviert, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="822f4-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="822f4-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="822f4-132">Gibt ein zu deaktivierenden **TrafficManagerProfile** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="822f4-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="822f4-133">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="822f4-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="822f4-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="822f4-134">-Confirm</span></span>
<span data-ttu-id="822f4-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="822f4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822f4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822f4-136">-WhatIf</span></span>
<span data-ttu-id="822f4-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="822f4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822f4-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="822f4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822f4-139">CommonParameters</span></span>
<span data-ttu-id="822f4-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822f4-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822f4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822f4-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="822f4-142">INPUTS</span></span>

### <span data-ttu-id="822f4-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="822f4-144">Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="822f4-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="822f4-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="822f4-145">OUTPUTS</span></span>

### <span data-ttu-id="822f4-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="822f4-146">System.Boolean</span></span>

## <span data-ttu-id="822f4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="822f4-147">NOTES</span></span>

## <span data-ttu-id="822f4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="822f4-148">RELATED LINKS</span></span>

[<span data-ttu-id="822f4-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="822f4-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="822f4-151">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="822f4-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="822f4-153">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="822f4-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



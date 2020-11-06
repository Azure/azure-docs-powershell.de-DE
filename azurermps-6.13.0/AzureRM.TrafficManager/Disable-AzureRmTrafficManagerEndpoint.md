---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: af05a91fe2281d457cff649bf0de6d986f7f413a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495578"
---
# <span data-ttu-id="b506a-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b506a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b506a-102">SYNOPSIS</span></span>
<span data-ttu-id="b506a-103">Deaktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b506a-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b506a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b506a-104">SYNTAX</span></span>

### <span data-ttu-id="b506a-105">Felder</span><span class="sxs-lookup"><span data-stu-id="b506a-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b506a-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="b506a-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b506a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b506a-107">DESCRIPTION</span></span>
<span data-ttu-id="b506a-108">Das Cmdlet **Disable-AzureRmTrafficManagerEndpoint** deaktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="b506a-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b506a-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint** -Objekt mit dem *TrafficManagerEndpoint* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b506a-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="b506a-110">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="b506a-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="b506a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b506a-111">EXAMPLES</span></span>

### <span data-ttu-id="b506a-112">Beispiel 1: Deaktivieren eines Endpunkts nach Name</span><span class="sxs-lookup"><span data-stu-id="b506a-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="b506a-113">Dieser Befehl deaktiviert den externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppen-ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b506a-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="b506a-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="b506a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b506a-115">Beispiel 2: Deaktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b506a-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="b506a-116">Dieser Befehl ruft den externen Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="b506a-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b506a-117">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das Cmdlet **Disable-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="b506a-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b506a-118">Dieses Cmdlet deaktiviert diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="b506a-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="b506a-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="b506a-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b506a-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b506a-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b506a-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="b506a-121">PARAMETERS</span></span>

### <span data-ttu-id="b506a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b506a-122">-DefaultProfile</span></span>
<span data-ttu-id="b506a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b506a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b506a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b506a-124">-Force</span></span>
<span data-ttu-id="b506a-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b506a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b506a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b506a-126">-Name</span></span>
<span data-ttu-id="b506a-127">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b506a-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="b506a-128">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b506a-128">-ProfileName</span></span>
<span data-ttu-id="b506a-129">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b506a-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="b506a-130">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b506a-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b506a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b506a-131">-ResourceGroupName</span></span>
<span data-ttu-id="b506a-132">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b506a-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b506a-133">Dieses Cmdlet deaktiviert einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b506a-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b506a-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b506a-135">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b506a-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="b506a-136">Verwenden Sie das Get-AzureRmTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b506a-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b506a-137">-Typ</span><span class="sxs-lookup"><span data-stu-id="b506a-137">-Type</span></span>
<span data-ttu-id="b506a-138">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b506a-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b506a-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b506a-139">Valid values are:</span></span> 

- <span data-ttu-id="b506a-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b506a-140">AzureEndpoints</span></span>
- <span data-ttu-id="b506a-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b506a-141">ExternalEndpoints</span></span>
- <span data-ttu-id="b506a-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b506a-142">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b506a-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b506a-143">-Confirm</span></span>
<span data-ttu-id="b506a-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b506a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b506a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b506a-145">-WhatIf</span></span>
<span data-ttu-id="b506a-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b506a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b506a-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b506a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b506a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b506a-148">CommonParameters</span></span>
<span data-ttu-id="b506a-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b506a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b506a-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b506a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b506a-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b506a-151">INPUTS</span></span>

### <span data-ttu-id="b506a-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="b506a-153">Der Parameter "TrafficManagerEndpoint" akzeptiert den Wert vom Typ "TrafficManagerEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b506a-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="b506a-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b506a-154">OUTPUTS</span></span>

### <span data-ttu-id="b506a-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b506a-155">System.Boolean</span></span>

## <span data-ttu-id="b506a-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="b506a-156">NOTES</span></span>

## <span data-ttu-id="b506a-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b506a-157">RELATED LINKS</span></span>

[<span data-ttu-id="b506a-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b506a-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b506a-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b506a-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b506a-161">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b506a-162">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b506a-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b506a-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b506a-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="b506a-164">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b506a-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



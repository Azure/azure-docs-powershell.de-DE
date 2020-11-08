---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179484"
---
# <span data-ttu-id="15639-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="15639-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15639-102">SYNOPSIS</span></span>
<span data-ttu-id="15639-103">Deaktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="15639-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="15639-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15639-104">SYNTAX</span></span>

### <span data-ttu-id="15639-105">Felder</span><span class="sxs-lookup"><span data-stu-id="15639-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15639-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="15639-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15639-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15639-107">DESCRIPTION</span></span>
<span data-ttu-id="15639-108">Das Cmdlet **Disable-AzTrafficManagerEndpoint** deaktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="15639-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="15639-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint** -Objekt mit dem *TrafficManagerEndpoint* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="15639-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="15639-110">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="15639-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="15639-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15639-111">EXAMPLES</span></span>

### <span data-ttu-id="15639-112">Beispiel 1: Deaktivieren eines Endpunkts nach Name</span><span class="sxs-lookup"><span data-stu-id="15639-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="15639-113">Dieser Befehl deaktiviert den externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppen-ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="15639-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="15639-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="15639-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="15639-115">Beispiel 2: Deaktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="15639-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="15639-116">Dieser Befehl ruft den externen Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="15639-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="15639-117">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das Cmdlet **Disable-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="15639-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="15639-118">Dieses Cmdlet deaktiviert diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="15639-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="15639-119">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="15639-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="15639-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="15639-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="15639-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="15639-121">PARAMETERS</span></span>

### <span data-ttu-id="15639-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15639-122">-DefaultProfile</span></span>
<span data-ttu-id="15639-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15639-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15639-124">-Force</span><span class="sxs-lookup"><span data-stu-id="15639-124">-Force</span></span>
<span data-ttu-id="15639-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="15639-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15639-126">-Name</span><span class="sxs-lookup"><span data-stu-id="15639-126">-Name</span></span>
<span data-ttu-id="15639-127">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="15639-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="15639-128">-Profilname</span><span class="sxs-lookup"><span data-stu-id="15639-128">-ProfileName</span></span>
<span data-ttu-id="15639-129">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="15639-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="15639-130">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15639-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="15639-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15639-131">-ResourceGroupName</span></span>
<span data-ttu-id="15639-132">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="15639-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="15639-133">Dieses Cmdlet deaktiviert einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="15639-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="15639-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="15639-135">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="15639-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="15639-136">Verwenden Sie das Get-AzTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15639-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="15639-137">-Typ</span><span class="sxs-lookup"><span data-stu-id="15639-137">-Type</span></span>
<span data-ttu-id="15639-138">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="15639-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="15639-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="15639-139">Valid values are:</span></span> 

- <span data-ttu-id="15639-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="15639-140">AzureEndpoints</span></span>
- <span data-ttu-id="15639-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="15639-141">ExternalEndpoints</span></span>
- <span data-ttu-id="15639-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="15639-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="15639-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15639-143">-Confirm</span></span>
<span data-ttu-id="15639-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15639-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15639-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15639-145">-WhatIf</span></span>
<span data-ttu-id="15639-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15639-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15639-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15639-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15639-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15639-148">CommonParameters</span></span>
<span data-ttu-id="15639-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15639-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15639-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15639-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15639-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15639-151">INPUTS</span></span>

### <span data-ttu-id="15639-152">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="15639-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15639-153">OUTPUTS</span></span>

### <span data-ttu-id="15639-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15639-154">System.Boolean</span></span>

## <span data-ttu-id="15639-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="15639-155">NOTES</span></span>

## <span data-ttu-id="15639-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15639-156">RELATED LINKS</span></span>

[<span data-ttu-id="15639-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15639-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15639-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15639-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="15639-160">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15639-161">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15639-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="15639-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15639-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15639-163">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15639-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: e14f74af1c8e50ddc5bc3281fca71b1e2d740e3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918016"
---
# <span data-ttu-id="7223c-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7223c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7223c-102">SYNOPSIS</span></span>
<span data-ttu-id="7223c-103">Deaktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="7223c-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="7223c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7223c-104">SYNTAX</span></span>

### <span data-ttu-id="7223c-105">Felder</span><span class="sxs-lookup"><span data-stu-id="7223c-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7223c-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="7223c-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7223c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7223c-107">DESCRIPTION</span></span>
<span data-ttu-id="7223c-108">Das **Cmdlet Disable-AzTrafficManagerEndpoint** deaktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="7223c-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="7223c-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint-Objekt** mit dem *Parameter TrafficManagerEndpoint* übergeben.</span><span class="sxs-lookup"><span data-stu-id="7223c-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="7223c-110">Alternativ können Sie den Endpunktnamen und -typ mithilfe der Parameter *Name* und *Typ* zusammen mit den Parametern *ProfileName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="7223c-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7223c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7223c-111">EXAMPLES</span></span>

### <span data-ttu-id="7223c-112">Beispiel 1: Deaktivieren eines Endpunkts nach Name</span><span class="sxs-lookup"><span data-stu-id="7223c-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="7223c-113">Mit diesem Befehl wird der externe Endpunkt contoso im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7223c-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="7223c-114">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="7223c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7223c-115">Beispiel 2: Deaktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7223c-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="7223c-116">Dieser Befehl ruft den externen Endpunkt namens Contoso aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="7223c-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7223c-117">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das **Cmdlet Disable-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="7223c-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7223c-118">Dieses Cmdlet deaktiviert diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7223c-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="7223c-119">Der Befehl gibt den Parameter *"Erzwingen"* an.</span><span class="sxs-lookup"><span data-stu-id="7223c-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7223c-120">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7223c-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7223c-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7223c-121">PARAMETERS</span></span>

### <span data-ttu-id="7223c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7223c-122">-DefaultProfile</span></span>
<span data-ttu-id="7223c-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7223c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7223c-124">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7223c-124">-Force</span></span>
<span data-ttu-id="7223c-125">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="7223c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7223c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7223c-126">-Name</span></span>
<span data-ttu-id="7223c-127">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7223c-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7223c-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7223c-128">-ProfileName</span></span>
<span data-ttu-id="7223c-129">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7223c-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="7223c-130">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7223c-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7223c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7223c-131">-ResourceGroupName</span></span>
<span data-ttu-id="7223c-132">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7223c-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7223c-133">Dieses Cmdlet deaktiviert einen Traffic Manager-Endpunkt in der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7223c-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7223c-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7223c-135">Gibt den Traffic Manager-Endpunkt an, den dieses Cmdlet deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7223c-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="7223c-136">Zum Abrufen eines **TrafficManagerEndpoint-Objekts** verwenden Sie das Get-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7223c-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7223c-137">-Type</span><span class="sxs-lookup"><span data-stu-id="7223c-137">-Type</span></span>
<span data-ttu-id="7223c-138">Gibt den Endpunkttyp an, den dieses Cmdlet dem Traffic Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7223c-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="7223c-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7223c-139">Valid values are:</span></span> 

- <span data-ttu-id="7223c-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="7223c-140">AzureEndpoints</span></span>
- <span data-ttu-id="7223c-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="7223c-141">ExternalEndpoints</span></span>
- <span data-ttu-id="7223c-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="7223c-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="7223c-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7223c-143">-Confirm</span></span>
<span data-ttu-id="7223c-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7223c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7223c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7223c-145">-WhatIf</span></span>
<span data-ttu-id="7223c-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7223c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7223c-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7223c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7223c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7223c-148">CommonParameters</span></span>
<span data-ttu-id="7223c-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7223c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7223c-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7223c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7223c-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7223c-151">INPUTS</span></span>

### <span data-ttu-id="7223c-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7223c-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7223c-153">OUTPUTS</span></span>

### <span data-ttu-id="7223c-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7223c-154">System.Boolean</span></span>

## <span data-ttu-id="7223c-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7223c-155">NOTES</span></span>

## <span data-ttu-id="7223c-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7223c-156">RELATED LINKS</span></span>

[<span data-ttu-id="7223c-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7223c-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7223c-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7223c-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7223c-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7223c-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7223c-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7223c-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7223c-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7223c-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7223c-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



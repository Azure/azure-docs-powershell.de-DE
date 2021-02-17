---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149812"
---
# <span data-ttu-id="4b268-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b268-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b268-102">SYNOPSIS</span></span>
<span data-ttu-id="4b268-103">Entfernt einen Endpunkt aus dem Verkehrs-Manager.</span><span class="sxs-lookup"><span data-stu-id="4b268-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="4b268-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b268-104">SYNTAX</span></span>

### <span data-ttu-id="4b268-105">Felder</span><span class="sxs-lookup"><span data-stu-id="4b268-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b268-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="4b268-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b268-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b268-107">DESCRIPTION</span></span>
<span data-ttu-id="4b268-108">Das **Cmdlet "Remove-AzTrafficManagerEndpoint"** entfernt einen Endpunkt aus Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="4b268-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="4b268-109">Dieses Cmdlet über committ jede Änderung am Datenverkehrs-Manager-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4b268-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="4b268-110">Verwenden Sie das cmdlet "Remove-AzTrafficManagerEndpointConfig", um mehrere Endpunkte aus einem lokalen Traffic Manager-Profilobjekt zu entfernen und Änderungen in einem einzigen Vorgang zu commiten.</span><span class="sxs-lookup"><span data-stu-id="4b268-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="4b268-111">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint-Objekt** mit dem Parameter *"TrafficManagerEndpoint" angeben.*</span><span class="sxs-lookup"><span data-stu-id="4b268-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="4b268-112">Alternativ können Sie den Namen und Typ des Endpunkts mithilfe der *Parameter "Name"* und *"Type"* zusammen mit den Parametern *"ProfileName"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="4b268-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="4b268-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b268-113">EXAMPLES</span></span>

### <span data-ttu-id="4b268-114">Beispiel 1: Entfernen eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="4b268-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="4b268-115">Mit diesem Befehl wird der Azure-Endpunkt "contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b268-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4b268-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b268-116">PARAMETERS</span></span>

### <span data-ttu-id="4b268-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b268-117">-DefaultProfile</span></span>
<span data-ttu-id="4b268-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b268-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b268-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4b268-119">-Force</span></span>
<span data-ttu-id="4b268-120">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4b268-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b268-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4b268-121">-Name</span></span>
<span data-ttu-id="4b268-122">Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b268-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b268-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4b268-123">-ProfileName</span></span>
<span data-ttu-id="4b268-124">Gibt den Namen eines Datenverkehrs-Manager-Profils an, aus dem dieses Cmdlet einen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b268-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="4b268-125">Verwenden Sie zum Abrufen eines Profils das Get-AzTrafficManagerProfile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b268-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4b268-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b268-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b268-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4b268-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4b268-128">Dieses Cmdlet entfernt einen Datenverkehrs-Manager-Endpunkt aus einem Traffic -Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b268-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b268-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b268-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="4b268-130">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b268-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="4b268-131">Verwenden Sie zum **Abrufen eines TrafficManagerEndpoint-Objekts** das Get-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b268-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="4b268-132">-Type</span><span class="sxs-lookup"><span data-stu-id="4b268-132">-Type</span></span>
<span data-ttu-id="4b268-133">Gibt den Endpunkttyp an, den dieses Cmdlet dem Datenverkehrs-Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4b268-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="4b268-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4b268-134">Valid values are:</span></span> 

- <span data-ttu-id="4b268-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="4b268-135">AzureEndpoints</span></span>
- <span data-ttu-id="4b268-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="4b268-136">ExternalEndpoints</span></span>
- <span data-ttu-id="4b268-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="4b268-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="4b268-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b268-138">-Confirm</span></span>
<span data-ttu-id="4b268-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b268-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b268-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4b268-140">-WhatIf</span></span>
<span data-ttu-id="4b268-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b268-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b268-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b268-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b268-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b268-143">CommonParameters</span></span>
<span data-ttu-id="4b268-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b268-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b268-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b268-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b268-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b268-146">INPUTS</span></span>

### <span data-ttu-id="4b268-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b268-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b268-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b268-148">OUTPUTS</span></span>

### <span data-ttu-id="4b268-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b268-149">System.Boolean</span></span>

## <span data-ttu-id="4b268-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b268-150">NOTES</span></span>

## <span data-ttu-id="4b268-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b268-151">RELATED LINKS</span></span>

[<span data-ttu-id="4b268-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b268-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="4b268-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b268-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4b268-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b268-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="4b268-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4b268-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="4b268-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b268-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



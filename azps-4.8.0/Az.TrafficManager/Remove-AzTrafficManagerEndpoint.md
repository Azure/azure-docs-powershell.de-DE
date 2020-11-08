---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167171"
---
# <span data-ttu-id="bf876-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf876-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="bf876-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf876-102">SYNOPSIS</span></span>
<span data-ttu-id="bf876-103">Entfernt einen Endpunkt aus Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bf876-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="bf876-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf876-104">SYNTAX</span></span>

### <span data-ttu-id="bf876-105">Felder</span><span class="sxs-lookup"><span data-stu-id="bf876-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf876-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="bf876-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf876-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf876-107">DESCRIPTION</span></span>
<span data-ttu-id="bf876-108">Mit dem Cmdlet **Remove-AzTrafficManagerEndpoint** wird ein Endpunkt aus Azure Traffic Manager entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf876-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="bf876-109">Dieses Cmdlet übergibt jede Änderung an den Traffic Manager-Dienst.</span><span class="sxs-lookup"><span data-stu-id="bf876-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="bf876-110">Verwenden Sie das Remove-AzTrafficManagerEndpointConfig-Cmdlet, um mehrere Endpunkte aus einem lokalen Traffic Manager-Profilobjekt zu entfernen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="bf876-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="bf876-111">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können mithilfe des *TrafficManagerEndpoint* -Parameters ein **TrafficManagerEndpoint** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="bf876-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="bf876-112">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf876-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bf876-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf876-113">EXAMPLES</span></span>

### <span data-ttu-id="bf876-114">Beispiel 1: Entfernen eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="bf876-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="bf876-115">Mit diesem Befehl wird der Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf876-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="bf876-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf876-116">PARAMETERS</span></span>

### <span data-ttu-id="bf876-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf876-117">-DefaultProfile</span></span>
<span data-ttu-id="bf876-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf876-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf876-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bf876-119">-Force</span></span>
<span data-ttu-id="bf876-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bf876-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf876-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bf876-121">-Name</span></span>
<span data-ttu-id="bf876-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf876-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf876-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="bf876-123">-ProfileName</span></span>
<span data-ttu-id="bf876-124">Gibt den Namen eines Traffic Manager-Profils an, aus dem dieses Cmdlet einen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf876-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="bf876-125">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf876-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bf876-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf876-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf876-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bf876-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bf876-128">Dieses Cmdlet entfernt einen Datenverkehrs-Manager-Endpunkt aus einem Datenverkehrs-Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf876-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf876-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf876-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="bf876-130">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf876-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="bf876-131">Verwenden Sie das Get-AzTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bf876-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="bf876-132">-Typ</span><span class="sxs-lookup"><span data-stu-id="bf876-132">-Type</span></span>
<span data-ttu-id="bf876-133">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="bf876-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="bf876-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bf876-134">Valid values are:</span></span> 

- <span data-ttu-id="bf876-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf876-135">AzureEndpoints</span></span>
- <span data-ttu-id="bf876-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf876-136">ExternalEndpoints</span></span>
- <span data-ttu-id="bf876-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf876-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="bf876-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf876-138">-Confirm</span></span>
<span data-ttu-id="bf876-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf876-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf876-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf876-140">-WhatIf</span></span>
<span data-ttu-id="bf876-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf876-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf876-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf876-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf876-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf876-143">CommonParameters</span></span>
<span data-ttu-id="bf876-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf876-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf876-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf876-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf876-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf876-146">INPUTS</span></span>

### <span data-ttu-id="bf876-147">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf876-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="bf876-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf876-148">OUTPUTS</span></span>

### <span data-ttu-id="bf876-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf876-149">System.Boolean</span></span>

## <span data-ttu-id="bf876-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf876-150">NOTES</span></span>

## <span data-ttu-id="bf876-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf876-151">RELATED LINKS</span></span>

[<span data-ttu-id="bf876-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf876-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf876-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf876-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf876-154">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf876-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf876-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bf876-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="bf876-156">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf876-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



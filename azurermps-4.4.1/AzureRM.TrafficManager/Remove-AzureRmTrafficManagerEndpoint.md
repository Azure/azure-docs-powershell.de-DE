---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 04053050720f2639eeeb698dcfbffb3e156fe2c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483226"
---
# <span data-ttu-id="d8f12-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8f12-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d8f12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8f12-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f12-103">Entfernt einen Endpunkt aus Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d8f12-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8f12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8f12-104">SYNTAX</span></span>

### <span data-ttu-id="d8f12-105">Felder</span><span class="sxs-lookup"><span data-stu-id="d8f12-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8f12-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="d8f12-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f12-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8f12-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f12-108">Mit dem Cmdlet **Remove-AzureRmTrafficManagerEndpoint** wird ein Endpunkt aus Azure Traffic Manager entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="d8f12-109">Dieses Cmdlet übergibt jede Änderung an den Traffic Manager-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d8f12-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="d8f12-110">Verwenden Sie das Remove-AzureRmTrafficManagerEndpointConfig-Cmdlet, um mehrere Endpunkte aus einem lokalen Traffic Manager-Profilobjekt zu entfernen und Änderungen in einem einzelnen Vorgang zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d8f12-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="d8f12-111">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können mithilfe des *TrafficManagerEndpoint* -Parameters ein **TrafficManagerEndpoint** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="d8f12-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="d8f12-112">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8f12-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d8f12-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8f12-113">EXAMPLES</span></span>

### <span data-ttu-id="d8f12-114">Beispiel 1: Entfernen eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="d8f12-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d8f12-115">Mit diesem Befehl wird der Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d8f12-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8f12-116">PARAMETERS</span></span>

### <span data-ttu-id="d8f12-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8f12-117">-Force</span></span>
<span data-ttu-id="d8f12-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d8f12-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8f12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d8f12-119">-Name</span></span>
<span data-ttu-id="d8f12-120">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8f12-121">-Profilname</span><span class="sxs-lookup"><span data-stu-id="d8f12-121">-ProfileName</span></span>
<span data-ttu-id="d8f12-122">Gibt den Namen eines Traffic Manager-Profils an, aus dem dieses Cmdlet einen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-122">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="d8f12-123">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8f12-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d8f12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f12-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8f12-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d8f12-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8f12-126">Dieses Cmdlet entfernt einen Datenverkehrs-Manager-Endpunkt aus einem Datenverkehrs-Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-126">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8f12-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8f12-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d8f12-128">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-128">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="d8f12-129">Verwenden Sie das Get-AzureRmTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8f12-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d8f12-130">-Typ</span><span class="sxs-lookup"><span data-stu-id="d8f12-130">-Type</span></span>
<span data-ttu-id="d8f12-131">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d8f12-131">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d8f12-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d8f12-132">Valid values are:</span></span> 

- <span data-ttu-id="d8f12-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8f12-133">AzureEndpoints</span></span>
- <span data-ttu-id="d8f12-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8f12-134">ExternalEndpoints</span></span>
- <span data-ttu-id="d8f12-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8f12-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="d8f12-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8f12-136">-Confirm</span></span>
<span data-ttu-id="d8f12-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8f12-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f12-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f12-138">-WhatIf</span></span>
<span data-ttu-id="d8f12-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8f12-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f12-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8f12-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f12-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f12-141">-DefaultProfile</span></span>
<span data-ttu-id="d8f12-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8f12-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8f12-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f12-143">CommonParameters</span></span>
<span data-ttu-id="d8f12-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f12-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f12-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f12-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f12-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8f12-146">INPUTS</span></span>

### <span data-ttu-id="d8f12-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8f12-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="d8f12-148">Der Parameter "TrafficManagerEndpoint" akzeptiert den Wert vom Typ "TrafficManagerEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8f12-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d8f12-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8f12-149">OUTPUTS</span></span>

### <span data-ttu-id="d8f12-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8f12-150">System.Boolean</span></span>

## <span data-ttu-id="d8f12-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8f12-151">NOTES</span></span>

## <span data-ttu-id="d8f12-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8f12-152">RELATED LINKS</span></span>

[<span data-ttu-id="d8f12-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8f12-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d8f12-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8f12-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d8f12-155">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8f12-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d8f12-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d8f12-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d8f12-157">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8f12-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



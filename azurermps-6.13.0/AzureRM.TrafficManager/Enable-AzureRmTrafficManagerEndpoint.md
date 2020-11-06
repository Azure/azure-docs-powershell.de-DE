---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 2556715c321ddcc3f8acbc518ddbe6a3048353af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495577"
---
# <span data-ttu-id="e747a-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e747a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e747a-102">SYNOPSIS</span></span>
<span data-ttu-id="e747a-103">Aktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="e747a-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e747a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e747a-104">SYNTAX</span></span>

### <span data-ttu-id="e747a-105">Felder</span><span class="sxs-lookup"><span data-stu-id="e747a-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e747a-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="e747a-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e747a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e747a-107">DESCRIPTION</span></span>
<span data-ttu-id="e747a-108">Das Cmdlet **enable-AzureRmTrafficManagerEndpoint** aktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="e747a-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="e747a-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können mithilfe des *TrafficManagerEndpoint* -Parameters ein **TrafficManagerEndpoint** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="e747a-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="e747a-110">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="e747a-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="e747a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e747a-111">EXAMPLES</span></span>

### <span data-ttu-id="e747a-112">Beispiel 1: Aktivieren eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="e747a-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="e747a-113">Dieser Befehl aktiviert den externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e747a-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="e747a-114">Beispiel 2: Aktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="e747a-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="e747a-115">Dieser Befehl ruft den externen Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="e747a-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="e747a-116">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das Cmdlet **enable-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="e747a-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e747a-117">Dieses Cmdlet aktiviert diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e747a-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="e747a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e747a-118">PARAMETERS</span></span>

### <span data-ttu-id="e747a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e747a-119">-DefaultProfile</span></span>
<span data-ttu-id="e747a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e747a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e747a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e747a-121">-Name</span></span>
<span data-ttu-id="e747a-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e747a-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="e747a-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="e747a-123">-ProfileName</span></span>
<span data-ttu-id="e747a-124">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e747a-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="e747a-125">Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e747a-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="e747a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e747a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e747a-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e747a-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e747a-128">Dieses Cmdlet aktiviert einen Datenverkehrs-Manager-Endpunkt in der Gruppe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e747a-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e747a-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e747a-130">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e747a-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="e747a-131">Verwenden Sie das Get-AzureRmTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e747a-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e747a-132">-Typ</span><span class="sxs-lookup"><span data-stu-id="e747a-132">-Type</span></span>
<span data-ttu-id="e747a-133">Gibt den Typ des Endpunkts an, den dieses Cmdlet im Traffic Manager-Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e747a-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="e747a-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e747a-134">Valid values are:</span></span> 

- <span data-ttu-id="e747a-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="e747a-135">AzureEndpoints</span></span>
- <span data-ttu-id="e747a-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="e747a-136">ExternalEndpoints</span></span>
- <span data-ttu-id="e747a-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="e747a-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="e747a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e747a-138">CommonParameters</span></span>
<span data-ttu-id="e747a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e747a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e747a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e747a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e747a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e747a-141">INPUTS</span></span>

### <span data-ttu-id="e747a-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="e747a-143">Der Parameter "TrafficManagerEndpoint" akzeptiert den Wert vom Typ "TrafficManagerEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e747a-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e747a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e747a-144">OUTPUTS</span></span>

### <span data-ttu-id="e747a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e747a-145">System.Boolean</span></span>

## <span data-ttu-id="e747a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e747a-146">NOTES</span></span>

## <span data-ttu-id="e747a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e747a-147">RELATED LINKS</span></span>

[<span data-ttu-id="e747a-148">Deaktivieren-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e747a-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e747a-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e747a-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e747a-151">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e747a-152">Neu – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e747a-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e747a-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e747a-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e747a-154">Satz-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e747a-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)



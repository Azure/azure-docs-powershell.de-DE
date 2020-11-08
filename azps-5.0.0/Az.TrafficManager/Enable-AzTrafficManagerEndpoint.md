---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179477"
---
# <span data-ttu-id="a2563-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a2563-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2563-102">SYNOPSIS</span></span>
<span data-ttu-id="a2563-103">Aktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="a2563-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="a2563-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2563-104">SYNTAX</span></span>

### <span data-ttu-id="a2563-105">Felder</span><span class="sxs-lookup"><span data-stu-id="a2563-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2563-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="a2563-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2563-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2563-107">DESCRIPTION</span></span>
<span data-ttu-id="a2563-108">Das Cmdlet **enable-AzTrafficManagerEndpoint** aktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="a2563-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a2563-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können mithilfe des *TrafficManagerEndpoint* -Parameters ein **TrafficManagerEndpoint** -Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="a2563-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="a2563-110">Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2563-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a2563-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2563-111">EXAMPLES</span></span>

### <span data-ttu-id="a2563-112">Beispiel 1: Aktivieren eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="a2563-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="a2563-113">Dieser Befehl aktiviert den externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a2563-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a2563-114">Beispiel 2: Aktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a2563-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="a2563-115">Dieser Befehl ruft den externen Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="a2563-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a2563-116">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das Cmdlet **enable-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="a2563-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a2563-117">Dieses Cmdlet aktiviert diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a2563-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="a2563-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2563-118">PARAMETERS</span></span>

### <span data-ttu-id="a2563-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2563-119">-DefaultProfile</span></span>
<span data-ttu-id="a2563-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2563-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2563-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2563-121">-Name</span></span>
<span data-ttu-id="a2563-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2563-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a2563-123">-Profilname</span><span class="sxs-lookup"><span data-stu-id="a2563-123">-ProfileName</span></span>
<span data-ttu-id="a2563-124">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2563-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="a2563-125">Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2563-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a2563-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2563-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2563-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a2563-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a2563-128">Dieses Cmdlet aktiviert einen Datenverkehrs-Manager-Endpunkt in der Gruppe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a2563-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2563-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a2563-130">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2563-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="a2563-131">Verwenden Sie das Get-AzTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2563-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a2563-132">-Typ</span><span class="sxs-lookup"><span data-stu-id="a2563-132">-Type</span></span>
<span data-ttu-id="a2563-133">Gibt den Typ des Endpunkts an, den dieses Cmdlet im Traffic Manager-Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2563-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="a2563-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a2563-134">Valid values are:</span></span> 

- <span data-ttu-id="a2563-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a2563-135">AzureEndpoints</span></span>
- <span data-ttu-id="a2563-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a2563-136">ExternalEndpoints</span></span>
- <span data-ttu-id="a2563-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a2563-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="a2563-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2563-138">CommonParameters</span></span>
<span data-ttu-id="a2563-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2563-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2563-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2563-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2563-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2563-141">INPUTS</span></span>

### <span data-ttu-id="a2563-142">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a2563-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2563-143">OUTPUTS</span></span>

### <span data-ttu-id="a2563-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2563-144">System.Boolean</span></span>

## <span data-ttu-id="a2563-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2563-145">NOTES</span></span>

## <span data-ttu-id="a2563-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2563-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2563-147">Deaktivieren-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a2563-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a2563-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a2563-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a2563-150">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a2563-151">Neu – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a2563-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a2563-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2563-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a2563-153">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a2563-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



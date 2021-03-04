---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5ab6ba03b9803cc8726eff458776f8ee40d48793
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918011"
---
# <span data-ttu-id="c05f4-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c05f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c05f4-103">Aktiviert einen Endpunkt in einem Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c05f4-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="c05f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c05f4-104">SYNTAX</span></span>

### <span data-ttu-id="c05f4-105">Felder</span><span class="sxs-lookup"><span data-stu-id="c05f4-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c05f4-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="c05f4-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c05f4-107">DESCRIPTION</span></span>
<span data-ttu-id="c05f4-108">Das **Cmdlet Enable-AzTrafficManagerEndpoint** ermöglicht einen Endpunkt in einem Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="c05f4-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c05f4-109">Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint-Objekt** mithilfe des *TrafficManagerEndpoint-Parameters* angeben.</span><span class="sxs-lookup"><span data-stu-id="c05f4-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="c05f4-110">Alternativ können Sie den Endpunktnamen und -typ mithilfe der Parameter *Name* und *Typ* zusammen mit den Parametern *ProfileName* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="c05f4-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c05f4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c05f4-111">EXAMPLES</span></span>

### <span data-ttu-id="c05f4-112">Beispiel 1: Aktivieren eines Endpunkts aus einem Profil</span><span class="sxs-lookup"><span data-stu-id="c05f4-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="c05f4-113">Dieser Befehl aktiviert den externen Endpunkt "contoso" im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c05f4-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="c05f4-114">Beispiel 2: Aktivieren eines Endpunkts mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c05f4-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="c05f4-115">Dieser Befehl ruft den externen Endpunkt namens Contoso aus dem Profil "ContosoProfile" in ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="c05f4-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c05f4-116">Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das **Enable-AzTrafficManagerEndpoint-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="c05f4-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c05f4-117">Dieses Cmdlet ermöglicht diesen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c05f4-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="c05f4-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c05f4-118">PARAMETERS</span></span>

### <span data-ttu-id="c05f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05f4-119">-DefaultProfile</span></span>
<span data-ttu-id="c05f4-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c05f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c05f4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c05f4-121">-Name</span></span>
<span data-ttu-id="c05f4-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c05f4-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="c05f4-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c05f4-123">-ProfileName</span></span>
<span data-ttu-id="c05f4-124">Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c05f4-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="c05f4-125">Verwenden Sie das cmdlet Get-AzTrafficManagerProfile, um ein Profil zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c05f4-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c05f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="c05f4-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c05f4-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c05f4-128">Dieses Cmdlet aktiviert einen Traffic Manager-Endpunkt in der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c05f4-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c05f4-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c05f4-130">Gibt den Traffic Manager-Endpunkt an, den dieses Cmdlet aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c05f4-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="c05f4-131">Zum Abrufen eines **TrafficManagerEndpoint-Objekts** verwenden Sie das Get-AzTrafficManagerEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c05f4-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c05f4-132">-Type</span><span class="sxs-lookup"><span data-stu-id="c05f4-132">-Type</span></span>
<span data-ttu-id="c05f4-133">Gibt den Endpunkttyp an, den dieses Cmdlet im Traffic Manager-Profil deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c05f4-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="c05f4-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c05f4-134">Valid values are:</span></span> 

- <span data-ttu-id="c05f4-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c05f4-135">AzureEndpoints</span></span>
- <span data-ttu-id="c05f4-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c05f4-136">ExternalEndpoints</span></span>
- <span data-ttu-id="c05f4-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c05f4-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="c05f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05f4-138">CommonParameters</span></span>
<span data-ttu-id="c05f4-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05f4-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05f4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05f4-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c05f4-141">INPUTS</span></span>

### <span data-ttu-id="c05f4-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c05f4-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c05f4-143">OUTPUTS</span></span>

### <span data-ttu-id="c05f4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c05f4-144">System.Boolean</span></span>

## <span data-ttu-id="c05f4-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c05f4-145">NOTES</span></span>

## <span data-ttu-id="c05f4-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c05f4-146">RELATED LINKS</span></span>

[<span data-ttu-id="c05f4-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c05f4-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c05f4-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c05f4-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c05f4-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c05f4-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c05f4-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c05f4-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c05f4-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c05f4-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c05f4-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



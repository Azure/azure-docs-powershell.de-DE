---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291083"
---
# <span data-ttu-id="1e855-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1e855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e855-102">SYNOPSIS</span></span>
<span data-ttu-id="1e855-103">Ruft einen Endpunkt für ein Datenverkehrs-Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="1e855-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="1e855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e855-104">SYNTAX</span></span>

### <span data-ttu-id="1e855-105">Felder</span><span class="sxs-lookup"><span data-stu-id="1e855-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e855-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="1e855-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e855-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e855-107">DESCRIPTION</span></span>
<span data-ttu-id="1e855-108">Das **Cmdlet "Get-AzTrafficManagerEndpoint"** ruft einen Endpunkt für ein Azure Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="1e855-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1e855-109">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzTrafficManagerEndpoint anwenden.</span><span class="sxs-lookup"><span data-stu-id="1e855-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="1e855-110">Geben Sie den Endpunkt mithilfe der *Parameter "Name"* und *"Type"* an.</span><span class="sxs-lookup"><span data-stu-id="1e855-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="1e855-111">Sie können das Datenverkehrs-Manager-Profil entweder mithilfe des Parameters *"ProfileName"* und *"ResourceGroupName"* oder durch Angeben eines **"TrafficManagerProfile"-Objekts** angeben.</span><span class="sxs-lookup"><span data-stu-id="1e855-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1e855-112">Alternativ können Sie den Wert mithilfe der Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1e855-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="1e855-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e855-113">EXAMPLES</span></span>

### <span data-ttu-id="1e855-114">Beispiel 1: Erhalten eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="1e855-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="1e855-115">Dieser Befehl ruft den Azure-Endpunkt "contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint Variable.</span><span class="sxs-lookup"><span data-stu-id="1e855-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="1e855-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e855-116">PARAMETERS</span></span>

### <span data-ttu-id="1e855-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e855-117">-DefaultProfile</span></span>
<span data-ttu-id="1e855-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e855-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e855-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1e855-119">-Name</span></span>
<span data-ttu-id="1e855-120">Gibt den Namen des Datenverkehrs-Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1e855-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e855-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1e855-121">-ProfileName</span></span>
<span data-ttu-id="1e855-122">Gibt den Namen des Datenverkehrs-Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1e855-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e855-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e855-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e855-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1e855-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1e855-125">Dieses Cmdlet ruft einen Datenverkehrs-Manager-Endpunkt in der Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1e855-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e855-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1e855-127">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1e855-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e855-128">-Type</span><span class="sxs-lookup"><span data-stu-id="1e855-128">-Type</span></span>
<span data-ttu-id="1e855-129">Gibt den Endpunkttyp an, den dieses Cmdlet dem Datenverkehrs-Manager-Profil hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1e855-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="1e855-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1e855-130">Valid values are:</span></span> 

- <span data-ttu-id="1e855-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1e855-131">AzureEndpoints</span></span>
- <span data-ttu-id="1e855-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1e855-132">ExternalEndpoints</span></span>
- <span data-ttu-id="1e855-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1e855-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="1e855-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e855-134">CommonParameters</span></span>
<span data-ttu-id="1e855-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e855-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e855-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e855-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e855-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e855-137">INPUTS</span></span>

### <span data-ttu-id="1e855-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1e855-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e855-139">OUTPUTS</span></span>

### <span data-ttu-id="1e855-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1e855-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e855-141">NOTES</span></span>

## <span data-ttu-id="1e855-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e855-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e855-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1e855-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1e855-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1e855-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1e855-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e855-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996341"
---
# <span data-ttu-id="b0343-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b0343-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0343-102">SYNOPSIS</span></span>
<span data-ttu-id="b0343-103">Ruft einen Endpunkt für ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="b0343-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="b0343-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0343-104">SYNTAX</span></span>

### <span data-ttu-id="b0343-105">Felder</span><span class="sxs-lookup"><span data-stu-id="b0343-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0343-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="b0343-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0343-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0343-107">DESCRIPTION</span></span>
<span data-ttu-id="b0343-108">Das Cmdlet " **Get-AzTrafficManagerEndpoint** " Ruft einen Endpunkt für ein Azure Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="b0343-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b0343-109">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b0343-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b0343-110">Geben Sie den Endpunkt mithilfe der Parameter *Name* und *Type* an.</span><span class="sxs-lookup"><span data-stu-id="b0343-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="b0343-111">Sie können das Traffic Manager-Profil entweder mit dem Parameter ProfileName und *ResourceGroupName* oder durch Angeben eines **TrafficManagerProfile** *-Objekts* angeben.</span><span class="sxs-lookup"><span data-stu-id="b0343-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b0343-112">Sie können diesen Wert auch über die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="b0343-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="b0343-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0343-113">EXAMPLES</span></span>

### <span data-ttu-id="b0343-114">Beispiel 1: Abrufen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="b0343-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="b0343-115">Dieser Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b0343-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="b0343-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0343-116">PARAMETERS</span></span>

### <span data-ttu-id="b0343-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0343-117">-DefaultProfile</span></span>
<span data-ttu-id="b0343-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0343-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0343-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b0343-119">-Name</span></span>
<span data-ttu-id="b0343-120">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b0343-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0343-121">-Profilname</span><span class="sxs-lookup"><span data-stu-id="b0343-121">-ProfileName</span></span>
<span data-ttu-id="b0343-122">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b0343-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0343-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0343-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0343-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b0343-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b0343-125">Dieses Cmdlet ruft einen Datenverkehrs-Manager-Endpunkt in der Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b0343-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0343-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b0343-127">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b0343-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0343-128">-Typ</span><span class="sxs-lookup"><span data-stu-id="b0343-128">-Type</span></span>
<span data-ttu-id="b0343-129">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b0343-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b0343-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b0343-130">Valid values are:</span></span> 

- <span data-ttu-id="b0343-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="b0343-131">AzureEndpoints</span></span>
- <span data-ttu-id="b0343-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="b0343-132">ExternalEndpoints</span></span>
- <span data-ttu-id="b0343-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="b0343-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="b0343-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0343-134">CommonParameters</span></span>
<span data-ttu-id="b0343-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0343-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0343-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0343-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0343-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0343-137">INPUTS</span></span>

### <span data-ttu-id="b0343-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b0343-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0343-139">OUTPUTS</span></span>

### <span data-ttu-id="b0343-140">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b0343-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0343-141">NOTES</span></span>

## <span data-ttu-id="b0343-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0343-142">RELATED LINKS</span></span>

[<span data-ttu-id="b0343-143">Deaktivieren-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b0343-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b0343-145">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b0343-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b0343-147">Satz-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0343-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)



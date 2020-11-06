---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 50ad29e9c28b42b1459d66358b8c6c37e2e0f4ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499105"
---
# <span data-ttu-id="2da24-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2da24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2da24-102">SYNOPSIS</span></span>
<span data-ttu-id="2da24-103">Ruft einen Endpunkt für ein Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="2da24-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2da24-104">SYNTAX</span></span>

### <span data-ttu-id="2da24-105">Felder</span><span class="sxs-lookup"><span data-stu-id="2da24-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da24-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="2da24-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da24-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2da24-107">DESCRIPTION</span></span>
<span data-ttu-id="2da24-108">Das Cmdlet " **Get-AzureRmTrafficManagerEndpoint** " Ruft einen Endpunkt für ein Azure Traffic Manager-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="2da24-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="2da24-109">Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets vornehmen.</span><span class="sxs-lookup"><span data-stu-id="2da24-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="2da24-110">Geben Sie den Endpunkt mithilfe der Parameter *Name* und *Type* an.</span><span class="sxs-lookup"><span data-stu-id="2da24-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="2da24-111">Sie können das Traffic Manager-Profil entweder mit dem Parameter ProfileName und *ResourceGroupName* oder durch Angeben eines **TrafficManagerProfile** *-Objekts* angeben.</span><span class="sxs-lookup"><span data-stu-id="2da24-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2da24-112">Sie können diesen Wert auch über die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="2da24-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="2da24-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2da24-113">EXAMPLES</span></span>

### <span data-ttu-id="2da24-114">Beispiel 1: Abrufen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="2da24-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="2da24-115">Dieser Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2da24-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="2da24-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2da24-116">PARAMETERS</span></span>

### <span data-ttu-id="2da24-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2da24-117">-Name</span></span>
<span data-ttu-id="2da24-118">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2da24-118">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2da24-119">-Profilname</span><span class="sxs-lookup"><span data-stu-id="2da24-119">-ProfileName</span></span>
<span data-ttu-id="2da24-120">Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2da24-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2da24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da24-121">-ResourceGroupName</span></span>
<span data-ttu-id="2da24-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2da24-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2da24-123">Dieses Cmdlet ruft einen Datenverkehrs-Manager-Endpunkt in der Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2da24-123">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2da24-124">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-124">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2da24-125">Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2da24-125">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2da24-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="2da24-126">-Type</span></span>
<span data-ttu-id="2da24-127">Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2da24-127">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="2da24-128">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2da24-128">Valid values are:</span></span> 

- <span data-ttu-id="2da24-129">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2da24-129">AzureEndpoints</span></span>
- <span data-ttu-id="2da24-130">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2da24-130">ExternalEndpoints</span></span>
- <span data-ttu-id="2da24-131">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2da24-131">NestedEndpoints</span></span>

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

### <span data-ttu-id="2da24-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da24-132">-DefaultProfile</span></span>
<span data-ttu-id="2da24-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2da24-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da24-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da24-134">CommonParameters</span></span>
<span data-ttu-id="2da24-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da24-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da24-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da24-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da24-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2da24-137">INPUTS</span></span>

### <span data-ttu-id="2da24-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="2da24-139">Der Parameter "TrafficManagerEndpoint" akzeptiert den Wert vom Typ "TrafficManagerEndpoint" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2da24-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="2da24-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2da24-140">OUTPUTS</span></span>

### <span data-ttu-id="2da24-141">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2da24-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2da24-142">NOTES</span></span>

## <span data-ttu-id="2da24-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2da24-143">RELATED LINKS</span></span>

[<span data-ttu-id="2da24-144">Deaktivieren-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2da24-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2da24-146">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2da24-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2da24-148">Satz-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2da24-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)



---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477393"
---
# <span data-ttu-id="54363-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="54363-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="54363-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54363-102">SYNOPSIS</span></span>
<span data-ttu-id="54363-103">Aktualisiert die Bereitstellungeines API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="54363-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54363-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54363-104">SYNTAX</span></span>

### <span data-ttu-id="54363-105">Spezifischer API-Verwaltungsdienst (Standard)</span><span class="sxs-lookup"><span data-stu-id="54363-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54363-106">Update von PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="54363-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54363-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54363-107">DESCRIPTION</span></span>
<span data-ttu-id="54363-108">Das Cmdlet **Update-AzureRmApiManagementDeployment** aktualisiert aktuelle Bereitstellungen eines API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="54363-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="54363-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54363-109">EXAMPLES</span></span>

### <span data-ttu-id="54363-110">Beispiel 1: Aktualisieren einer Bereitstellung einer ApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="54363-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="54363-111">Mit diesem Befehl wird die Bereitstellung einer API-Verwaltungsinstanz auf einen drei-Komponenten-Kapazitäts Standard aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="54363-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="54363-112">Beispiel 2: Abrufen einer ApiManagement-Instanz und erneutes skalieren</span><span class="sxs-lookup"><span data-stu-id="54363-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="54363-113">In diesem Beispiel wird eine API-Verwaltungsinstanz abgerufen, auf fünf Premium-Einheiten skaliert und dann dem Premium-Bereich weitere drei Einheiten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="54363-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="54363-114">Beispiel 3: Update Bereitstellung (externe VNET)</span><span class="sxs-lookup"><span data-stu-id="54363-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="54363-115">Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem externen *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="54363-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="54363-116">Beispiel 4: Update Bereitstellung (interne VNET)</span><span class="sxs-lookup"><span data-stu-id="54363-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="54363-117">Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem internen *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="54363-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="54363-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="54363-118">PARAMETERS</span></span>

### <span data-ttu-id="54363-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="54363-119">-AdditionalRegions</span></span>
<span data-ttu-id="54363-120">Gibt zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="54363-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="54363-121">-ApiManagement</span></span>
<span data-ttu-id="54363-122">Gibt die **PsApiManagement** -Instanz an, von der die Bereitstellungskonfiguration abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="54363-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="54363-123">Verwenden Sie diesen Parameter, wenn die Instanz bereits alle erforderlichen Änderungen aufweist.</span><span class="sxs-lookup"><span data-stu-id="54363-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-124">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="54363-124">-Capacity</span></span>
<span data-ttu-id="54363-125">Gibt die SKU-Kapazität des Master Azure API Management Deployment-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="54363-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="54363-126">-Location</span></span>
<span data-ttu-id="54363-127">Gibt den Speicherort des Bereitstellungsbereichs der Master-API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="54363-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="54363-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54363-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54363-129">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="54363-129">North Central US</span></span>
- <span data-ttu-id="54363-130">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="54363-130">South Central US</span></span>
- <span data-ttu-id="54363-131">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="54363-131">Central US</span></span>
- <span data-ttu-id="54363-132">West Europa</span><span class="sxs-lookup"><span data-stu-id="54363-132">West Europe</span></span>
- <span data-ttu-id="54363-133">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="54363-133">North Europe</span></span>
- <span data-ttu-id="54363-134">West-US</span><span class="sxs-lookup"><span data-stu-id="54363-134">West US</span></span>
- <span data-ttu-id="54363-135">East US</span><span class="sxs-lookup"><span data-stu-id="54363-135">East US</span></span>
- <span data-ttu-id="54363-136">East US 2</span><span class="sxs-lookup"><span data-stu-id="54363-136">East US 2</span></span>
- <span data-ttu-id="54363-137">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="54363-137">Japan East</span></span>
- <span data-ttu-id="54363-138">Japan West</span><span class="sxs-lookup"><span data-stu-id="54363-138">Japan West</span></span>
- <span data-ttu-id="54363-139">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="54363-139">Brazil South</span></span>
- <span data-ttu-id="54363-140">Südostasien</span><span class="sxs-lookup"><span data-stu-id="54363-140">Southeast Asia</span></span>
- <span data-ttu-id="54363-141">Ostasien</span><span class="sxs-lookup"><span data-stu-id="54363-141">East Asia</span></span>
- <span data-ttu-id="54363-142">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="54363-142">Australia East</span></span>
- <span data-ttu-id="54363-143">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="54363-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-144">-Name</span><span class="sxs-lookup"><span data-stu-id="54363-144">-Name</span></span>
<span data-ttu-id="54363-145">Gibt den Namen der API-Verwaltung an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="54363-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54363-146">-PassThru</span></span>
<span data-ttu-id="54363-147">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="54363-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54363-148">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="54363-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54363-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54363-149">-ResourceGroupName</span></span>
<span data-ttu-id="54363-150">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="54363-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="54363-151">-Sku</span></span>
<span data-ttu-id="54363-152">Gibt die Ebene des Bereitstellungsbereichs der Master Azure API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="54363-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="54363-153">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54363-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54363-154">Entwickler</span><span class="sxs-lookup"><span data-stu-id="54363-154">Developer</span></span>
- <span data-ttu-id="54363-155">Standard</span><span class="sxs-lookup"><span data-stu-id="54363-155">Standard</span></span>
- <span data-ttu-id="54363-156">Premium</span><span class="sxs-lookup"><span data-stu-id="54363-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="54363-157">-VirtualNetwork</span></span>
<span data-ttu-id="54363-158">Gibt die Konfiguration des virtuellen Netzwerks des Master Azure API-Verwaltungs Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="54363-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="54363-159">-VpnType</span></span>
<span data-ttu-id="54363-160">Gibt den virtuellen Netzwerktyp der API-Verwaltungs Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="54363-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="54363-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="54363-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54363-162">Keine.</span><span class="sxs-lookup"><span data-stu-id="54363-162">None.</span></span>
<span data-ttu-id="54363-163">Die Bereitstellung der API-Verwaltung gehört nicht zu einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="54363-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="54363-164">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="54363-164">This is the default value.</span></span> 
- <span data-ttu-id="54363-165">Externen.</span><span class="sxs-lookup"><span data-stu-id="54363-165">External.</span></span>
<span data-ttu-id="54363-166">Die API-Verwaltungs Bereitstellung hat eine virtuelle Adresse mit externer Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="54363-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="54363-167">Internen.</span><span class="sxs-lookup"><span data-stu-id="54363-167">Internal.</span></span>
<span data-ttu-id="54363-168">Die API-Verwaltungs Bereitstellung hat eine virtuelle Adresse im Intranet.</span><span class="sxs-lookup"><span data-stu-id="54363-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54363-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54363-169">-DefaultProfile</span></span>
<span data-ttu-id="54363-170">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54363-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54363-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54363-171">CommonParameters</span></span>
<span data-ttu-id="54363-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54363-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54363-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54363-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54363-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54363-174">INPUTS</span></span>

### <span data-ttu-id="54363-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="54363-175">PsApiManagement</span></span>
<span data-ttu-id="54363-176">Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="54363-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="54363-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54363-177">OUTPUTS</span></span>

### <span data-ttu-id="54363-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="54363-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="54363-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="54363-179">NOTES</span></span>

## <span data-ttu-id="54363-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54363-180">RELATED LINKS</span></span>

[<span data-ttu-id="54363-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="54363-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)



---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478013"
---
# <span data-ttu-id="e3c9c-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e3c9c-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="e3c9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c9c-103">Aktualisiert die Bereitstellungeines API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3c9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c9c-104">SYNTAX</span></span>

### <span data-ttu-id="e3c9c-105">UpdateSpecificService (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3c9c-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="e3c9c-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3c9c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3c9c-107">DESCRIPTION</span></span>
<span data-ttu-id="e3c9c-108">Das Cmdlet **Update-AzureRmApiManagementDeployment** aktualisiert aktuelle Bereitstellungen eines API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="e3c9c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3c9c-109">EXAMPLES</span></span>

### <span data-ttu-id="e3c9c-110">Beispiel 1: Aktualisieren einer Bereitstellung einer ApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="e3c9c-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="e3c9c-111">Mit diesem Befehl wird die Bereitstellung einer API-Verwaltungsinstanz auf einen drei-Komponenten-Kapazitäts Standard aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="e3c9c-112">Beispiel 2: Abrufen einer ApiManagement-Instanz und erneutes skalieren</span><span class="sxs-lookup"><span data-stu-id="e3c9c-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="e3c9c-113">In diesem Beispiel wird eine API-Verwaltungsinstanz abgerufen, auf fünf Premium-Einheiten skaliert und dann dem Premium-Bereich weitere drei Einheiten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="e3c9c-114">Beispiel 3: Update Bereitstellung (externe VNET)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="e3c9c-115">Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem externen *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="e3c9c-116">Beispiel 4: Update Bereitstellung (interne VNET)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="e3c9c-117">Mit diesem Befehl wird eine vorhandene API-Verwaltungs Bereitstellung aktualisiert und eine Verknüpfung zu einem internen *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="e3c9c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3c9c-118">PARAMETERS</span></span>

### <span data-ttu-id="e3c9c-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="e3c9c-119">-AdditionalRegions</span></span>
<span data-ttu-id="e3c9c-120">Gibt zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3c9c-121">-ApiManagement</span></span>
<span data-ttu-id="e3c9c-122">Gibt die **PsApiManagement** -Instanz an, von der die Bereitstellungskonfiguration abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="e3c9c-123">Verwenden Sie diesen Parameter, wenn die Instanz bereits alle erforderlichen Änderungen aufweist.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-124">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e3c9c-124">-Capacity</span></span>
<span data-ttu-id="e3c9c-125">Gibt die SKU-Kapazität des Master Azure API Management Deployment-Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c9c-126">-DefaultProfile</span></span>
<span data-ttu-id="e3c9c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c9c-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="e3c9c-128">-Location</span></span>
<span data-ttu-id="e3c9c-129">Gibt den Speicherort des Bereitstellungsbereichs der Master-API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="e3c9c-130">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="e3c9c-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e3c9c-131">-Name</span></span>
<span data-ttu-id="e3c9c-132">Gibt den Namen der API-Verwaltung an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3c9c-133">-PassThru</span></span>
<span data-ttu-id="e3c9c-134">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3c9c-135">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3c9c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c9c-136">-ResourceGroupName</span></span>
<span data-ttu-id="e3c9c-137">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="e3c9c-138">-Sku</span></span>
<span data-ttu-id="e3c9c-139">Gibt die Ebene des Bereitstellungsbereichs der Master Azure API-Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="e3c9c-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3c9c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3c9c-141">Entwickler</span><span class="sxs-lookup"><span data-stu-id="e3c9c-141">Developer</span></span>
- <span data-ttu-id="e3c9c-142">Standard</span><span class="sxs-lookup"><span data-stu-id="e3c9c-142">Standard</span></span>
- <span data-ttu-id="e3c9c-143">Premium</span><span class="sxs-lookup"><span data-stu-id="e3c9c-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3c9c-144">-VirtualNetwork</span></span>
<span data-ttu-id="e3c9c-145">Gibt die Konfiguration des virtuellen Netzwerks des Master Azure API-Verwaltungs Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="e3c9c-146">-VpnType</span></span>
<span data-ttu-id="e3c9c-147">Gibt den virtuellen Netzwerktyp der API-Verwaltungs Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="e3c9c-148">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3c9c-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3c9c-149">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-149">None.</span></span>
<span data-ttu-id="e3c9c-150">Die Bereitstellung der API-Verwaltung gehört nicht zu einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="e3c9c-151">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-151">This is the default value.</span></span> 
- <span data-ttu-id="e3c9c-152">Externen.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-152">External.</span></span>
<span data-ttu-id="e3c9c-153">Die API-Verwaltungs Bereitstellung hat eine virtuelle Adresse mit externer Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="e3c9c-154">Internen.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-154">Internal.</span></span>
<span data-ttu-id="e3c9c-155">Die API-Verwaltungs Bereitstellung hat eine virtuelle Adresse im Intranet.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c9c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c9c-156">CommonParameters</span></span>
<span data-ttu-id="e3c9c-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c9c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c9c-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c9c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c9c-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3c9c-159">INPUTS</span></span>

### <span data-ttu-id="e3c9c-160">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3c9c-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="e3c9c-161">Parameter: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3c9c-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="e3c9c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e3c9c-162">System.String</span></span>

### <span data-ttu-id="e3c9c-163">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="e3c9c-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="e3c9c-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e3c9c-164">System.Int32</span></span>

### <span data-ttu-id="e3c9c-165">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3c9c-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="e3c9c-166">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVpnType</span><span class="sxs-lookup"><span data-stu-id="e3c9c-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="e3c9c-167">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion, Microsoft. Azure. Commands. ApiManagement, Version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3c9c-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3c9c-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3c9c-168">OUTPUTS</span></span>

### <span data-ttu-id="e3c9c-169">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3c9c-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e3c9c-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3c9c-170">NOTES</span></span>

## <span data-ttu-id="e3c9c-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3c9c-171">RELATED LINKS</span></span>

[<span data-ttu-id="e3c9c-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3c9c-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)



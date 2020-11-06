---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503909"
---
# <span data-ttu-id="6fe10-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="6fe10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fe10-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe10-103">Erstellt eine API-Verwaltungs Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6fe10-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fe10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe10-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fe10-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe10-106">Das Cmdlet **New-AzureRmApiManagement** erstellt eine API-Verwaltungs Bereitstellung in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="6fe10-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="6fe10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fe10-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe10-108">Beispiel 1: Erstellen eines API-Verwaltungsdiensts für die Entwicklerebene</span><span class="sxs-lookup"><span data-stu-id="6fe10-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="6fe10-109">Dieser Befehl erstellt einen API-Verwaltungsdienst für Entwickler Ebenen.</span><span class="sxs-lookup"><span data-stu-id="6fe10-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="6fe10-110">Der Befehl gibt die Organisation und die Administratoradresse an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="6fe10-111">Der Befehl gibt den *SKU* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="6fe10-112">Daher verwendet das Cmdlet den Standardwert von Developer.</span><span class="sxs-lookup"><span data-stu-id="6fe10-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="6fe10-113">Beispiel 2: Erstellen eines Standard Tier Diensts mit drei Einheiten</span><span class="sxs-lookup"><span data-stu-id="6fe10-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="6fe10-114">Mit diesem Befehl wird ein Standard-Tier-API-Verwaltungsdienst mit drei Einheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fe10-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="6fe10-115">Beispiel 3: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="6fe10-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="6fe10-116">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem extern zugewandten Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="6fe10-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="6fe10-117">Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="6fe10-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="6fe10-118">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem internen Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="6fe10-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="6fe10-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fe10-119">PARAMETERS</span></span>

### <span data-ttu-id="6fe10-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="6fe10-120">-AdditionalRegions</span></span>
<span data-ttu-id="6fe10-121">Zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="6fe10-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="6fe10-122">-AdminEmail</span></span>
<span data-ttu-id="6fe10-123">Gibt die ursprüngliche e-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fe10-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-124">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="6fe10-124">-Capacity</span></span>
<span data-ttu-id="6fe10-125">Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="6fe10-126">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="6fe10-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe10-127">-DefaultProfile</span></span>
<span data-ttu-id="6fe10-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fe10-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="6fe10-129">-Location</span></span>
<span data-ttu-id="6fe10-130">Gibt den Speicherort an, an dem der API-Verwaltungsdienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fe10-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="6fe10-131">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="6fe10-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe10-132">-Name</span></span>
<span data-ttu-id="6fe10-133">Gibt einen Namen für die API-Verwaltungs Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-134">-Organisation</span><span class="sxs-lookup"><span data-stu-id="6fe10-134">-Organization</span></span>
<span data-ttu-id="6fe10-135">Gibt den Namen einer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="6fe10-136">Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in e-Mail-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="6fe10-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe10-137">-ResourceGroupName</span></span>
<span data-ttu-id="6fe10-138">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungs Bereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fe10-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="6fe10-139">-Sku</span></span>
<span data-ttu-id="6fe10-140">Gibt die Stufe des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="6fe10-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="6fe10-141">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6fe10-141">Valid values are:</span></span> 

- <span data-ttu-id="6fe10-142">Entwickler</span><span class="sxs-lookup"><span data-stu-id="6fe10-142">Developer</span></span> 
- <span data-ttu-id="6fe10-143">Standard</span><span class="sxs-lookup"><span data-stu-id="6fe10-143">Standard</span></span> 
- <span data-ttu-id="6fe10-144">Premium</span><span class="sxs-lookup"><span data-stu-id="6fe10-144">Premium</span></span> 

<span data-ttu-id="6fe10-145">Der Standardwert ist Developer.</span><span class="sxs-lookup"><span data-stu-id="6fe10-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fe10-146">-Tag</span></span>
<span data-ttu-id="6fe10-147">Tags-Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="6fe10-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6fe10-148">-VirtualNetwork</span></span>
<span data-ttu-id="6fe10-149">Konfiguration des virtuellen Netzwerks des Master Azure API Management Deployment-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="6fe10-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="6fe10-150">-VpnType</span></span>
<span data-ttu-id="6fe10-151">Virtueller Netzwerktyp der ApiManagement-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6fe10-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="6fe10-152">Gültige Werte sind</span><span class="sxs-lookup"><span data-stu-id="6fe10-152">Valid Values are</span></span> 
- <span data-ttu-id="6fe10-153">"None" (Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6fe10-153">"None" (Default Value.</span></span> <span data-ttu-id="6fe10-154">ApiManagement ist nicht Bestandteileines virtuellen Netzwerks ")</span><span class="sxs-lookup"><span data-stu-id="6fe10-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="6fe10-155">"Extern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Internet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="6fe10-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="6fe10-156">"Intern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Intranet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="6fe10-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe10-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe10-157">CommonParameters</span></span>
<span data-ttu-id="6fe10-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe10-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe10-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe10-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe10-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fe10-160">INPUTS</span></span>

### <span data-ttu-id="6fe10-161">Keine</span><span class="sxs-lookup"><span data-stu-id="6fe10-161">None</span></span>
<span data-ttu-id="6fe10-162">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6fe10-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6fe10-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fe10-163">OUTPUTS</span></span>

### <span data-ttu-id="6fe10-164">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6fe10-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fe10-165">NOTES</span></span>

## <span data-ttu-id="6fe10-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fe10-166">RELATED LINKS</span></span>

[<span data-ttu-id="6fe10-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="6fe10-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="6fe10-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="6fe10-170">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6fe10-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)



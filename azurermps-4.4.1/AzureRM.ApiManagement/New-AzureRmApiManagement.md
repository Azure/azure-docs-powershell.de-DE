---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498086"
---
# <span data-ttu-id="206c0-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="206c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="206c0-102">SYNOPSIS</span></span>
<span data-ttu-id="206c0-103">Erstellt eine API-Verwaltungs Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="206c0-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="206c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="206c0-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="206c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="206c0-105">DESCRIPTION</span></span>
<span data-ttu-id="206c0-106">Das Cmdlet **New-AzureRmApiManagement** erstellt eine API-Verwaltungs Bereitstellung in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="206c0-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="206c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="206c0-107">EXAMPLES</span></span>

### <span data-ttu-id="206c0-108">Beispiel 1: Erstellen eines API-Verwaltungsdiensts für die Entwicklerebene</span><span class="sxs-lookup"><span data-stu-id="206c0-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="206c0-109">Dieser Befehl erstellt einen API-Verwaltungsdienst für Entwickler Ebenen.</span><span class="sxs-lookup"><span data-stu-id="206c0-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="206c0-110">Der Befehl gibt die Organisation und die Administratoradresse an.</span><span class="sxs-lookup"><span data-stu-id="206c0-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="206c0-111">Der Befehl gibt den *SKU* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="206c0-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="206c0-112">Daher verwendet das Cmdlet den Standardwert von Developer.</span><span class="sxs-lookup"><span data-stu-id="206c0-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="206c0-113">Beispiel 2: Erstellen eines Standard Tier Diensts mit drei Einheiten</span><span class="sxs-lookup"><span data-stu-id="206c0-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="206c0-114">Mit diesem Befehl wird ein Standard-Tier-API-Verwaltungsdienst mit drei Einheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="206c0-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="206c0-115">Beispiel 3: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="206c0-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="206c0-116">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem extern zugewandten Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="206c0-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="206c0-117">Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="206c0-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="206c0-118">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem internen Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="206c0-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="206c0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="206c0-119">PARAMETERS</span></span>

### <span data-ttu-id="206c0-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="206c0-120">-AdditionalRegions</span></span>
<span data-ttu-id="206c0-121">Zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="206c0-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="206c0-122">-AdminEmail</span></span>
<span data-ttu-id="206c0-123">Gibt die ursprüngliche e-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="206c0-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-124">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="206c0-124">-Capacity</span></span>
<span data-ttu-id="206c0-125">Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="206c0-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="206c0-126">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="206c0-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="206c0-127">-Location</span></span>
<span data-ttu-id="206c0-128">Gibt den Speicherort an, an dem mit diesem Cmdlet eine API-Verwaltungs Bereitstellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="206c0-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="206c0-129">Verwenden Sie die Get-AzureLocation-Cmdlets, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="206c0-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="206c0-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="206c0-130">Valid values are:</span></span> 

- <span data-ttu-id="206c0-131">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="206c0-131">North Central US</span></span>
- <span data-ttu-id="206c0-132">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="206c0-132">South Central US</span></span>
- <span data-ttu-id="206c0-133">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="206c0-133">Central US</span></span>
- <span data-ttu-id="206c0-134">West Europa</span><span class="sxs-lookup"><span data-stu-id="206c0-134">West Europe</span></span>
- <span data-ttu-id="206c0-135">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="206c0-135">North Europe</span></span>
- <span data-ttu-id="206c0-136">West-US</span><span class="sxs-lookup"><span data-stu-id="206c0-136">West US</span></span>
- <span data-ttu-id="206c0-137">East US</span><span class="sxs-lookup"><span data-stu-id="206c0-137">East US</span></span>
- <span data-ttu-id="206c0-138">East US 2</span><span class="sxs-lookup"><span data-stu-id="206c0-138">East US 2</span></span>
- <span data-ttu-id="206c0-139">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="206c0-139">Japan East</span></span>
- <span data-ttu-id="206c0-140">Japan West</span><span class="sxs-lookup"><span data-stu-id="206c0-140">Japan West</span></span>
- <span data-ttu-id="206c0-141">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="206c0-141">Brazil South</span></span>
- <span data-ttu-id="206c0-142">Südostasien</span><span class="sxs-lookup"><span data-stu-id="206c0-142">Southeast Asia</span></span>
- <span data-ttu-id="206c0-143">Ostasien</span><span class="sxs-lookup"><span data-stu-id="206c0-143">East Asia</span></span>
- <span data-ttu-id="206c0-144">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="206c0-144">Australia East</span></span>
- <span data-ttu-id="206c0-145">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="206c0-145">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-146">-Name</span><span class="sxs-lookup"><span data-stu-id="206c0-146">-Name</span></span>
<span data-ttu-id="206c0-147">Gibt einen Namen für die API-Verwaltungs Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="206c0-147">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-148">-Organisation</span><span class="sxs-lookup"><span data-stu-id="206c0-148">-Organization</span></span>
<span data-ttu-id="206c0-149">Gibt den Namen einer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="206c0-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="206c0-150">Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in e-Mail-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="206c0-150">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206c0-151">-ResourceGroupName</span></span>
<span data-ttu-id="206c0-152">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungs Bereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="206c0-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="206c0-153">-Sku</span></span>
<span data-ttu-id="206c0-154">Gibt die Stufe des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="206c0-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="206c0-155">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="206c0-155">Valid values are:</span></span> 

- <span data-ttu-id="206c0-156">Entwickler</span><span class="sxs-lookup"><span data-stu-id="206c0-156">Developer</span></span> 
- <span data-ttu-id="206c0-157">Standard</span><span class="sxs-lookup"><span data-stu-id="206c0-157">Standard</span></span> 
- <span data-ttu-id="206c0-158">Premium</span><span class="sxs-lookup"><span data-stu-id="206c0-158">Premium</span></span> 

<span data-ttu-id="206c0-159">Der Standardwert ist Developer.</span><span class="sxs-lookup"><span data-stu-id="206c0-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-160">-Tags</span><span class="sxs-lookup"><span data-stu-id="206c0-160">-Tags</span></span>
<span data-ttu-id="206c0-161">Gibt ein Wörterbuch mit Tags an.</span><span class="sxs-lookup"><span data-stu-id="206c0-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="206c0-162">-VirtualNetwork</span></span>
<span data-ttu-id="206c0-163">Konfiguration des virtuellen Netzwerks des Master Azure API Management Deployment-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="206c0-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="206c0-164">-VpnType</span></span>
<span data-ttu-id="206c0-165">Virtueller Netzwerktyp der ApiManagement-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="206c0-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="206c0-166">Gültige Werte sind</span><span class="sxs-lookup"><span data-stu-id="206c0-166">Valid Values are</span></span> 
- <span data-ttu-id="206c0-167">"None" (Standardwert.</span><span class="sxs-lookup"><span data-stu-id="206c0-167">"None" (Default Value.</span></span> <span data-ttu-id="206c0-168">ApiManagement ist nicht Bestandteileines virtuellen Netzwerks ")</span><span class="sxs-lookup"><span data-stu-id="206c0-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="206c0-169">"Extern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Internet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="206c0-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="206c0-170">"Intern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Intranet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="206c0-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206c0-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206c0-171">-DefaultProfile</span></span>
<span data-ttu-id="206c0-172">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="206c0-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="206c0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206c0-173">CommonParameters</span></span>
<span data-ttu-id="206c0-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206c0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206c0-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206c0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206c0-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="206c0-176">INPUTS</span></span>

## <span data-ttu-id="206c0-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="206c0-177">OUTPUTS</span></span>

### <span data-ttu-id="206c0-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="206c0-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="206c0-179">NOTES</span></span>

## <span data-ttu-id="206c0-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="206c0-180">RELATED LINKS</span></span>

[<span data-ttu-id="206c0-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="206c0-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="206c0-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="206c0-184">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="206c0-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471438"
---
# <span data-ttu-id="44c67-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-101">New-AzApiManagement</span></span>

## <span data-ttu-id="44c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c67-102">SYNOPSIS</span></span>
<span data-ttu-id="44c67-103">Erstellt eine API-Verwaltungsbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="44c67-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="44c67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44c67-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44c67-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44c67-105">DESCRIPTION</span></span>
<span data-ttu-id="44c67-106">Das **Cmdlet "New-AzApiManagement"** erstellt eine API-Verwaltungsbereitstellung in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="44c67-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="44c67-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44c67-107">EXAMPLES</span></span>

### <span data-ttu-id="44c67-108">Beispiel 1: Erstellen eines API-Verwaltungsdiensts auf Entwicklerebene</span><span class="sxs-lookup"><span data-stu-id="44c67-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="44c67-109">Mit diesem Befehl wird ein API-Verwaltungsdienst auf Entwicklerebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="44c67-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="44c67-110">Der Befehl gibt die Organisation und die Administratoradresse an.</span><span class="sxs-lookup"><span data-stu-id="44c67-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="44c67-111">Der Befehl gibt den *SKU-Parameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="44c67-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="44c67-112">Daher verwendet das Cmdlet den Standardwert "Developer".</span><span class="sxs-lookup"><span data-stu-id="44c67-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="44c67-113">Beispiel 2: Erstellen eines Standarddiensts mit drei Einheiten</span><span class="sxs-lookup"><span data-stu-id="44c67-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="44c67-114">Mit diesem Befehl wird ein Api-Verwaltungsdienst der Standardebene erstellt, der drei Einheiten hat.</span><span class="sxs-lookup"><span data-stu-id="44c67-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="44c67-115">Beispiel 3: Erstellen eines Verbrauchsstufendiensts</span><span class="sxs-lookup"><span data-stu-id="44c67-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="44c67-116">Dieser Befehl erstellt einen API-Verwaltungsdienst auf Verbrauchsebene mit aktivierten Clientzertifikaten in Westeuropa.</span><span class="sxs-lookup"><span data-stu-id="44c67-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="44c67-117">Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="44c67-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="44c67-118">Dieser Befehl erstellt einen Premium-API-Verwaltungsdienst in einem virtuellen Azure-Netzwerk-Subnetz, das einen extern gerichteten Gatewayendpunkt mit einer Masterregion in den USA hat.</span><span class="sxs-lookup"><span data-stu-id="44c67-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="44c67-119">Beispiel 5: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="44c67-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="44c67-120">Mit diesem Befehl wird ein Premium-API-Verwaltungsdienst in einem virtuellen Azure-Netzwerk-Subnetz mit einem intern gerichteten Gatewayendpunkt mit einer Masterregion in den USA erstellt.</span><span class="sxs-lookup"><span data-stu-id="44c67-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="44c67-121">Beispiel 6: Erstellen eines API-Verwaltungsdiensts und Aktivieren des TLS 1.0-Protokolls</span><span class="sxs-lookup"><span data-stu-id="44c67-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="44c67-122">Dieser Befehl erstellt einen Standard-SKU-Api-Verwaltungsdienst und aktiviert TLS 1.0 auf dem Frontend-Client für das ApiManagement Gateway und den Back-End-Client zwischen ApiManagement Gateway und Back-End.</span><span class="sxs-lookup"><span data-stu-id="44c67-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="44c67-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44c67-123">PARAMETERS</span></span>

### <span data-ttu-id="44c67-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="44c67-124">-AdditionalRegions</span></span>
<span data-ttu-id="44c67-125">Weitere Bereitstellungsregionen von Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="44c67-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="44c67-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="44c67-126">-AdminEmail</span></span>
<span data-ttu-id="44c67-127">Gibt die ursprüngliche E-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="44c67-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="44c67-128">-Capacity</span><span class="sxs-lookup"><span data-stu-id="44c67-128">-Capacity</span></span>
<span data-ttu-id="44c67-129">Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="44c67-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="44c67-130">Die Standardeinstellung ist eine (1).</span><span class="sxs-lookup"><span data-stu-id="44c67-130">The default is one (1).</span></span>

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

### <span data-ttu-id="44c67-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="44c67-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="44c67-132">Benutzerdefinierte Hostnamenkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="44c67-132">Custom hostname configurations.</span></span> <span data-ttu-id="44c67-133">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="44c67-133">Default value is $null.</span></span> <span data-ttu-id="44c67-134">Durch $null wird der Standardhostname festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44c67-134">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c67-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c67-135">-DefaultProfile</span></span>
<span data-ttu-id="44c67-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44c67-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44c67-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="44c67-137">-EnableClientCertificate</span></span>
<span data-ttu-id="44c67-138">Das Kennzeichen ist nur für die Verwendung des SKU-ApiManagement-Diensts (Consumption SKU ApiManagement Service) gedacht.</span><span class="sxs-lookup"><span data-stu-id="44c67-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="44c67-139">Dadurch wird ein Clientzertifikat erzwungen, das bei jeder Anforderung an das Gateway präsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="44c67-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="44c67-140">Dadurch kann das Zertifikat auch in der Richtlinie auf dem Gateway authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="44c67-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="44c67-141">-Location</span><span class="sxs-lookup"><span data-stu-id="44c67-141">-Location</span></span>
<span data-ttu-id="44c67-142">Gibt den Speicherort an, an dem der Api-Verwaltungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="44c67-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="44c67-143">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="44c67-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="44c67-144">-Name</span><span class="sxs-lookup"><span data-stu-id="44c67-144">-Name</span></span>
<span data-ttu-id="44c67-145">Gibt einen Namen für die API-Verwaltungsbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="44c67-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="44c67-146">-Organisation</span><span class="sxs-lookup"><span data-stu-id="44c67-146">-Organization</span></span>
<span data-ttu-id="44c67-147">Gibt den Namen einer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="44c67-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="44c67-148">Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in E-Mail-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="44c67-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="44c67-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c67-149">-ResourceGroupName</span></span>
<span data-ttu-id="44c67-150">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungsbereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="44c67-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="44c67-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="44c67-151">-Sku</span></span>
<span data-ttu-id="44c67-152">Gibt die Stufe des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="44c67-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="44c67-153">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="44c67-153">Valid values are:</span></span> 
- <span data-ttu-id="44c67-154">Entwickler</span><span class="sxs-lookup"><span data-stu-id="44c67-154">Developer</span></span> 
- <span data-ttu-id="44c67-155">Standard</span><span class="sxs-lookup"><span data-stu-id="44c67-155">Standard</span></span> 
- <span data-ttu-id="44c67-156">Premium Die Standardeinstellung ist "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="44c67-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c67-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="44c67-157">-SslSetting</span></span>
<span data-ttu-id="44c67-158">Die Ssl-Einstellung des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="44c67-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="44c67-159">Der Standardwert ist $null</span><span class="sxs-lookup"><span data-stu-id="44c67-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c67-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="44c67-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="44c67-161">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diesen Server zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="44c67-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="44c67-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="44c67-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="44c67-163">Von der internen Zertifizierungsstelle ausgestellte Zertifikate, die auf dem Dienst installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44c67-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="44c67-164">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="44c67-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c67-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="44c67-165">-Tag</span></span>
<span data-ttu-id="44c67-166">Kategorienwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="44c67-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="44c67-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="44c67-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="44c67-168">Weisen Sie diesem Server Benutzeridentitäten zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="44c67-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c67-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44c67-169">-VirtualNetwork</span></span>
<span data-ttu-id="44c67-170">Virtual Network Configuration of master Azure API Management deployment region.</span><span class="sxs-lookup"><span data-stu-id="44c67-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="44c67-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="44c67-171">-VpnType</span></span>
<span data-ttu-id="44c67-172">Virtueller Netzwerktyp der ApiManagement-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="44c67-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="44c67-173">Gültige Werte sind</span><span class="sxs-lookup"><span data-stu-id="44c67-173">Valid Values are</span></span> 
- <span data-ttu-id="44c67-174">"None" (Standardwert.</span><span class="sxs-lookup"><span data-stu-id="44c67-174">"None" (Default Value.</span></span> <span data-ttu-id="44c67-175">ApiManagement ist kein Teil eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="44c67-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="44c67-176">"Extern" (ApiManagement Deployment wird in einem virtuellen Netzwerk eingerichtet, das einen internet gerichteten Endpunkt hat)</span><span class="sxs-lookup"><span data-stu-id="44c67-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="44c67-177">"Intern" (ApiManagement Deployment wird in einem virtuellen Netzwerk eingerichtet, das einen Endpunkt mit Intranetaus gerichtet hat)</span><span class="sxs-lookup"><span data-stu-id="44c67-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="44c67-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c67-178">CommonParameters</span></span>
<span data-ttu-id="44c67-179">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c67-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c67-180">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44c67-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c67-181">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44c67-181">INPUTS</span></span>

### <span data-ttu-id="44c67-182">System.String</span><span class="sxs-lookup"><span data-stu-id="44c67-182">System.String</span></span>

### <span data-ttu-id="44c67-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="44c67-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="44c67-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44c67-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="44c67-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44c67-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="44c67-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44c67-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="44c67-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="44c67-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="44c67-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="44c67-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="44c67-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="44c67-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="44c67-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44c67-190">OUTPUTS</span></span>

### <span data-ttu-id="44c67-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="44c67-192">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44c67-192">NOTES</span></span>

## <span data-ttu-id="44c67-193">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44c67-193">RELATED LINKS</span></span>

[<span data-ttu-id="44c67-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="44c67-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="44c67-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="44c67-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="44c67-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="44c67-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



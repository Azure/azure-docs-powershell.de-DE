---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159729"
---
# <span data-ttu-id="c04b1-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-101">New-AzApiManagement</span></span>

## <span data-ttu-id="c04b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c04b1-103">Erstellt eine API-Verwaltungsbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c04b1-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="c04b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c04b1-104">SYNTAX</span></span>

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

## <span data-ttu-id="c04b1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c04b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c04b1-106">Das **Cmdlet "New-AzApiManagement"** erstellt eine API-Verwaltungsbereitstellung in Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c04b1-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="c04b1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c04b1-107">EXAMPLES</span></span>

### <span data-ttu-id="c04b1-108">Beispiel 1: Erstellen eines API-Verwaltungsdiensts auf Entwicklerebene</span><span class="sxs-lookup"><span data-stu-id="c04b1-108">Example 1: Create a Developer tier API Management service</span></span>
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

<span data-ttu-id="c04b1-109">Mit diesem Befehl wird ein API-Verwaltungsdienst auf Entwicklerebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="c04b1-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="c04b1-110">Der Befehl gibt die Organisation und die Administratoradresse an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="c04b1-111">Der Befehl gibt den *SKU-Parameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="c04b1-112">Daher verwendet das Cmdlet den Standardwert "Developer".</span><span class="sxs-lookup"><span data-stu-id="c04b1-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="c04b1-113">Beispiel 2: Erstellen eines Diensts der Ebene "Standard" mit drei Einheiten</span><span class="sxs-lookup"><span data-stu-id="c04b1-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="c04b1-114">Mit diesem Befehl wird ein Api-Verwaltungsdienst der Standardebene erstellt, der drei Einheiten hat.</span><span class="sxs-lookup"><span data-stu-id="c04b1-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="c04b1-115">Beispiel 3: Erstellen eines Verbrauchsstufendiensts</span><span class="sxs-lookup"><span data-stu-id="c04b1-115">Example 3: Create a Consumption tier service</span></span>
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

<span data-ttu-id="c04b1-116">Dieser Befehl erstellt einen API-Verwaltungsdienst auf Verbrauchsebene mit aktivierten Clientzertifikaten in Westeuropa.</span><span class="sxs-lookup"><span data-stu-id="c04b1-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="c04b1-117">Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c04b1-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="c04b1-118">Mit diesem Befehl wird ein Premium-API-Verwaltungsdienst in einem virtuellen Azure-Netzwerk-Subnetz mit einem extern gerichteten Gatewayendpunkt mit einer Masterregion in den USA erstellt.</span><span class="sxs-lookup"><span data-stu-id="c04b1-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="c04b1-119">Beispiel 5: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c04b1-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="c04b1-120">Mit diesem Befehl wird ein Premium-API-Verwaltungsdienst in einem virtuellen Azure-Netzwerk-Subnetz mit einem intern gerichteten Gatewayendpunkt mit einer Masterregion in den USA erstellt.</span><span class="sxs-lookup"><span data-stu-id="c04b1-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="c04b1-121">Beispiel 6: Erstellen eines API-Verwaltungsdiensts und Aktivieren des TLS 1.0-Protokolls</span><span class="sxs-lookup"><span data-stu-id="c04b1-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="c04b1-122">Dieser Befehl erstellt einen Standard-SKU-Api-Verwaltungsdienst und aktiviert TLS 1.0 auf dem Frontend-Client für das ApiManagement Gateway und den Back-End-Client zwischen ApiManagement Gateway und Back-End.</span><span class="sxs-lookup"><span data-stu-id="c04b1-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="c04b1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c04b1-123">PARAMETERS</span></span>

### <span data-ttu-id="c04b1-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="c04b1-124">-AdditionalRegions</span></span>
<span data-ttu-id="c04b1-125">Weitere Bereitstellungsregionen von Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c04b1-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="c04b1-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="c04b1-126">-AdminEmail</span></span>
<span data-ttu-id="c04b1-127">Gibt die ursprüngliche E-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c04b1-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="c04b1-128">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c04b1-128">-Capacity</span></span>
<span data-ttu-id="c04b1-129">Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="c04b1-130">Die Standardeinstellung ist eine (1).</span><span class="sxs-lookup"><span data-stu-id="c04b1-130">The default is one (1).</span></span>

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

### <span data-ttu-id="c04b1-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c04b1-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="c04b1-132">Benutzerdefinierte Hostnamenkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c04b1-132">Custom hostname configurations.</span></span> <span data-ttu-id="c04b1-133">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="c04b1-133">Default value is $null.</span></span> <span data-ttu-id="c04b1-134">Durch $null wird der Standardhostname festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c04b1-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="c04b1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04b1-135">-DefaultProfile</span></span>
<span data-ttu-id="c04b1-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c04b1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c04b1-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c04b1-137">-EnableClientCertificate</span></span>
<span data-ttu-id="c04b1-138">Das Kennzeichen ist nur für die Verwendung des SKU-ApiManagement-Diensts (Consumption SKU ApiManagement Service) gedacht.</span><span class="sxs-lookup"><span data-stu-id="c04b1-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="c04b1-139">Dadurch wird ein Clientzertifikat erzwungen, das bei jeder Anforderung an das Gateway präsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="c04b1-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="c04b1-140">Dadurch kann das Zertifikat auch in der Richtlinie auf dem Gateway authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c04b1-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="c04b1-141">-Location</span><span class="sxs-lookup"><span data-stu-id="c04b1-141">-Location</span></span>
<span data-ttu-id="c04b1-142">Gibt den Speicherort an, an dem der Api-Verwaltungsdienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c04b1-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="c04b1-143">Um gültige Speicherorte zu erhalten, verwenden Sie das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="c04b1-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c04b1-144">-Name</span><span class="sxs-lookup"><span data-stu-id="c04b1-144">-Name</span></span>
<span data-ttu-id="c04b1-145">Gibt einen Namen für die API-Verwaltungsbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="c04b1-146">-Organisation</span><span class="sxs-lookup"><span data-stu-id="c04b1-146">-Organization</span></span>
<span data-ttu-id="c04b1-147">Gibt den Namen einer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="c04b1-148">Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in E-Mail-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c04b1-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="c04b1-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04b1-149">-ResourceGroupName</span></span>
<span data-ttu-id="c04b1-150">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungsbereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="c04b1-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="c04b1-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="c04b1-151">-Sku</span></span>
<span data-ttu-id="c04b1-152">Gibt die Stufe des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="c04b1-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="c04b1-153">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c04b1-153">Valid values are:</span></span> 
- <span data-ttu-id="c04b1-154">Entwickler</span><span class="sxs-lookup"><span data-stu-id="c04b1-154">Developer</span></span> 
- <span data-ttu-id="c04b1-155">Standard</span><span class="sxs-lookup"><span data-stu-id="c04b1-155">Standard</span></span> 
- <span data-ttu-id="c04b1-156">Premium Die Standardeinstellung ist "Entwickler".</span><span class="sxs-lookup"><span data-stu-id="c04b1-156">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="c04b1-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="c04b1-157">-SslSetting</span></span>
<span data-ttu-id="c04b1-158">Die Ssl-Einstellung des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c04b1-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="c04b1-159">Der Standardwert ist $null</span><span class="sxs-lookup"><span data-stu-id="c04b1-159">Default value is $null</span></span>

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

### <span data-ttu-id="c04b1-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c04b1-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c04b1-161">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diesen Server zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c04b1-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c04b1-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c04b1-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="c04b1-163">Von der internen Zertifizierungsstelle ausgestellte Zertifikate, die auf dem Dienst installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c04b1-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="c04b1-164">Der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="c04b1-164">Default value is $null.</span></span>

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

### <span data-ttu-id="c04b1-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="c04b1-165">-Tag</span></span>
<span data-ttu-id="c04b1-166">Kategorienwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="c04b1-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="c04b1-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c04b1-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="c04b1-168">Weisen Sie diesem Server Benutzeridentitäten zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="c04b1-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c04b1-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c04b1-169">-VirtualNetwork</span></span>
<span data-ttu-id="c04b1-170">Virtual Network Configuration of master Azure API Management deployment region.</span><span class="sxs-lookup"><span data-stu-id="c04b1-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="c04b1-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c04b1-171">-VpnType</span></span>
<span data-ttu-id="c04b1-172">Virtueller Netzwerktyp der ApiManagement-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c04b1-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="c04b1-173">Gültige Werte sind</span><span class="sxs-lookup"><span data-stu-id="c04b1-173">Valid Values are</span></span> 
- <span data-ttu-id="c04b1-174">"None" (Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c04b1-174">"None" (Default Value.</span></span> <span data-ttu-id="c04b1-175">ApiManagement ist kein Teil eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="c04b1-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="c04b1-176">"Extern" (ApiManagement Deployment wird in einem virtuellen Netzwerk eingerichtet, das einen internet gerichteten Endpunkt hat)</span><span class="sxs-lookup"><span data-stu-id="c04b1-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="c04b1-177">"Intern" (Die Bereitstellung von ApiManagement ist in einem virtuellen Netzwerk eingerichtet, das über einen Endpunkt in einem Intranet verfügen)</span><span class="sxs-lookup"><span data-stu-id="c04b1-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="c04b1-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04b1-178">CommonParameters</span></span>
<span data-ttu-id="c04b1-179">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04b1-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04b1-180">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c04b1-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04b1-181">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c04b1-181">INPUTS</span></span>

### <span data-ttu-id="c04b1-182">System.String</span><span class="sxs-lookup"><span data-stu-id="c04b1-182">System.String</span></span>

### <span data-ttu-id="c04b1-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c04b1-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c04b1-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c04b1-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c04b1-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c04b1-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="c04b1-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c04b1-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c04b1-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="c04b1-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="c04b1-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c04b1-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="c04b1-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="c04b1-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="c04b1-190">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c04b1-190">OUTPUTS</span></span>

### <span data-ttu-id="c04b1-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c04b1-192">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c04b1-192">NOTES</span></span>

## <span data-ttu-id="c04b1-193">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c04b1-193">RELATED LINKS</span></span>

[<span data-ttu-id="c04b1-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="c04b1-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c04b1-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="c04b1-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c04b1-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c04b1-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



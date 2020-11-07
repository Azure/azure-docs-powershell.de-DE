---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650358"
---
# <span data-ttu-id="c852d-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-101">New-AzApiManagement</span></span>

## <span data-ttu-id="c852d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c852d-102">SYNOPSIS</span></span>
<span data-ttu-id="c852d-103">Erstellt eine API-Verwaltungs Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c852d-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="c852d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c852d-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c852d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c852d-105">DESCRIPTION</span></span>
<span data-ttu-id="c852d-106">Das Cmdlet **New-AzApiManagement** erstellt eine API-Verwaltungs Bereitstellung in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="c852d-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="c852d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c852d-107">EXAMPLES</span></span>

### <span data-ttu-id="c852d-108">Beispiel 1: Erstellen eines API-Verwaltungsdiensts für die Entwicklerebene</span><span class="sxs-lookup"><span data-stu-id="c852d-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="c852d-109">Dieser Befehl erstellt einen API-Verwaltungsdienst für Entwickler Ebenen.</span><span class="sxs-lookup"><span data-stu-id="c852d-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="c852d-110">Der Befehl gibt die Organisation und die Administratoradresse an.</span><span class="sxs-lookup"><span data-stu-id="c852d-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="c852d-111">Der Befehl gibt den *SKU* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="c852d-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="c852d-112">Daher verwendet das Cmdlet den Standardwert von Developer.</span><span class="sxs-lookup"><span data-stu-id="c852d-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="c852d-113">Beispiel 2: Erstellen eines Standard Tier Diensts mit drei Einheiten</span><span class="sxs-lookup"><span data-stu-id="c852d-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="c852d-114">Mit diesem Befehl wird ein Standard-Tier-API-Verwaltungsdienst mit drei Einheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="c852d-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="c852d-115">Beispiel 3: Erstellen eines API-Verwaltungsdiensts für ein externes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c852d-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="c852d-116">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem extern zugewandten Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="c852d-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="c852d-117">Beispiel 4: Erstellen eines API-Verwaltungsdiensts für ein internes virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c852d-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="c852d-118">Dieser Befehl erstellt einen Premium-Tier-API-Verwaltungsdienst in einem Azure Virtual Network-Subnetz mit einem internen Gateway-Endpunkt mit einem Masterbereich im Westen der USA.</span><span class="sxs-lookup"><span data-stu-id="c852d-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="c852d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c852d-119">PARAMETERS</span></span>

### <span data-ttu-id="c852d-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="c852d-120">-AdditionalRegions</span></span>
<span data-ttu-id="c852d-121">Zusätzliche Bereitstellungsbereiche der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="c852d-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="c852d-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="c852d-122">-AdminEmail</span></span>
<span data-ttu-id="c852d-123">Gibt die ursprüngliche e-Mail-Adresse für alle Benachrichtigungen an, die vom API-Verwaltungssystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c852d-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="c852d-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c852d-124">-AssignIdentity</span></span>
<span data-ttu-id="c852d-125">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c852d-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c852d-126">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="c852d-126">-Capacity</span></span>
<span data-ttu-id="c852d-127">Gibt die SKU-Kapazität des Azure API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="c852d-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="c852d-128">Der Standardwert ist eins (1).</span><span class="sxs-lookup"><span data-stu-id="c852d-128">The default is one (1).</span></span>

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

### <span data-ttu-id="c852d-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c852d-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="c852d-130">Benutzerdefinierte Hostname-Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c852d-130">Custom hostname configurations.</span></span> <span data-ttu-id="c852d-131">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="c852d-131">Default value is $null.</span></span> <span data-ttu-id="c852d-132">Durch Übergabe $NULL wird der Standardhostname gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c852d-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="c852d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c852d-133">-DefaultProfile</span></span>
<span data-ttu-id="c852d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c852d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c852d-135">-Standort</span><span class="sxs-lookup"><span data-stu-id="c852d-135">-Location</span></span>
<span data-ttu-id="c852d-136">Gibt den Speicherort an, an dem der API-Verwaltungsdienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c852d-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="c852d-137">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="c852d-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c852d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="c852d-138">-Name</span></span>
<span data-ttu-id="c852d-139">Gibt einen Namen für die API-Verwaltungs Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="c852d-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="c852d-140">-Organisation</span><span class="sxs-lookup"><span data-stu-id="c852d-140">-Organization</span></span>
<span data-ttu-id="c852d-141">Gibt den Namen einer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="c852d-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="c852d-142">Die API-Verwaltung verwendet diese Adresse im Entwicklerportal in e-Mail-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c852d-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="c852d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c852d-143">-ResourceGroupName</span></span>
<span data-ttu-id="c852d-144">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine API-Verwaltungs Bereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="c852d-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="c852d-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="c852d-145">-Sku</span></span>
<span data-ttu-id="c852d-146">Gibt die Stufe des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="c852d-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="c852d-147">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="c852d-147">Valid values are:</span></span> 
- <span data-ttu-id="c852d-148">Entwickler</span><span class="sxs-lookup"><span data-stu-id="c852d-148">Developer</span></span> 
- <span data-ttu-id="c852d-149">Standard</span><span class="sxs-lookup"><span data-stu-id="c852d-149">Standard</span></span> 
- <span data-ttu-id="c852d-150">Premium der Standardwert ist Developer.</span><span class="sxs-lookup"><span data-stu-id="c852d-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852d-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="c852d-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="c852d-152">Zertifikate, die von der internen Zertifizierungsstelle ausgestellt werden, um auf dem Dienst installiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="c852d-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="c852d-153">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="c852d-153">Default value is $null.</span></span>

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

### <span data-ttu-id="c852d-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="c852d-154">-Tag</span></span>
<span data-ttu-id="c852d-155">Tags-Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="c852d-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="c852d-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c852d-156">-VirtualNetwork</span></span>
<span data-ttu-id="c852d-157">Konfiguration des virtuellen Netzwerks des Master Azure API Management Deployment-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c852d-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="c852d-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c852d-158">-VpnType</span></span>
<span data-ttu-id="c852d-159">Virtueller Netzwerktyp der ApiManagement-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c852d-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="c852d-160">Gültige Werte sind</span><span class="sxs-lookup"><span data-stu-id="c852d-160">Valid Values are</span></span> 
- <span data-ttu-id="c852d-161">"None" (Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c852d-161">"None" (Default Value.</span></span> <span data-ttu-id="c852d-162">ApiManagement ist nicht Bestandteileines virtuellen Netzwerks ")</span><span class="sxs-lookup"><span data-stu-id="c852d-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="c852d-163">"Extern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Internet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="c852d-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="c852d-164">"Intern" (ApiManagement-Bereitstellung erfolgt in einem virtuellen Netzwerk mit einem Intranet-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="c852d-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="c852d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c852d-165">CommonParameters</span></span>
<span data-ttu-id="c852d-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c852d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c852d-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c852d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c852d-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c852d-168">INPUTS</span></span>

### <span data-ttu-id="c852d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="c852d-169">System.String</span></span>

### <span data-ttu-id="c852d-170">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c852d-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c852d-171">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c852d-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c852d-172">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c852d-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="c852d-173">System. Collections. Generic. Dictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Kultur = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c852d-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c852d-174">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="c852d-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="c852d-175">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="c852d-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="c852d-176">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="c852d-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="c852d-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c852d-177">OUTPUTS</span></span>

### <span data-ttu-id="c852d-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c852d-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="c852d-179">NOTES</span></span>

## <span data-ttu-id="c852d-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c852d-180">RELATED LINKS</span></span>

[<span data-ttu-id="c852d-181">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="c852d-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c852d-183">Satz-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="c852d-184">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c852d-185">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c852d-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



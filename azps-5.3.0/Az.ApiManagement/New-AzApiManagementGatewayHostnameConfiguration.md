---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471410"
---
# <span data-ttu-id="a0f5c-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f5c-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="a0f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f5c-103">Erstellt eine Hostnamenkonfigurierung für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="a0f5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f5c-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f5c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f5c-106">Das **Cmdlet "New-AzApiManagementGatewayHostnameConfiguration"** erstellt eine Hostnamenkonfigurierung für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="a0f5c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="a0f5c-108">Beispiel 1: Erstellen einer Hostnamenkonfiguration für das vorhandene Gateway</span><span class="sxs-lookup"><span data-stu-id="a0f5c-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="a0f5c-109">Mit diesem Befehl wird eine Konfiguration des Hostnamens "h01" für ein "g01"-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="a0f5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="a0f5c-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f5c-111">-CertificateResourceId</span></span>
<span data-ttu-id="a0f5c-112">Eine Ressourcen-ID für die vorhandene Zertifikat-ID. Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="a0f5c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a0f5c-113">-Context</span></span>
<span data-ttu-id="a0f5c-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a0f5c-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f5c-116">-DefaultProfile</span></span>
<span data-ttu-id="a0f5c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f5c-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a0f5c-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="a0f5c-119">Id des neuen Hostnamens des Gateways.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="a0f5c-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-120">This parameter is optional.</span></span>
<span data-ttu-id="a0f5c-121">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-121">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f5c-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a0f5c-122">-GatewayId</span></span>
<span data-ttu-id="a0f5c-123">ID eines vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="a0f5c-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a0f5c-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="a0f5c-125">-Hostname</span></span>
<span data-ttu-id="a0f5c-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-126">Hostname.</span></span>
<span data-ttu-id="a0f5c-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a0f5c-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a0f5c-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="a0f5c-129">Flag zum Erzwingen von NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="a0f5c-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f5c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f5c-131">-Confirm</span></span>
<span data-ttu-id="a0f5c-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f5c-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0f5c-133">-WhatIf</span></span>
<span data-ttu-id="a0f5c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0f5c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f5c-136">CommonParameters</span></span>
<span data-ttu-id="a0f5c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f5c-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0f5c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f5c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f5c-139">INPUTS</span></span>

### <span data-ttu-id="a0f5c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a0f5c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a0f5c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a0f5c-141">System.String</span></span>

### <span data-ttu-id="a0f5c-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0f5c-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0f5c-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f5c-143">OUTPUTS</span></span>

### <span data-ttu-id="a0f5c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f5c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="a0f5c-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0f5c-145">NOTES</span></span>

## <span data-ttu-id="a0f5c-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0f5c-146">RELATED LINKS</span></span>

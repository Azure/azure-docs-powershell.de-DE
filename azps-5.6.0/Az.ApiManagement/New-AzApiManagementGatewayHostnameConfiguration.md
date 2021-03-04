---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 98e160253db571c32fe14455b8642337029a9707
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925379"
---
# <span data-ttu-id="6bdc6-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bdc6-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="6bdc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdc6-103">Erstellt einen Hostnamenkonfiguratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="6bdc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bdc6-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bdc6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdc6-106">Das **Cmdlet New-AzApiManagementGatewayHostnameConfiguration** erstellt ein Hostnamenkonfiguratin für das vorhandene Gateway.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="6bdc6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bdc6-107">EXAMPLES</span></span>

### <span data-ttu-id="6bdc6-108">Beispiel 1: Erstellen einer Hostnamenkonfiguration für das vorhandene Gateway</span><span class="sxs-lookup"><span data-stu-id="6bdc6-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="6bdc6-109">Mit diesem Befehl wird eine "h01"-Hostnamenkonfiguration für ein "g01"-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="6bdc6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bdc6-110">PARAMETERS</span></span>

### <span data-ttu-id="6bdc6-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="6bdc6-111">-CertificateResourceId</span></span>
<span data-ttu-id="6bdc6-112">Ein Ressourcenbezeichner für die vorhandene Zertifikat-ID. Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="6bdc6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6bdc6-113">-Context</span></span>
<span data-ttu-id="6bdc6-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6bdc6-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6bdc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdc6-116">-DefaultProfile</span></span>
<span data-ttu-id="6bdc6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bdc6-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6bdc6-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="6bdc6-119">Bezeichner des neuen Gatewayhostnamens confiuration.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="6bdc6-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-120">This parameter is optional.</span></span>
<span data-ttu-id="6bdc6-121">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="6bdc6-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6bdc6-122">-GatewayId</span></span>
<span data-ttu-id="6bdc6-123">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="6bdc6-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-124">This parameter is required.</span></span>

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

### <span data-ttu-id="6bdc6-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="6bdc6-125">-Hostname</span></span>
<span data-ttu-id="6bdc6-126">Hostname.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-126">Hostname.</span></span>
<span data-ttu-id="6bdc6-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-127">This parameter is required.</span></span>

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

### <span data-ttu-id="6bdc6-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6bdc6-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="6bdc6-129">Kennzeichnen, um NegotiateClientCertificate zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="6bdc6-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bdc6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bdc6-131">-Confirm</span></span>
<span data-ttu-id="6bdc6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdc6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdc6-133">-WhatIf</span></span>
<span data-ttu-id="6bdc6-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bdc6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bdc6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdc6-136">CommonParameters</span></span>
<span data-ttu-id="6bdc6-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdc6-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bdc6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdc6-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bdc6-139">INPUTS</span></span>

### <span data-ttu-id="6bdc6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6bdc6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bdc6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6bdc6-141">System.String</span></span>

### <span data-ttu-id="6bdc6-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bdc6-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bdc6-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bdc6-143">OUTPUTS</span></span>

### <span data-ttu-id="6bdc6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bdc6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="6bdc6-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bdc6-145">NOTES</span></span>

## <span data-ttu-id="6bdc6-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bdc6-146">RELATED LINKS</span></span>

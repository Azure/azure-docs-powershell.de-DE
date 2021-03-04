---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 9c6d556845192a4bd6e5d6c856d113be4a4074a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929123"
---
# <span data-ttu-id="535fb-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="535fb-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="535fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="535fb-102">SYNOPSIS</span></span>
<span data-ttu-id="535fb-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="535fb-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="535fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="535fb-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="535fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="535fb-105">DESCRIPTION</span></span>
<span data-ttu-id="535fb-106">Das **Add-AzApiManagementApiToGateway-Cmdlet** fügt einem Gateway eine Azure-API-Verwaltungs-API hinzu.</span><span class="sxs-lookup"><span data-stu-id="535fb-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="535fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="535fb-107">EXAMPLES</span></span>

### <span data-ttu-id="535fb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="535fb-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="535fb-109">Mit diesem Befehl wird die angegebene API zum angegebenen Gateway addiert.</span><span class="sxs-lookup"><span data-stu-id="535fb-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="535fb-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="535fb-110">PARAMETERS</span></span>

### <span data-ttu-id="535fb-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="535fb-111">-ApiId</span></span>
<span data-ttu-id="535fb-112">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="535fb-112">Identifier of existing API.</span></span>
<span data-ttu-id="535fb-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="535fb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="535fb-114">-Context</span><span class="sxs-lookup"><span data-stu-id="535fb-114">-Context</span></span>
<span data-ttu-id="535fb-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="535fb-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="535fb-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="535fb-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535fb-117">-DefaultProfile</span></span>
<span data-ttu-id="535fb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="535fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="535fb-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="535fb-119">-GatewayId</span></span>
<span data-ttu-id="535fb-120">Bezeichner des vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="535fb-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="535fb-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="535fb-121">This parameter is required.</span></span>

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

### <span data-ttu-id="535fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="535fb-122">-PassThru</span></span>
<span data-ttu-id="535fb-123">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="535fb-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="535fb-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="535fb-124">This parameter is optional.</span></span>
<span data-ttu-id="535fb-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="535fb-125">Default value is false.</span></span>

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

### <span data-ttu-id="535fb-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="535fb-126">-ProvisioningState</span></span>
<span data-ttu-id="535fb-127">Bereitstellungszustand (Erstellt).</span><span class="sxs-lookup"><span data-stu-id="535fb-127">Provisioning State (Created).</span></span>
<span data-ttu-id="535fb-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="535fb-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535fb-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="535fb-129">-Confirm</span></span>
<span data-ttu-id="535fb-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="535fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="535fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535fb-131">-WhatIf</span></span>
<span data-ttu-id="535fb-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="535fb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="535fb-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="535fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="535fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535fb-134">CommonParameters</span></span>
<span data-ttu-id="535fb-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="535fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535fb-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="535fb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535fb-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="535fb-137">INPUTS</span></span>

### <span data-ttu-id="535fb-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="535fb-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="535fb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="535fb-139">System.String</span></span>

### <span data-ttu-id="535fb-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="535fb-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="535fb-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="535fb-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="535fb-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="535fb-142">OUTPUTS</span></span>

### <span data-ttu-id="535fb-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="535fb-143">System.Boolean</span></span>

## <span data-ttu-id="535fb-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="535fb-144">NOTES</span></span>

## <span data-ttu-id="535fb-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="535fb-145">RELATED LINKS</span></span>

[<span data-ttu-id="535fb-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="535fb-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)
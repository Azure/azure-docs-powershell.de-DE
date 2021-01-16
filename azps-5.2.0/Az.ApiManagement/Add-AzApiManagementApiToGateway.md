---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301419"
---
# <span data-ttu-id="76d58-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="76d58-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="76d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d58-102">SYNOPSIS</span></span>
<span data-ttu-id="76d58-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="76d58-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="76d58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76d58-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76d58-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76d58-105">DESCRIPTION</span></span>
<span data-ttu-id="76d58-106">Das **Cmdlet "Add-AzApiManagementApiToGateway"** fügt einem Gateway eine Azure API-Verwaltungs-API hinzu.</span><span class="sxs-lookup"><span data-stu-id="76d58-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="76d58-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76d58-107">EXAMPLES</span></span>

### <span data-ttu-id="76d58-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76d58-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="76d58-109">Mit diesem Befehl wird die angegebene API dem angegebenen Gateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="76d58-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="76d58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76d58-110">PARAMETERS</span></span>

### <span data-ttu-id="76d58-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76d58-111">-ApiId</span></span>
<span data-ttu-id="76d58-112">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="76d58-112">Identifier of existing API.</span></span>
<span data-ttu-id="76d58-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76d58-113">This parameter is required.</span></span>

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

### <span data-ttu-id="76d58-114">-Context</span><span class="sxs-lookup"><span data-stu-id="76d58-114">-Context</span></span>
<span data-ttu-id="76d58-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="76d58-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="76d58-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76d58-116">This parameter is required.</span></span>

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

### <span data-ttu-id="76d58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d58-117">-DefaultProfile</span></span>
<span data-ttu-id="76d58-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76d58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d58-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="76d58-119">-GatewayId</span></span>
<span data-ttu-id="76d58-120">ID eines vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="76d58-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="76d58-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76d58-121">This parameter is required.</span></span>

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

### <span data-ttu-id="76d58-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76d58-122">-PassThru</span></span>
<span data-ttu-id="76d58-123">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="76d58-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="76d58-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="76d58-124">This parameter is optional.</span></span>
<span data-ttu-id="76d58-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="76d58-125">Default value is false.</span></span>

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

### <span data-ttu-id="76d58-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="76d58-126">-ProvisioningState</span></span>
<span data-ttu-id="76d58-127">Bereitstellungszustand (Erstellt).</span><span class="sxs-lookup"><span data-stu-id="76d58-127">Provisioning State (Created).</span></span>
<span data-ttu-id="76d58-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="76d58-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="76d58-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76d58-129">-Confirm</span></span>
<span data-ttu-id="76d58-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76d58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d58-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76d58-131">-WhatIf</span></span>
<span data-ttu-id="76d58-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76d58-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76d58-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76d58-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d58-134">CommonParameters</span></span>
<span data-ttu-id="76d58-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d58-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76d58-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d58-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76d58-137">INPUTS</span></span>

### <span data-ttu-id="76d58-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76d58-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76d58-139">System.String</span><span class="sxs-lookup"><span data-stu-id="76d58-139">System.String</span></span>

### <span data-ttu-id="76d58-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="76d58-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="76d58-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76d58-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76d58-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76d58-142">OUTPUTS</span></span>

### <span data-ttu-id="76d58-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76d58-143">System.Boolean</span></span>

## <span data-ttu-id="76d58-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76d58-144">NOTES</span></span>

## <span data-ttu-id="76d58-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76d58-145">RELATED LINKS</span></span>

[<span data-ttu-id="76d58-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="76d58-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)
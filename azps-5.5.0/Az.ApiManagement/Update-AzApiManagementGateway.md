---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176172"
---
# <span data-ttu-id="7c411-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7c411-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="7c411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c411-102">SYNOPSIS</span></span>
<span data-ttu-id="7c411-103">Konfiguriert ein API-Verwaltungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7c411-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="7c411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c411-104">SYNTAX</span></span>

### <span data-ttu-id="7c411-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c411-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c411-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c411-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c411-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c411-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c411-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c411-108">DESCRIPTION</span></span>
<span data-ttu-id="7c411-109">Das **Cmdlet "Update-AzApiManagementGateway"** konfiguriert ein API-Verwaltungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7c411-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="7c411-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c411-110">EXAMPLES</span></span>

### <span data-ttu-id="7c411-111">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7c411-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="7c411-112">Mit diesem Befehl wird ein Gateway konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7c411-112">This command configures a gateway.</span></span>

## <span data-ttu-id="7c411-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c411-113">PARAMETERS</span></span>

### <span data-ttu-id="7c411-114">-Context</span><span class="sxs-lookup"><span data-stu-id="7c411-114">-Context</span></span>
<span data-ttu-id="7c411-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7c411-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7c411-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c411-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c411-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c411-117">-DefaultProfile</span></span>
<span data-ttu-id="7c411-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c411-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c411-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c411-119">-Description</span></span>
<span data-ttu-id="7c411-120">Gatewaybeschreibung.</span><span class="sxs-lookup"><span data-stu-id="7c411-120">Gateway description.</span></span>
<span data-ttu-id="7c411-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7c411-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="7c411-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7c411-122">-GatewayId</span></span>
<span data-ttu-id="7c411-123">ID eines vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="7c411-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="7c411-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c411-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c411-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c411-125">-InputObject</span></span>
<span data-ttu-id="7c411-126">Instanz von PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="7c411-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="7c411-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c411-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c411-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="7c411-128">-LocationData</span></span>
<span data-ttu-id="7c411-129">Gatewayspeicherort.</span><span class="sxs-lookup"><span data-stu-id="7c411-129">Gateway location.</span></span>
<span data-ttu-id="7c411-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7c411-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c411-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c411-131">-PassThru</span></span>
<span data-ttu-id="7c411-132">Wenn angegeben, dann Instanz des Typs "Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway", der das geänderte Gateway darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c411-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="7c411-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c411-133">-ResourceId</span></span>
<span data-ttu-id="7c411-134">Arm ResourceId des Gateways.</span><span class="sxs-lookup"><span data-stu-id="7c411-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="7c411-135">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c411-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c411-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c411-136">-Confirm</span></span>
<span data-ttu-id="7c411-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c411-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c411-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7c411-138">-WhatIf</span></span>
<span data-ttu-id="7c411-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c411-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c411-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c411-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c411-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c411-141">CommonParameters</span></span>
<span data-ttu-id="7c411-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c411-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c411-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c411-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c411-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c411-144">INPUTS</span></span>

### <span data-ttu-id="7c411-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7c411-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7c411-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7c411-146">System.String</span></span>

### <span data-ttu-id="7c411-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="7c411-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="7c411-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c411-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c411-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c411-149">OUTPUTS</span></span>

### <span data-ttu-id="7c411-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7c411-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="7c411-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c411-151">NOTES</span></span>

## <span data-ttu-id="7c411-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c411-152">RELATED LINKS</span></span>

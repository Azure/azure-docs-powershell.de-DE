---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361400"
---
# <span data-ttu-id="577ed-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="577ed-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="577ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577ed-102">SYNOPSIS</span></span>
<span data-ttu-id="577ed-103">Entfernt eine Hostnamenkonfiguration aus dem vorhandenen Gateway.</span><span class="sxs-lookup"><span data-stu-id="577ed-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="577ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="577ed-104">SYNTAX</span></span>

### <span data-ttu-id="577ed-105">ContextParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="577ed-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="577ed-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="577ed-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="577ed-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="577ed-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="577ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="577ed-108">DESCRIPTION</span></span>
<span data-ttu-id="577ed-109">Das **Cmdlet "Remove-AzApiManagementGatewayHostnameConfiguration"** entfernt eine Hostnamenkonfiguration aus dem vorhandenen Gateway.</span><span class="sxs-lookup"><span data-stu-id="577ed-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="577ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="577ed-110">EXAMPLES</span></span>

### <span data-ttu-id="577ed-111">Beispiel 1: Entfernen einer vorhandenen Konfiguration des Hostnamens eines Gateways</span><span class="sxs-lookup"><span data-stu-id="577ed-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="577ed-112">Dieser Befehl entfernt eine vorhandene Konfiguration des Hostnamens des Gateways und fordert den Benutzer nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="577ed-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="577ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577ed-113">PARAMETERS</span></span>

### <span data-ttu-id="577ed-114">-Context</span><span class="sxs-lookup"><span data-stu-id="577ed-114">-Context</span></span>
<span data-ttu-id="577ed-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="577ed-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="577ed-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="577ed-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577ed-117">-DefaultProfile</span></span>
<span data-ttu-id="577ed-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="577ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577ed-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="577ed-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="577ed-120">Bezeichner der vorhandenen Konfiguration des Gatewayhostnamens.</span><span class="sxs-lookup"><span data-stu-id="577ed-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="577ed-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="577ed-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ed-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="577ed-122">-GatewayId</span></span>
<span data-ttu-id="577ed-123">ID eines vorhandenen Gateways.</span><span class="sxs-lookup"><span data-stu-id="577ed-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="577ed-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="577ed-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ed-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="577ed-125">-InputObject</span></span>
<span data-ttu-id="577ed-126">Instanz von PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="577ed-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="577ed-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="577ed-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577ed-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="577ed-128">-PassThru</span></span>
<span data-ttu-id="577ed-129">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="577ed-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="577ed-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="577ed-130">This parameter is optional.</span></span>
<span data-ttu-id="577ed-131">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="577ed-131">Default value is false.</span></span>

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

### <span data-ttu-id="577ed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="577ed-132">-ResourceId</span></span>
<span data-ttu-id="577ed-133">Arm ResourceId der GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="577ed-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="577ed-134">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="577ed-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577ed-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577ed-135">-Confirm</span></span>
<span data-ttu-id="577ed-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="577ed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577ed-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="577ed-137">-WhatIf</span></span>
<span data-ttu-id="577ed-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="577ed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577ed-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="577ed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577ed-140">CommonParameters</span></span>
<span data-ttu-id="577ed-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577ed-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="577ed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577ed-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="577ed-143">INPUTS</span></span>

### <span data-ttu-id="577ed-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="577ed-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="577ed-145">System.String</span><span class="sxs-lookup"><span data-stu-id="577ed-145">System.String</span></span>

### <span data-ttu-id="577ed-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="577ed-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="577ed-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="577ed-147">OUTPUTS</span></span>

### <span data-ttu-id="577ed-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="577ed-148">System.Boolean</span></span>

## <span data-ttu-id="577ed-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="577ed-149">NOTES</span></span>

## <span data-ttu-id="577ed-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="577ed-150">RELATED LINKS</span></span>

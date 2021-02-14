---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176276"
---
# <span data-ttu-id="8bd9d-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="8bd9d-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="8bd9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd9d-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd9d-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="8bd9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bd9d-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd9d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bd9d-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd9d-106">Das **Cmdlet "Remove-AzApiManagementApiFromGateway"** fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="8bd9d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bd9d-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd9d-108">Beispiel 1: Entfernen einer API von einem Gateway</span><span class="sxs-lookup"><span data-stu-id="8bd9d-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="8bd9d-109">Mit diesem Befehl wird die angegebene API von einem Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="8bd9d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bd9d-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd9d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8bd9d-111">-ApiId</span></span>
<span data-ttu-id="8bd9d-112">Bezeichner vorhandener APIs, die aus dem Gateway entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="8bd9d-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8bd9d-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8bd9d-114">-Context</span></span>
<span data-ttu-id="8bd9d-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8bd9d-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8bd9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd9d-117">-DefaultProfile</span></span>
<span data-ttu-id="8bd9d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd9d-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8bd9d-119">-GatewayId</span></span>
<span data-ttu-id="8bd9d-120">Id des vorhandenen Gateways, aus dem die API entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="8bd9d-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="8bd9d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bd9d-122">-PassThru</span></span>
<span data-ttu-id="8bd9d-123">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8bd9d-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-124">This parameter is optional.</span></span>
<span data-ttu-id="8bd9d-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="8bd9d-125">Default value is false.</span></span>

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

### <span data-ttu-id="8bd9d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bd9d-126">-Confirm</span></span>
<span data-ttu-id="8bd9d-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd9d-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8bd9d-128">-WhatIf</span></span>
<span data-ttu-id="8bd9d-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bd9d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd9d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd9d-131">CommonParameters</span></span>
<span data-ttu-id="8bd9d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd9d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd9d-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bd9d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd9d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bd9d-134">INPUTS</span></span>

### <span data-ttu-id="8bd9d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8bd9d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8bd9d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8bd9d-136">System.String</span></span>

### <span data-ttu-id="8bd9d-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8bd9d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8bd9d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bd9d-138">OUTPUTS</span></span>

### <span data-ttu-id="8bd9d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd9d-139">System.Boolean</span></span>

## <span data-ttu-id="8bd9d-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8bd9d-140">NOTES</span></span>

## <span data-ttu-id="8bd9d-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8bd9d-141">RELATED LINKS</span></span>

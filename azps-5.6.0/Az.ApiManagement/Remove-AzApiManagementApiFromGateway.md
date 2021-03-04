---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922152"
---
# <span data-ttu-id="abbd2-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="abbd2-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="abbd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="abbd2-103">Fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="abbd2-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="abbd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abbd2-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abbd2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abbd2-105">DESCRIPTION</span></span>
<span data-ttu-id="abbd2-106">Das **Cmdlet Remove-AzApiManagementApiFromGateway** fügt eine API an ein Gateway an.</span><span class="sxs-lookup"><span data-stu-id="abbd2-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="abbd2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abbd2-107">EXAMPLES</span></span>

### <span data-ttu-id="abbd2-108">Beispiel 1: Entfernen einer API aus einem Gateway</span><span class="sxs-lookup"><span data-stu-id="abbd2-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="abbd2-109">Mit diesem Befehl wird die angegebene API aus einem Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="abbd2-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="abbd2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="abbd2-110">PARAMETERS</span></span>

### <span data-ttu-id="abbd2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="abbd2-111">-ApiId</span></span>
<span data-ttu-id="abbd2-112">Bezeichner vorhandener APIs, die aus dem Gateway entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="abbd2-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="abbd2-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abbd2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="abbd2-114">-Context</span><span class="sxs-lookup"><span data-stu-id="abbd2-114">-Context</span></span>
<span data-ttu-id="abbd2-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="abbd2-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="abbd2-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abbd2-116">This parameter is required.</span></span>

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

### <span data-ttu-id="abbd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbd2-117">-DefaultProfile</span></span>
<span data-ttu-id="abbd2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abbd2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abbd2-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="abbd2-119">-GatewayId</span></span>
<span data-ttu-id="abbd2-120">Bezeichner des vorhandenen Gateways zum Entfernen der API aus.</span><span class="sxs-lookup"><span data-stu-id="abbd2-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="abbd2-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abbd2-121">This parameter is required.</span></span>

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

### <span data-ttu-id="abbd2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abbd2-122">-PassThru</span></span>
<span data-ttu-id="abbd2-123">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="abbd2-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="abbd2-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="abbd2-124">This parameter is optional.</span></span>
<span data-ttu-id="abbd2-125">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="abbd2-125">Default value is false.</span></span>

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

### <span data-ttu-id="abbd2-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abbd2-126">-Confirm</span></span>
<span data-ttu-id="abbd2-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abbd2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbd2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbd2-128">-WhatIf</span></span>
<span data-ttu-id="abbd2-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abbd2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abbd2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abbd2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbd2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbd2-131">CommonParameters</span></span>
<span data-ttu-id="abbd2-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abbd2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbd2-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abbd2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbd2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abbd2-134">INPUTS</span></span>

### <span data-ttu-id="abbd2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="abbd2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="abbd2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="abbd2-136">System.String</span></span>

### <span data-ttu-id="abbd2-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="abbd2-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="abbd2-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abbd2-138">OUTPUTS</span></span>

### <span data-ttu-id="abbd2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abbd2-139">System.Boolean</span></span>

## <span data-ttu-id="abbd2-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="abbd2-140">NOTES</span></span>

## <span data-ttu-id="abbd2-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="abbd2-141">RELATED LINKS</span></span>

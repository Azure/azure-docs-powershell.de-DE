---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944320"
---
# <span data-ttu-id="17cbc-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17cbc-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="17cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="17cbc-103">Entfernt einen bestimmten Api-Versionssatz</span><span class="sxs-lookup"><span data-stu-id="17cbc-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="17cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17cbc-104">SYNTAX</span></span>

### <span data-ttu-id="17cbc-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="17cbc-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17cbc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17cbc-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17cbc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17cbc-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17cbc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17cbc-108">DESCRIPTION</span></span>

<span data-ttu-id="17cbc-109">Das **Cmdlet Remove-AzAzureRmApiManagementApiVersionSet** entfernt einen vorhandenen API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="17cbc-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="17cbc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="17cbc-111">Beispiel 1: Entfernen eines API-Versionssatzs</span><span class="sxs-lookup"><span data-stu-id="17cbc-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="17cbc-112">Mit diesem Befehl wird der API-Versionssatz mit der angegebenen ApiVersionSetId entfernt.</span><span class="sxs-lookup"><span data-stu-id="17cbc-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="17cbc-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17cbc-113">PARAMETERS</span></span>

### <span data-ttu-id="17cbc-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="17cbc-114">-ApiVersionSetId</span></span>
<span data-ttu-id="17cbc-115">Bezeichner des API-Versionssets.</span><span class="sxs-lookup"><span data-stu-id="17cbc-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="17cbc-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17cbc-116">This parameter is required.</span></span>

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

### <span data-ttu-id="17cbc-117">-Context</span><span class="sxs-lookup"><span data-stu-id="17cbc-117">-Context</span></span>
<span data-ttu-id="17cbc-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="17cbc-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17cbc-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17cbc-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17cbc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17cbc-120">-DefaultProfile</span></span>
<span data-ttu-id="17cbc-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17cbc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17cbc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17cbc-122">-InputObject</span></span>
<span data-ttu-id="17cbc-123">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="17cbc-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="17cbc-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17cbc-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17cbc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17cbc-125">-PassThru</span></span>
<span data-ttu-id="17cbc-126">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="17cbc-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="17cbc-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="17cbc-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="17cbc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17cbc-128">-ResourceId</span></span>
<span data-ttu-id="17cbc-129">Arm ResourceId von ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="17cbc-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="17cbc-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="17cbc-130">This parameter is required.</span></span>

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

### <span data-ttu-id="17cbc-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17cbc-131">-Confirm</span></span>
<span data-ttu-id="17cbc-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17cbc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17cbc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17cbc-133">-WhatIf</span></span>
<span data-ttu-id="17cbc-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17cbc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17cbc-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17cbc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17cbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17cbc-136">CommonParameters</span></span>
<span data-ttu-id="17cbc-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17cbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17cbc-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17cbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17cbc-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17cbc-139">INPUTS</span></span>

### <span data-ttu-id="17cbc-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17cbc-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17cbc-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17cbc-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="17cbc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="17cbc-142">System.String</span></span>

## <span data-ttu-id="17cbc-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17cbc-143">OUTPUTS</span></span>

### <span data-ttu-id="17cbc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17cbc-144">System.Boolean</span></span>

## <span data-ttu-id="17cbc-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17cbc-145">NOTES</span></span>

## <span data-ttu-id="17cbc-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17cbc-146">RELATED LINKS</span></span>

[<span data-ttu-id="17cbc-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17cbc-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="17cbc-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17cbc-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="17cbc-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="17cbc-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
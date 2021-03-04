---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 4f6f7f1cf2223d4ef139d60e710f4a861149a3ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949787"
---
# <span data-ttu-id="bc3ad-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc3ad-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="bc3ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3ad-103">Entfernen Sie die Diagnoseentität aus dem Bereich "Global" oder "API-Ebene".</span><span class="sxs-lookup"><span data-stu-id="bc3ad-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="bc3ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc3ad-104">SYNTAX</span></span>

### <span data-ttu-id="bc3ad-105">ByResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc3ad-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc3ad-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bc3ad-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc3ad-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc3ad-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc3ad-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc3ad-108">DESCRIPTION</span></span>
<span data-ttu-id="bc3ad-109">Das Cmdlet **Remove-AzApiManagementDiagnostic** entfernt die vom globalen Bereich oder einem Bereich `DiagnosticId` angegebene `ApiId` Diagnoseentität.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="bc3ad-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc3ad-110">EXAMPLES</span></span>

### <span data-ttu-id="bc3ad-111">Beispiel 1: Entfernen der Diagnoseentität</span><span class="sxs-lookup"><span data-stu-id="bc3ad-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="bc3ad-112">In diesem Beispiel wird die Diagnose `applicationinsights` aus dem Api-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="bc3ad-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bc3ad-113">PARAMETERS</span></span>

### <span data-ttu-id="bc3ad-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bc3ad-114">-ApiId</span></span>
<span data-ttu-id="bc3ad-115">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-115">Identifier of the API.</span></span>
<span data-ttu-id="bc3ad-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3ad-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bc3ad-117">-Context</span></span>
<span data-ttu-id="bc3ad-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bc3ad-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3ad-120">-DefaultProfile</span></span>
<span data-ttu-id="bc3ad-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc3ad-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="bc3ad-122">-DiagnosticId</span></span>
<span data-ttu-id="bc3ad-123">Bezeichner des vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-123">Identifier of existing product.</span></span>
<span data-ttu-id="bc3ad-124">Wenn angegeben wird, gibt die Richtlinie für den Produktbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="bc3ad-125">Diese Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3ad-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc3ad-126">-InputObject</span></span>
<span data-ttu-id="bc3ad-127">Instanz von PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="bc3ad-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3ad-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc3ad-129">-PassThru</span></span>
<span data-ttu-id="bc3ad-130">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="bc3ad-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc3ad-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc3ad-132">-ResourceId</span></span>
<span data-ttu-id="bc3ad-133">Arm ResourceId of Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="bc3ad-134">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-134">This parameter is required.</span></span>

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

### <span data-ttu-id="bc3ad-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc3ad-135">-Confirm</span></span>
<span data-ttu-id="bc3ad-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc3ad-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc3ad-137">-WhatIf</span></span>
<span data-ttu-id="bc3ad-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc3ad-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc3ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3ad-140">CommonParameters</span></span>
<span data-ttu-id="bc3ad-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3ad-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc3ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3ad-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc3ad-143">INPUTS</span></span>

### <span data-ttu-id="bc3ad-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc3ad-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc3ad-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bc3ad-145">System.String</span></span>

### <span data-ttu-id="bc3ad-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc3ad-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc3ad-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc3ad-147">OUTPUTS</span></span>

### <span data-ttu-id="bc3ad-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc3ad-148">System.Boolean</span></span>

## <span data-ttu-id="bc3ad-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bc3ad-149">NOTES</span></span>

## <span data-ttu-id="bc3ad-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bc3ad-150">RELATED LINKS</span></span>

[<span data-ttu-id="bc3ad-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc3ad-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="bc3ad-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc3ad-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="bc3ad-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc3ad-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)
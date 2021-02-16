---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145284"
---
# <span data-ttu-id="bf698-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf698-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="bf698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf698-102">SYNOPSIS</span></span>
<span data-ttu-id="bf698-103">Entfernen Sie die Diagnoseentität aus dem Bereich auf globaler oder API-Ebene.</span><span class="sxs-lookup"><span data-stu-id="bf698-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="bf698-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf698-104">SYNTAX</span></span>

### <span data-ttu-id="bf698-105">ByResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf698-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf698-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bf698-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf698-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf698-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf698-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf698-108">DESCRIPTION</span></span>
<span data-ttu-id="bf698-109">Das Cmdlet **"Remove-AzApiManagementDiagnostic"** entfernt die Diagnoseentität, die durch den globalen Bereich oder einen `DiagnosticId` Bereich angegeben `ApiId` wurde.</span><span class="sxs-lookup"><span data-stu-id="bf698-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="bf698-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf698-110">EXAMPLES</span></span>

### <span data-ttu-id="bf698-111">Beispiel 1: Entfernen der Diagnoseentität</span><span class="sxs-lookup"><span data-stu-id="bf698-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="bf698-112">In diesem Beispiel wird die Diagnose `applicationinsights` aus dem Api-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="bf698-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="bf698-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf698-113">PARAMETERS</span></span>

### <span data-ttu-id="bf698-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bf698-114">-ApiId</span></span>
<span data-ttu-id="bf698-115">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="bf698-115">Identifier of the API.</span></span>
<span data-ttu-id="bf698-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf698-116">This parameter is required.</span></span>

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

### <span data-ttu-id="bf698-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bf698-117">-Context</span></span>
<span data-ttu-id="bf698-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bf698-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bf698-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf698-119">This parameter is required.</span></span>

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

### <span data-ttu-id="bf698-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf698-120">-DefaultProfile</span></span>
<span data-ttu-id="bf698-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf698-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf698-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="bf698-122">-DiagnosticId</span></span>
<span data-ttu-id="bf698-123">Id eines vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="bf698-123">Identifier of existing product.</span></span>
<span data-ttu-id="bf698-124">Wenn diese Angabe angegeben wird, wird eine Richtlinie für den Produktbereich zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bf698-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="bf698-125">Diese Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="bf698-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="bf698-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf698-126">-InputObject</span></span>
<span data-ttu-id="bf698-127">Instanz von PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="bf698-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="bf698-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf698-128">This parameter is required.</span></span>

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

### <span data-ttu-id="bf698-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf698-129">-PassThru</span></span>
<span data-ttu-id="bf698-130">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bf698-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="bf698-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bf698-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="bf698-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf698-132">-ResourceId</span></span>
<span data-ttu-id="bf698-133">Arm ResourceId of Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bf698-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="bf698-134">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf698-134">This parameter is required.</span></span>

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

### <span data-ttu-id="bf698-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf698-135">-Confirm</span></span>
<span data-ttu-id="bf698-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf698-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf698-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bf698-137">-WhatIf</span></span>
<span data-ttu-id="bf698-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf698-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf698-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf698-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf698-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf698-140">CommonParameters</span></span>
<span data-ttu-id="bf698-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf698-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf698-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf698-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf698-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf698-143">INPUTS</span></span>

### <span data-ttu-id="bf698-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bf698-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bf698-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bf698-145">System.String</span></span>

### <span data-ttu-id="bf698-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bf698-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bf698-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf698-147">OUTPUTS</span></span>

### <span data-ttu-id="bf698-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf698-148">System.Boolean</span></span>

## <span data-ttu-id="bf698-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf698-149">NOTES</span></span>

## <span data-ttu-id="bf698-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf698-150">RELATED LINKS</span></span>

[<span data-ttu-id="bf698-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf698-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="bf698-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf698-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="bf698-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf698-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)
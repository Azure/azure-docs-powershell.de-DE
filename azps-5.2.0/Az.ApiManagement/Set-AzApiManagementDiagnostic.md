---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365810"
---
# <span data-ttu-id="869e1-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="869e1-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="869e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="869e1-102">SYNOPSIS</span></span>
<span data-ttu-id="869e1-103">Ändert eine API-Verwaltungsdiagnose im globalen Bereich oder api-Bereich.</span><span class="sxs-lookup"><span data-stu-id="869e1-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="869e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="869e1-104">SYNTAX</span></span>

### <span data-ttu-id="869e1-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="869e1-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="869e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="869e1-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="869e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="869e1-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869e1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="869e1-108">DESCRIPTION</span></span>
<span data-ttu-id="869e1-109">Das Cmdlet **"Set-AzApiManagementDiagnostic"** aktualisiert die Diagnose, die im globalen Bereich oder im Api-Bereich konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="869e1-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="869e1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="869e1-110">EXAMPLES</span></span>

### <span data-ttu-id="869e1-111">Beispiel 1: Ändern einer Diagnose im globalen Bereich</span><span class="sxs-lookup"><span data-stu-id="869e1-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="869e1-112">Dieser Befehl ändert den angegebenen Prozentsatz der Diagnoses sampling von 100 bis 50 %.</span><span class="sxs-lookup"><span data-stu-id="869e1-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="869e1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="869e1-113">Example 2</span></span>

<span data-ttu-id="869e1-114">Ändert eine API-Verwaltungsdiagnose im globalen Bereich oder api-Bereich.</span><span class="sxs-lookup"><span data-stu-id="869e1-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="869e1-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="869e1-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="869e1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="869e1-116">PARAMETERS</span></span>

### <span data-ttu-id="869e1-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="869e1-117">-AlwaysLog</span></span>
<span data-ttu-id="869e1-118">Gibt an, welche Art von Nachrichtens sampling-Einstellungen nicht angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="869e1-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="869e1-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="869e1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="869e1-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="869e1-120">-ApiId</span></span>
<span data-ttu-id="869e1-121">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="869e1-121">Identifier of existing API.</span></span>
<span data-ttu-id="869e1-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="869e1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869e1-123">-Back-EndSetting</span><span class="sxs-lookup"><span data-stu-id="869e1-123">-BackendSetting</span></span>
<span data-ttu-id="869e1-124">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="869e1-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="869e1-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="869e1-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869e1-126">-Context</span><span class="sxs-lookup"><span data-stu-id="869e1-126">-Context</span></span>
<span data-ttu-id="869e1-127">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="869e1-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="869e1-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869e1-128">This parameter is required.</span></span>

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

### <span data-ttu-id="869e1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869e1-129">-DefaultProfile</span></span>
<span data-ttu-id="869e1-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="869e1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="869e1-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="869e1-131">-DiagnosticId</span></span>
<span data-ttu-id="869e1-132">Bezeichner eines vorhandenen Diagnosetools.</span><span class="sxs-lookup"><span data-stu-id="869e1-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="869e1-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869e1-133">This parameter is required.</span></span>

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

### <span data-ttu-id="869e1-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="869e1-134">-FrontEndSetting</span></span>
<span data-ttu-id="869e1-135">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="869e1-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="869e1-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="869e1-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869e1-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="869e1-137">-InputObject</span></span>
<span data-ttu-id="869e1-138">Instanz von PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="869e1-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="869e1-139">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869e1-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="869e1-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="869e1-140">-LoggerId</span></span>
<span data-ttu-id="869e1-141">Bezeichner des Loggers, an den die Diagnose pusht werden soll.</span><span class="sxs-lookup"><span data-stu-id="869e1-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="869e1-142">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869e1-142">This parameter is required.</span></span>

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

### <span data-ttu-id="869e1-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="869e1-143">-PassThru</span></span>
<span data-ttu-id="869e1-144">Wenn angegeben, dann Instanz des Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic-Typs, der den festgelegten Diagnosetyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="869e1-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="869e1-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="869e1-145">-ResourceId</span></span>
<span data-ttu-id="869e1-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="869e1-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="869e1-147">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="869e1-147">This parameter is required.</span></span>

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

### <span data-ttu-id="869e1-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="869e1-148">-SamplingSetting</span></span>
<span data-ttu-id="869e1-149">Samplingeinstellung der Diagnose.</span><span class="sxs-lookup"><span data-stu-id="869e1-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="869e1-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="869e1-150">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869e1-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="869e1-151">-Confirm</span></span>
<span data-ttu-id="869e1-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="869e1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="869e1-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="869e1-153">-WhatIf</span></span>
<span data-ttu-id="869e1-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="869e1-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="869e1-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="869e1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="869e1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869e1-156">CommonParameters</span></span>
<span data-ttu-id="869e1-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869e1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869e1-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="869e1-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869e1-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="869e1-159">INPUTS</span></span>

### <span data-ttu-id="869e1-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="869e1-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="869e1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="869e1-161">System.String</span></span>

### <span data-ttu-id="869e1-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="869e1-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="869e1-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="869e1-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="869e1-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="869e1-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="869e1-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="869e1-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="869e1-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="869e1-166">OUTPUTS</span></span>

### <span data-ttu-id="869e1-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="869e1-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="869e1-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="869e1-168">NOTES</span></span>

## <span data-ttu-id="869e1-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="869e1-169">RELATED LINKS</span></span>

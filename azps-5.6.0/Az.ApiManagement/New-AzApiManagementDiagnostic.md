---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937203"
---
# <span data-ttu-id="d9c7f-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="d9c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c7f-103">Erstellt eine neue Diagnose im Bereich "Global" oder "Api Scope".</span><span class="sxs-lookup"><span data-stu-id="d9c7f-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="d9c7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9c7f-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c7f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9c7f-106">Das Cmdlet **New-AzApiManagementDiagnostic** erstellt eine Diagnoseentität entweder im globalen Bereich oder im bestimmten Api-Bereich.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="d9c7f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9c7f-107">EXAMPLES</span></span>

### <span data-ttu-id="d9c7f-108">Beispiel 1: Erstellen eines neuen globalen Bereichs Diagnose</span><span class="sxs-lookup"><span data-stu-id="d9c7f-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="d9c7f-109">In diesem Beispiel wird eine Diagnoseentität im globalen Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="d9c7f-110">Beispiel 2: Erstellen einer Diagnose im Api-Bereich</span><span class="sxs-lookup"><span data-stu-id="d9c7f-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="d9c7f-111">Im obigen Beispiel wird eine Diagnose für die API erstellt, um die Kopfzeile und 100 Byte textkörper für `httpbin` den `azuremonitor` Logger zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="d9c7f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9c7f-112">PARAMETERS</span></span>

### <span data-ttu-id="d9c7f-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="d9c7f-113">-AlwaysLog</span></span>
<span data-ttu-id="d9c7f-114">Gibt an, welcher Nachrichtentyp nicht angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="d9c7f-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9c7f-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d9c7f-116">-ApiId</span></span>
<span data-ttu-id="d9c7f-117">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-117">Identifier of existing API.</span></span>
<span data-ttu-id="d9c7f-118">Wenn angegeben wird, wird die API-Scope-Richtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="d9c7f-119">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-119">This parameters is required.</span></span>

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

### <span data-ttu-id="d9c7f-120">-Back-EndSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-120">-BackendSetting</span></span>
<span data-ttu-id="d9c7f-121">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten im Back-End.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="d9c7f-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9c7f-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d9c7f-123">-Context</span></span>
<span data-ttu-id="d9c7f-124">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d9c7f-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c7f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c7f-126">-DefaultProfile</span></span>
<span data-ttu-id="d9c7f-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c7f-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="d9c7f-128">-DiagnosticId</span></span>
<span data-ttu-id="d9c7f-129">Bezeichner der Diagnoseentität.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="d9c7f-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9c7f-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-131">-FrontEndSetting</span></span>
<span data-ttu-id="d9c7f-132">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="d9c7f-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9c7f-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d9c7f-134">-LoggerId</span></span>
<span data-ttu-id="d9c7f-135">Bezeichner des Loggers, an den die Diagnose weitergeschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="d9c7f-136">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-136">This parameter is required.</span></span>

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

### <span data-ttu-id="d9c7f-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-137">-SamplingSetting</span></span>
<span data-ttu-id="d9c7f-138">Samplingeinstellung der Diagnose.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="d9c7f-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9c7f-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9c7f-140">-Confirm</span></span>
<span data-ttu-id="d9c7f-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c7f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c7f-142">-WhatIf</span></span>
<span data-ttu-id="d9c7f-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c7f-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c7f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c7f-145">CommonParameters</span></span>
<span data-ttu-id="d9c7f-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c7f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c7f-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9c7f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c7f-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c7f-148">INPUTS</span></span>

### <span data-ttu-id="d9c7f-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9c7f-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9c7f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c7f-150">System.String</span></span>

### <span data-ttu-id="d9c7f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="d9c7f-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d9c7f-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9c7f-153">OUTPUTS</span></span>

### <span data-ttu-id="d9c7f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="d9c7f-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9c7f-155">NOTES</span></span>

## <span data-ttu-id="d9c7f-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9c7f-156">RELATED LINKS</span></span>

[<span data-ttu-id="d9c7f-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d9c7f-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d9c7f-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d9c7f-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d9c7f-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="d9c7f-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d9c7f-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
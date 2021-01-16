---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293926"
---
# <span data-ttu-id="01eb9-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="01eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="01eb9-103">Erstellt ein neues Diagnosetool für den globalen Bereich oder api-Bereich.</span><span class="sxs-lookup"><span data-stu-id="01eb9-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="01eb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01eb9-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01eb9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="01eb9-106">Das Cmdlet **"New-AzApiManagementDiagnostic"** erstellt eine Diagnoseentität entweder im globalen Bereich oder im spezifischen API-Bereich.</span><span class="sxs-lookup"><span data-stu-id="01eb9-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="01eb9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="01eb9-108">Beispiel 1: Erstellen einer neuen Diagnose für globalen Bereich</span><span class="sxs-lookup"><span data-stu-id="01eb9-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="01eb9-109">In diesem Beispiel wird eine Diagnoseentität im globalen Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="01eb9-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="01eb9-110">Beispiel 2: Erstellen eines Diagnosetool für den Api-Bereich</span><span class="sxs-lookup"><span data-stu-id="01eb9-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="01eb9-111">Im vorstehenden Beispiel wird ein Diagnosetool für die API erstellt, um die Header- und `httpbin` 100 Bytes des Textkörpers für die `azuremonitor` Protokollierung zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="01eb9-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="01eb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01eb9-112">PARAMETERS</span></span>

### <span data-ttu-id="01eb9-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="01eb9-113">-AlwaysLog</span></span>
<span data-ttu-id="01eb9-114">Gibt an, welche Art von Nachrichtens sampling-Einstellungen nicht angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01eb9-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="01eb9-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="01eb9-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="01eb9-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="01eb9-116">-ApiId</span></span>
<span data-ttu-id="01eb9-117">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="01eb9-117">Identifier of existing API.</span></span>
<span data-ttu-id="01eb9-118">Wenn angegeben, wird die RICHTLINIE für den API-Bereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01eb9-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="01eb9-119">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01eb9-119">This parameters is required.</span></span>

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

### <span data-ttu-id="01eb9-120">-Back-EndSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-120">-BackendSetting</span></span>
<span data-ttu-id="01eb9-121">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="01eb9-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="01eb9-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="01eb9-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="01eb9-123">-Context</span><span class="sxs-lookup"><span data-stu-id="01eb9-123">-Context</span></span>
<span data-ttu-id="01eb9-124">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="01eb9-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="01eb9-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01eb9-125">This parameter is required.</span></span>

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

### <span data-ttu-id="01eb9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01eb9-126">-DefaultProfile</span></span>
<span data-ttu-id="01eb9-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01eb9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01eb9-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="01eb9-128">-DiagnosticId</span></span>
<span data-ttu-id="01eb9-129">Bezeichner der Diagnoseentität.</span><span class="sxs-lookup"><span data-stu-id="01eb9-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="01eb9-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="01eb9-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="01eb9-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-131">-FrontEndSetting</span></span>
<span data-ttu-id="01eb9-132">Diagnoseeinstellung für eingehende/ausgehende Http-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="01eb9-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="01eb9-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="01eb9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="01eb9-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="01eb9-134">-LoggerId</span></span>
<span data-ttu-id="01eb9-135">Bezeichner des Loggers, an den die Diagnose pusht werden soll.</span><span class="sxs-lookup"><span data-stu-id="01eb9-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="01eb9-136">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="01eb9-136">This parameter is required.</span></span>

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

### <span data-ttu-id="01eb9-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-137">-SamplingSetting</span></span>
<span data-ttu-id="01eb9-138">Samplingeinstellung der Diagnose.</span><span class="sxs-lookup"><span data-stu-id="01eb9-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="01eb9-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="01eb9-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="01eb9-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01eb9-140">-Confirm</span></span>
<span data-ttu-id="01eb9-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01eb9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01eb9-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01eb9-142">-WhatIf</span></span>
<span data-ttu-id="01eb9-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01eb9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01eb9-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01eb9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01eb9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01eb9-145">CommonParameters</span></span>
<span data-ttu-id="01eb9-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01eb9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01eb9-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01eb9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01eb9-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01eb9-148">INPUTS</span></span>

### <span data-ttu-id="01eb9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01eb9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01eb9-150">System.String</span><span class="sxs-lookup"><span data-stu-id="01eb9-150">System.String</span></span>

### <span data-ttu-id="01eb9-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="01eb9-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="01eb9-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01eb9-153">OUTPUTS</span></span>

### <span data-ttu-id="01eb9-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="01eb9-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01eb9-155">NOTES</span></span>

## <span data-ttu-id="01eb9-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01eb9-156">RELATED LINKS</span></span>

[<span data-ttu-id="01eb9-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="01eb9-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="01eb9-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="01eb9-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01eb9-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="01eb9-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="01eb9-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
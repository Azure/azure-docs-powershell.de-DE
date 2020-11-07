---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658147"
---
# <span data-ttu-id="5cffe-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5cffe-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="5cffe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cffe-102">SYNOPSIS</span></span>
<span data-ttu-id="5cffe-103">Ändert eine API-Verwaltungs Diagnose im globalen oder API-Bereich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="5cffe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cffe-104">SYNTAX</span></span>

### <span data-ttu-id="5cffe-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cffe-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cffe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5cffe-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cffe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cffe-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cffe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cffe-108">DESCRIPTION</span></span>
<span data-ttu-id="5cffe-109">Das Cmdlet **Satz-AzApiManagementDiagnostic** aktualisiert die Diagnose, die im globalen oder API-Bereich konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="5cffe-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="5cffe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cffe-110">EXAMPLES</span></span>

### <span data-ttu-id="5cffe-111">Beispiel 1: Ändern einer Diagnose im globalen Bereich</span><span class="sxs-lookup"><span data-stu-id="5cffe-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="5cffe-112">Mit diesem Befehl wird der angegebene diagnostische Sampling-Prozentsatz von 100 auf 50% geändert.</span><span class="sxs-lookup"><span data-stu-id="5cffe-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="5cffe-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cffe-113">PARAMETERS</span></span>

### <span data-ttu-id="5cffe-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="5cffe-114">-AlwaysLog</span></span>
<span data-ttu-id="5cffe-115">Gibt an, für welche Art von Nachrichten samplingeinstellungen nicht gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="5cffe-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="5cffe-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5cffe-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cffe-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5cffe-117">-ApiId</span></span>
<span data-ttu-id="5cffe-118">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="5cffe-118">Identifier of existing API.</span></span>
<span data-ttu-id="5cffe-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5cffe-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cffe-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="5cffe-120">-BackendSetting</span></span>
<span data-ttu-id="5cffe-121">Diagnose Einstellung für eingehende/ausgehende HTTP-Nachrichten an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="5cffe-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="5cffe-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5cffe-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cffe-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5cffe-123">-Context</span></span>
<span data-ttu-id="5cffe-124">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5cffe-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5cffe-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5cffe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cffe-126">-DefaultProfile</span></span>
<span data-ttu-id="5cffe-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cffe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cffe-128">-Diagnose-Nr</span><span class="sxs-lookup"><span data-stu-id="5cffe-128">-DiagnosticId</span></span>
<span data-ttu-id="5cffe-129">Bezeichner der vorhandenen Diagnose.</span><span class="sxs-lookup"><span data-stu-id="5cffe-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="5cffe-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-130">This parameter is required.</span></span>

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

### <span data-ttu-id="5cffe-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="5cffe-131">-FrontEndSetting</span></span>
<span data-ttu-id="5cffe-132">Diagnose Einstellung für eingehende/ausgehende HTTP-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="5cffe-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="5cffe-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5cffe-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cffe-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5cffe-134">-InputObject</span></span>
<span data-ttu-id="5cffe-135">Instanz von PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="5cffe-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="5cffe-136">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-136">This parameter is required.</span></span>

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

### <span data-ttu-id="5cffe-137">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="5cffe-137">-LoggerId</span></span>
<span data-ttu-id="5cffe-138">Bezeichner der Protokollierung, an die die Diagnose weiter gepusht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cffe-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="5cffe-139">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-139">This parameter is required.</span></span>

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

### <span data-ttu-id="5cffe-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cffe-140">-PassThru</span></span>
<span data-ttu-id="5cffe-141">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementDiagnostic-Typs für die festgelegte Diagnose angegeben.</span><span class="sxs-lookup"><span data-stu-id="5cffe-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="5cffe-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5cffe-142">-ResourceId</span></span>
<span data-ttu-id="5cffe-143">Arm-findige Diagnose-oder API-Diagnose.</span><span class="sxs-lookup"><span data-stu-id="5cffe-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="5cffe-144">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cffe-144">This parameter is required.</span></span>

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

### <span data-ttu-id="5cffe-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5cffe-145">-SamplingSetting</span></span>
<span data-ttu-id="5cffe-146">Sampling-Einstellung der Diagnose.</span><span class="sxs-lookup"><span data-stu-id="5cffe-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="5cffe-147">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5cffe-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="5cffe-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cffe-148">-Confirm</span></span>
<span data-ttu-id="5cffe-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cffe-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cffe-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cffe-150">-WhatIf</span></span>
<span data-ttu-id="5cffe-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cffe-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cffe-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cffe-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cffe-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cffe-153">CommonParameters</span></span>
<span data-ttu-id="5cffe-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cffe-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cffe-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cffe-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cffe-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cffe-156">INPUTS</span></span>

### <span data-ttu-id="5cffe-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5cffe-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5cffe-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5cffe-158">System.String</span></span>

### <span data-ttu-id="5cffe-159">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5cffe-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="5cffe-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5cffe-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="5cffe-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5cffe-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="5cffe-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5cffe-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5cffe-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cffe-163">OUTPUTS</span></span>

### <span data-ttu-id="5cffe-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5cffe-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="5cffe-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cffe-165">NOTES</span></span>

## <span data-ttu-id="5cffe-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cffe-166">RELATED LINKS</span></span>

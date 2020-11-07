---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 430264a27cfff11416b322285a0db05b230b3bbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658191"
---
# <span data-ttu-id="c5cf2-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5cf2-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="c5cf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5cf2-103">Entfernen Sie die diagnostische Entität aus dem globalen oder API-Level-Bereich.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="c5cf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5cf2-104">SYNTAX</span></span>

### <span data-ttu-id="c5cf2-105">ByResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5cf2-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5cf2-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c5cf2-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5cf2-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5cf2-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5cf2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5cf2-108">DESCRIPTION</span></span>
<span data-ttu-id="c5cf2-109">Das Cmdlet **Remove-AzApiManagementDiagnostic** entfernt die diagnostische Entität, die vom `DiagnosticId` globalen Bereich oder einem Bereich angegeben wird. `ApiId`</span><span class="sxs-lookup"><span data-stu-id="c5cf2-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="c5cf2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5cf2-110">EXAMPLES</span></span>

### <span data-ttu-id="c5cf2-111">Beispiel 1: Entfernen der Diagnose Entität</span><span class="sxs-lookup"><span data-stu-id="c5cf2-111">Example 1 : Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="c5cf2-112">In diesem Beispiel wird die Diagnose des `applicationinsights` API-Verwaltungsdiensts entfernt.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="c5cf2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5cf2-113">PARAMETERS</span></span>

### <span data-ttu-id="c5cf2-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c5cf2-114">-ApiId</span></span>
<span data-ttu-id="c5cf2-115">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-115">Identifier of the API.</span></span>
<span data-ttu-id="c5cf2-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c5cf2-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c5cf2-117">-Context</span></span>
<span data-ttu-id="c5cf2-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c5cf2-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c5cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="c5cf2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5cf2-122">-Diagnose-Nr</span><span class="sxs-lookup"><span data-stu-id="c5cf2-122">-DiagnosticId</span></span>
<span data-ttu-id="c5cf2-123">Bezeichner des vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-123">Identifier of existing product.</span></span>
<span data-ttu-id="c5cf2-124">Wenn angegeben, wird die Richtlinie für den Produktbereich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="c5cf2-125">Diese Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="c5cf2-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5cf2-126">-InputObject</span></span>
<span data-ttu-id="c5cf2-127">Instanz von PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="c5cf2-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-128">This parameter is required.</span></span>

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

### <span data-ttu-id="c5cf2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5cf2-129">-PassThru</span></span>
<span data-ttu-id="c5cf2-130">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c5cf2-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="c5cf2-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5cf2-132">-ResourceId</span></span>
<span data-ttu-id="c5cf2-133">Arm-Resourcen-Diagnose.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="c5cf2-134">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-134">This parameter is required.</span></span>

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

### <span data-ttu-id="c5cf2-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5cf2-135">-Confirm</span></span>
<span data-ttu-id="c5cf2-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5cf2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5cf2-137">-WhatIf</span></span>
<span data-ttu-id="c5cf2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5cf2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5cf2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5cf2-140">CommonParameters</span></span>
<span data-ttu-id="c5cf2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5cf2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5cf2-142">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5cf2-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5cf2-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5cf2-143">INPUTS</span></span>

### <span data-ttu-id="c5cf2-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c5cf2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c5cf2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c5cf2-145">System.String</span></span>

### <span data-ttu-id="c5cf2-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c5cf2-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5cf2-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5cf2-147">OUTPUTS</span></span>

### <span data-ttu-id="c5cf2-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5cf2-148">System.Boolean</span></span>

## <span data-ttu-id="c5cf2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5cf2-149">NOTES</span></span>

## <span data-ttu-id="c5cf2-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5cf2-150">RELATED LINKS</span></span>

[<span data-ttu-id="c5cf2-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5cf2-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c5cf2-152">Neu – AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5cf2-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c5cf2-153">Satz-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c5cf2-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)
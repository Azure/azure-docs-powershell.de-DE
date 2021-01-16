---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381588"
---
# <span data-ttu-id="c0c76-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c0c76-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c0c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c76-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c76-103">Aktualisiert eine bestimmte API-Version.</span><span class="sxs-lookup"><span data-stu-id="c0c76-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="c0c76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0c76-104">SYNTAX</span></span>

### <span data-ttu-id="c0c76-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0c76-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0c76-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c76-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0c76-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c76-108">Das **Cmdlet "Update-AzApiManagementApiRelease"** ändert eine Azure API Management API Release.</span><span class="sxs-lookup"><span data-stu-id="c0c76-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="c0c76-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0c76-109">EXAMPLES</span></span>

### <span data-ttu-id="c0c76-110">Beispiel 1: Aktualisiert eine API-Version für eine API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="c0c76-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="c0c76-111">Mit diesem Befehl wird `echo-api-release` die API-Version der API `echo-api` mit einer neuen Notiz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c0c76-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="c0c76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c76-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c76-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c0c76-113">-ApiId</span></span>
<span data-ttu-id="c0c76-114">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="c0c76-114">Identifier of existing API.</span></span>
<span data-ttu-id="c0c76-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0c76-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c0c76-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c0c76-116">-Context</span></span>
<span data-ttu-id="c0c76-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c0c76-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c0c76-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0c76-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c0c76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c76-119">-DefaultProfile</span></span>
<span data-ttu-id="c0c76-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0c76-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c76-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0c76-121">-InputObject</span></span>
<span data-ttu-id="c0c76-122">Instanz des Typs "Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease".</span><span class="sxs-lookup"><span data-stu-id="c0c76-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c76-123">-Note</span><span class="sxs-lookup"><span data-stu-id="c0c76-123">-Note</span></span>
<span data-ttu-id="c0c76-124">Api-Versionshinweise.</span><span class="sxs-lookup"><span data-stu-id="c0c76-124">Api Release Notes.</span></span>
<span data-ttu-id="c0c76-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c0c76-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0c76-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0c76-126">-PassThru</span></span>
<span data-ttu-id="c0c76-127">Wenn angegeben, dann Instanz von Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease-Typ, der den festgelegten API Release darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0c76-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="c0c76-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c0c76-128">-ReleaseId</span></span>
<span data-ttu-id="c0c76-129">Bezeichner für die Api Revision ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="c0c76-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="c0c76-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0c76-130">This parameter is required.</span></span>

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

### <span data-ttu-id="c0c76-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c76-131">-Confirm</span></span>
<span data-ttu-id="c0c76-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0c76-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c76-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0c76-133">-WhatIf</span></span>
<span data-ttu-id="c0c76-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0c76-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c76-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c76-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c76-136">CommonParameters</span></span>
<span data-ttu-id="c0c76-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c76-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0c76-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c76-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0c76-139">INPUTS</span></span>

### <span data-ttu-id="c0c76-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0c76-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0c76-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0c76-141">System.String</span></span>

### <span data-ttu-id="c0c76-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c0c76-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c0c76-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0c76-143">OUTPUTS</span></span>

### <span data-ttu-id="c0c76-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c0c76-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c0c76-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0c76-145">NOTES</span></span>

## <span data-ttu-id="c0c76-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0c76-146">RELATED LINKS</span></span>

[<span data-ttu-id="c0c76-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c0c76-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c0c76-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c0c76-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004368"
---
# <span data-ttu-id="c7699-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c7699-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c7699-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7699-102">SYNOPSIS</span></span>
<span data-ttu-id="c7699-103">Aktualisiert eine bestimmte API-Version.</span><span class="sxs-lookup"><span data-stu-id="c7699-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="c7699-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7699-104">SYNTAX</span></span>

### <span data-ttu-id="c7699-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7699-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7699-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7699-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7699-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7699-107">DESCRIPTION</span></span>
<span data-ttu-id="c7699-108">Das Cmdlet **Update-AzApiManagementApiRelease** ändert eine Azure API Management-API-Version.</span><span class="sxs-lookup"><span data-stu-id="c7699-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="c7699-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7699-109">EXAMPLES</span></span>

### <span data-ttu-id="c7699-110">Beispiel 1: aktualisiert eine API-Version für eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="c7699-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="c7699-111">Mit diesem Befehl wird die `echo-api-release` API-Version der API `echo-api` mit neuer Notiz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c7699-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="c7699-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7699-112">PARAMETERS</span></span>

### <span data-ttu-id="c7699-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c7699-113">-ApiId</span></span>
<span data-ttu-id="c7699-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="c7699-114">Identifier of existing API.</span></span>
<span data-ttu-id="c7699-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7699-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c7699-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c7699-116">-Context</span></span>
<span data-ttu-id="c7699-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c7699-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c7699-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7699-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c7699-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7699-119">-DefaultProfile</span></span>
<span data-ttu-id="c7699-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7699-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7699-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7699-121">-InputObject</span></span>
<span data-ttu-id="c7699-122">Instanz des Typs Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="c7699-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="c7699-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="c7699-123">-Note</span></span>
<span data-ttu-id="c7699-124">Anmerkungen zur API-Version.</span><span class="sxs-lookup"><span data-stu-id="c7699-124">Api Release Notes.</span></span>
<span data-ttu-id="c7699-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c7699-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7699-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7699-126">-PassThru</span></span>
<span data-ttu-id="c7699-127">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease-Typs, die die Version der festgelegten API darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7699-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="c7699-128">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="c7699-128">-ReleaseId</span></span>
<span data-ttu-id="c7699-129">Bezeichner für die Versionskennung der API-Version.</span><span class="sxs-lookup"><span data-stu-id="c7699-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="c7699-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7699-130">This parameter is required.</span></span>

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

### <span data-ttu-id="c7699-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7699-131">-Confirm</span></span>
<span data-ttu-id="c7699-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7699-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7699-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7699-133">-WhatIf</span></span>
<span data-ttu-id="c7699-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7699-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7699-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7699-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7699-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7699-136">CommonParameters</span></span>
<span data-ttu-id="c7699-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7699-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7699-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7699-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7699-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7699-139">INPUTS</span></span>

### <span data-ttu-id="c7699-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7699-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7699-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c7699-141">System.String</span></span>

### <span data-ttu-id="c7699-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c7699-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c7699-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7699-143">OUTPUTS</span></span>

### <span data-ttu-id="c7699-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c7699-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c7699-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7699-145">NOTES</span></span>

## <span data-ttu-id="c7699-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7699-146">RELATED LINKS</span></span>

[<span data-ttu-id="c7699-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c7699-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c7699-148">Neu – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c7699-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

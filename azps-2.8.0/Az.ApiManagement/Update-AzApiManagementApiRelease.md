---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 1141d671db13c3ea44a7ed7bd003574f3c13615c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658124"
---
# <span data-ttu-id="00fdf-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00fdf-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="00fdf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="00fdf-103">Aktualisiert eine bestimmte API-Version.</span><span class="sxs-lookup"><span data-stu-id="00fdf-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="00fdf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00fdf-104">SYNTAX</span></span>

### <span data-ttu-id="00fdf-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="00fdf-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00fdf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="00fdf-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fdf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00fdf-107">DESCRIPTION</span></span>
<span data-ttu-id="00fdf-108">Das Cmdlet **Update-AzApiManagementApiRelease** ändert eine Azure API Management-API-Version.</span><span class="sxs-lookup"><span data-stu-id="00fdf-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="00fdf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00fdf-109">EXAMPLES</span></span>

### <span data-ttu-id="00fdf-110">Beispiel 1: aktualisiert eine API-Version für eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="00fdf-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="00fdf-111">Mit diesem Befehl wird die `echo-api-release` API-Version der API `echo-api` mit neuer Notiz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00fdf-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="00fdf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00fdf-112">PARAMETERS</span></span>

### <span data-ttu-id="00fdf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00fdf-113">-ApiId</span></span>
<span data-ttu-id="00fdf-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="00fdf-114">Identifier of existing API.</span></span>
<span data-ttu-id="00fdf-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00fdf-115">This parameter is required.</span></span>

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

### <span data-ttu-id="00fdf-116">-Context</span><span class="sxs-lookup"><span data-stu-id="00fdf-116">-Context</span></span>
<span data-ttu-id="00fdf-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="00fdf-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="00fdf-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00fdf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="00fdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fdf-119">-DefaultProfile</span></span>
<span data-ttu-id="00fdf-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00fdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00fdf-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="00fdf-121">-InputObject</span></span>
<span data-ttu-id="00fdf-122">Instanz des Typs Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="00fdf-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="00fdf-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="00fdf-123">-Note</span></span>
<span data-ttu-id="00fdf-124">Anmerkungen zur API-Version.</span><span class="sxs-lookup"><span data-stu-id="00fdf-124">Api Release Notes.</span></span>
<span data-ttu-id="00fdf-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="00fdf-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="00fdf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00fdf-126">-PassThru</span></span>
<span data-ttu-id="00fdf-127">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease-Typs, die die Version der festgelegten API darstellt.</span><span class="sxs-lookup"><span data-stu-id="00fdf-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="00fdf-128">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="00fdf-128">-ReleaseId</span></span>
<span data-ttu-id="00fdf-129">Bezeichner für die Versionskennung der API-Version.</span><span class="sxs-lookup"><span data-stu-id="00fdf-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="00fdf-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00fdf-130">This parameter is required.</span></span>

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

### <span data-ttu-id="00fdf-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00fdf-131">-Confirm</span></span>
<span data-ttu-id="00fdf-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00fdf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fdf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fdf-133">-WhatIf</span></span>
<span data-ttu-id="00fdf-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00fdf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fdf-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00fdf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fdf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fdf-136">CommonParameters</span></span>
<span data-ttu-id="00fdf-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fdf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fdf-138">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00fdf-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fdf-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00fdf-139">INPUTS</span></span>

### <span data-ttu-id="00fdf-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00fdf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00fdf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="00fdf-141">System.String</span></span>

### <span data-ttu-id="00fdf-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00fdf-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="00fdf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00fdf-143">OUTPUTS</span></span>

### <span data-ttu-id="00fdf-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00fdf-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="00fdf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="00fdf-145">NOTES</span></span>

## <span data-ttu-id="00fdf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00fdf-146">RELATED LINKS</span></span>

[<span data-ttu-id="00fdf-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00fdf-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="00fdf-148">Neu – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00fdf-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

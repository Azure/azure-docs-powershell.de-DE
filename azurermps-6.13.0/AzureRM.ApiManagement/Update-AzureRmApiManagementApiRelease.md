---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478014"
---
# <span data-ttu-id="f07fd-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f07fd-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="f07fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f07fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f07fd-103">Aktualisiert eine bestimmte API-Version.</span><span class="sxs-lookup"><span data-stu-id="f07fd-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f07fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f07fd-104">SYNTAX</span></span>

### <span data-ttu-id="f07fd-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f07fd-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f07fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f07fd-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07fd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f07fd-107">DESCRIPTION</span></span>
<span data-ttu-id="f07fd-108">Das Cmdlet **Update-AzureRmApiManagementApiRelease** ändert eine Azure API Management-API-Version.</span><span class="sxs-lookup"><span data-stu-id="f07fd-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="f07fd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f07fd-109">EXAMPLES</span></span>

### <span data-ttu-id="f07fd-110">Beispiel 1: aktualisiert eine API-Version für eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="f07fd-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="f07fd-111">Mit diesem Befehl wird die `echo-api-release` API-Version der API `echo-api` mit neuer Notiz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f07fd-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="f07fd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f07fd-112">PARAMETERS</span></span>

### <span data-ttu-id="f07fd-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f07fd-113">-ApiId</span></span>
<span data-ttu-id="f07fd-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="f07fd-114">Identifier of existing API.</span></span>
<span data-ttu-id="f07fd-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f07fd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="f07fd-116">-Context</span><span class="sxs-lookup"><span data-stu-id="f07fd-116">-Context</span></span>
<span data-ttu-id="f07fd-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f07fd-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f07fd-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f07fd-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f07fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07fd-119">-DefaultProfile</span></span>
<span data-ttu-id="f07fd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f07fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07fd-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f07fd-121">-InputObject</span></span>
<span data-ttu-id="f07fd-122">Instanz des Typs Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="f07fd-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="f07fd-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="f07fd-123">-Note</span></span>
<span data-ttu-id="f07fd-124">Anmerkungen zur API-Version.</span><span class="sxs-lookup"><span data-stu-id="f07fd-124">Api Release Notes.</span></span>
<span data-ttu-id="f07fd-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f07fd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="f07fd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f07fd-126">-PassThru</span></span>
<span data-ttu-id="f07fd-127">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease-Typs, die die Version der festgelegten API darstellt.</span><span class="sxs-lookup"><span data-stu-id="f07fd-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="f07fd-128">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="f07fd-128">-ReleaseId</span></span>
<span data-ttu-id="f07fd-129">Bezeichner für die Versionskennung der API-Version.</span><span class="sxs-lookup"><span data-stu-id="f07fd-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="f07fd-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f07fd-130">This parameter is required.</span></span>

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

### <span data-ttu-id="f07fd-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f07fd-131">-Confirm</span></span>
<span data-ttu-id="f07fd-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f07fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f07fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07fd-133">-WhatIf</span></span>
<span data-ttu-id="f07fd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f07fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07fd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f07fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f07fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07fd-136">CommonParameters</span></span>
<span data-ttu-id="f07fd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07fd-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07fd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07fd-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f07fd-139">INPUTS</span></span>

### <span data-ttu-id="f07fd-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f07fd-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="f07fd-141">Parameter: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f07fd-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="f07fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f07fd-142">System.String</span></span>

### <span data-ttu-id="f07fd-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f07fd-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f07fd-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f07fd-144">OUTPUTS</span></span>

### <span data-ttu-id="f07fd-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f07fd-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f07fd-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f07fd-146">NOTES</span></span>

## <span data-ttu-id="f07fd-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f07fd-147">RELATED LINKS</span></span>

[<span data-ttu-id="f07fd-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f07fd-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="f07fd-149">Neu – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f07fd-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

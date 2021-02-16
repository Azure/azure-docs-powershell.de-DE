---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157617"
---
# <span data-ttu-id="a423c-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a423c-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="a423c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a423c-102">SYNOPSIS</span></span>
<span data-ttu-id="a423c-103">Erstellt einen API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="a423c-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="a423c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a423c-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a423c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a423c-105">DESCRIPTION</span></span>
<span data-ttu-id="a423c-106">Das **Cmdlet "New-AzApiManagementApiVersionSet"** erstellt eine API-Versionssatzentität im Azure API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="a423c-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="a423c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a423c-107">EXAMPLES</span></span>

### <span data-ttu-id="a423c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a423c-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="a423c-109">Mit diesem Befehl wird ein API-Versionssatz erstellt, welches Versionsschema und `Query` welcher Abfrageparameter verwendet `api-version` wird.</span><span class="sxs-lookup"><span data-stu-id="a423c-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="a423c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a423c-110">PARAMETERS</span></span>

### <span data-ttu-id="a423c-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="a423c-111">-ApiVersionSetId</span></span>
<span data-ttu-id="a423c-112">Id für neue API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="a423c-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="a423c-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a423c-113">This parameter is optional.</span></span>
<span data-ttu-id="a423c-114">Wenn keine Angabe angegeben wird, wird ein Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="a423c-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="a423c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a423c-115">-Context</span></span>
<span data-ttu-id="a423c-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a423c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a423c-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a423c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="a423c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a423c-118">-DefaultProfile</span></span>
<span data-ttu-id="a423c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a423c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a423c-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a423c-120">-Description</span></span>
<span data-ttu-id="a423c-121">Beschreibung des Api-Versions-Sets.</span><span class="sxs-lookup"><span data-stu-id="a423c-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="a423c-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="a423c-122">-HeaderName</span></span>
<span data-ttu-id="a423c-123">Der Headerwert, der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a423c-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="a423c-124">Wenn schema header für die Versionsversion ausgewählt wird, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a423c-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="a423c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a423c-125">-Name</span></span>
<span data-ttu-id="a423c-126">Der Name des ApiVersion-Sets.</span><span class="sxs-lookup"><span data-stu-id="a423c-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="a423c-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a423c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a423c-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="a423c-128">-QueryName</span></span>
<span data-ttu-id="a423c-129">Der Abfragewert, der die Versionsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a423c-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="a423c-130">Wenn eine Schemaabfrage für die Versionsierung ausgewählt wird, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a423c-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="a423c-131">-Schema</span><span class="sxs-lookup"><span data-stu-id="a423c-131">-Scheme</span></span>
<span data-ttu-id="a423c-132">Versionsschema zum Auswählen für den API-Versionssatz.</span><span class="sxs-lookup"><span data-stu-id="a423c-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="a423c-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a423c-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a423c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a423c-134">-Confirm</span></span>
<span data-ttu-id="a423c-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a423c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a423c-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a423c-136">-WhatIf</span></span>
<span data-ttu-id="a423c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a423c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a423c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a423c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a423c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a423c-139">CommonParameters</span></span>
<span data-ttu-id="a423c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a423c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a423c-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a423c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a423c-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a423c-142">INPUTS</span></span>

### <span data-ttu-id="a423c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a423c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a423c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a423c-144">System.String</span></span>

### <span data-ttu-id="a423c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="a423c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="a423c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a423c-146">OUTPUTS</span></span>

### <span data-ttu-id="a423c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a423c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="a423c-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a423c-148">NOTES</span></span>

## <span data-ttu-id="a423c-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a423c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a423c-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a423c-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="a423c-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a423c-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="a423c-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="a423c-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
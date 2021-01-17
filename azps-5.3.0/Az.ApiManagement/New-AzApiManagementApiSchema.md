---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471432"
---
# <span data-ttu-id="d1a6f-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d1a6f-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="d1a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a6f-103">Erstellt das neue API-Schema im ApiManagement-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="d1a6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1a6f-104">SYNTAX</span></span>

### <span data-ttu-id="d1a6f-105">SchemaDocumentInline (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1a6f-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1a6f-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="d1a6f-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a6f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1a6f-107">DESCRIPTION</span></span>
<span data-ttu-id="d1a6f-108">Erstellt das neue API-Schema der API.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="d1a6f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d1a6f-109">EXAMPLES</span></span>

### <span data-ttu-id="d1a6f-110">Beispiel 1: Erstellen eines neuen Schemas für die umfangreiche API "Swagger Petstore"</span><span class="sxs-lookup"><span data-stu-id="d1a6f-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="d1a6f-111">Das Cmdlet **"New-AzApiManagementApiSchema"** erstellt oder aktualisiert das Schema des `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="d1a6f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a6f-112">PARAMETERS</span></span>

### <span data-ttu-id="d1a6f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1a6f-113">-ApiId</span></span>
<span data-ttu-id="d1a6f-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-114">Identifier of api.</span></span> <span data-ttu-id="d1a6f-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d1a6f-116">-Context</span><span class="sxs-lookup"><span data-stu-id="d1a6f-116">-Context</span></span>
<span data-ttu-id="d1a6f-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d1a6f-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d1a6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a6f-119">-DefaultProfile</span></span>
<span data-ttu-id="d1a6f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a6f-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="d1a6f-121">-SchemaDocument</span></span>
<span data-ttu-id="d1a6f-122">Api-Schemadokument als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-122">Api schema document as a string.</span></span> <span data-ttu-id="d1a6f-123">Dieser Parameter ist erforderlich: "-SchemaDocumentFile" wird nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a6f-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="d1a6f-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="d1a6f-125">ContentType des api-Schemas.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-125">ContentType of the api Schema.</span></span> <span data-ttu-id="d1a6f-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-126">This parameter is required.</span></span>

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

### <span data-ttu-id="d1a6f-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="d1a6f-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="d1a6f-128">Dateipfad des API-Schemadokuments.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-128">Api schema document file path.</span></span> <span data-ttu-id="d1a6f-129">Dieser Parameter ist erforderlich: "-SchemaDocument" wird nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a6f-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="d1a6f-130">-SchemaId</span></span>
<span data-ttu-id="d1a6f-131">Id des neuen Schemas.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-131">Identifier of new schema.</span></span>
<span data-ttu-id="d1a6f-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-132">This parameter is optional.</span></span>
<span data-ttu-id="d1a6f-133">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d1a6f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1a6f-134">-Confirm</span></span>
<span data-ttu-id="d1a6f-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a6f-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d1a6f-136">-WhatIf</span></span>
<span data-ttu-id="d1a6f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a6f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a6f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a6f-139">CommonParameters</span></span>
<span data-ttu-id="d1a6f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a6f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a6f-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1a6f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a6f-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d1a6f-142">INPUTS</span></span>

### <span data-ttu-id="d1a6f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1a6f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1a6f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d1a6f-144">System.String</span></span>

## <span data-ttu-id="d1a6f-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d1a6f-145">OUTPUTS</span></span>

### <span data-ttu-id="d1a6f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d1a6f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="d1a6f-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d1a6f-147">NOTES</span></span>

## <span data-ttu-id="d1a6f-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d1a6f-148">RELATED LINKS</span></span>

[<span data-ttu-id="d1a6f-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d1a6f-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="d1a6f-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d1a6f-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="d1a6f-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d1a6f-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)

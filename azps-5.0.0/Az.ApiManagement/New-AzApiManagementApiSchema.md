---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178089"
---
# <span data-ttu-id="e246d-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e246d-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="e246d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e246d-102">SYNOPSIS</span></span>
<span data-ttu-id="e246d-103">Erstellt das neue API-Schema im ApiManagement-Dienst</span><span class="sxs-lookup"><span data-stu-id="e246d-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="e246d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e246d-104">SYNTAX</span></span>

### <span data-ttu-id="e246d-105">SchemaDocumentInline (Standard)</span><span class="sxs-lookup"><span data-stu-id="e246d-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e246d-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="e246d-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e246d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e246d-107">DESCRIPTION</span></span>
<span data-ttu-id="e246d-108">Erstellt das neue API-Schema der API.</span><span class="sxs-lookup"><span data-stu-id="e246d-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="e246d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e246d-109">EXAMPLES</span></span>

### <span data-ttu-id="e246d-110">Beispiel 1: Erstellen eines neuen Schemas für Prahlerei PetStore extensive API</span><span class="sxs-lookup"><span data-stu-id="e246d-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="e246d-111">Das Cmdlet **New-AzApiManagementApiSchema** erstellt oder aktualisiert das Schema der `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="e246d-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="e246d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e246d-112">PARAMETERS</span></span>

### <span data-ttu-id="e246d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e246d-113">-ApiId</span></span>
<span data-ttu-id="e246d-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="e246d-114">Identifier of api.</span></span> <span data-ttu-id="e246d-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e246d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e246d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="e246d-116">-Context</span></span>
<span data-ttu-id="e246d-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e246d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e246d-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e246d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e246d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e246d-119">-DefaultProfile</span></span>
<span data-ttu-id="e246d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e246d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e246d-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="e246d-121">-SchemaDocument</span></span>
<span data-ttu-id="e246d-122">API-Schemadokument als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e246d-122">Api schema document as a string.</span></span> <span data-ttu-id="e246d-123">Dieser Parameter ist erforderlich, da-SchemaDocumentFile nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e246d-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="e246d-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="e246d-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="e246d-125">ContentType des API-Schemas.</span><span class="sxs-lookup"><span data-stu-id="e246d-125">ContentType of the api Schema.</span></span> <span data-ttu-id="e246d-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e246d-126">This parameter is required.</span></span>

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

### <span data-ttu-id="e246d-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="e246d-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="e246d-128">API-Schema-Dokument Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="e246d-128">Api schema document file path.</span></span> <span data-ttu-id="e246d-129">Dieser Parameter ist erforderlich, da-SchemaDocument nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e246d-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="e246d-130">-Schema-Nr</span><span class="sxs-lookup"><span data-stu-id="e246d-130">-SchemaId</span></span>
<span data-ttu-id="e246d-131">Bezeichner des neuen Schemas.</span><span class="sxs-lookup"><span data-stu-id="e246d-131">Identifier of new schema.</span></span>
<span data-ttu-id="e246d-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e246d-132">This parameter is optional.</span></span>
<span data-ttu-id="e246d-133">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="e246d-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e246d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e246d-134">-Confirm</span></span>
<span data-ttu-id="e246d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e246d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e246d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e246d-136">-WhatIf</span></span>
<span data-ttu-id="e246d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e246d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e246d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e246d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e246d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e246d-139">CommonParameters</span></span>
<span data-ttu-id="e246d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e246d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e246d-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e246d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e246d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e246d-142">INPUTS</span></span>

### <span data-ttu-id="e246d-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e246d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e246d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e246d-144">System.String</span></span>

## <span data-ttu-id="e246d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e246d-145">OUTPUTS</span></span>

### <span data-ttu-id="e246d-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e246d-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="e246d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="e246d-147">NOTES</span></span>

## <span data-ttu-id="e246d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e246d-148">RELATED LINKS</span></span>

[<span data-ttu-id="e246d-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e246d-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="e246d-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e246d-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="e246d-151">Satz-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e246d-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 23881baf47536db4fa694cf2165b8550b7f8cd62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004069"
---
# <span data-ttu-id="68744-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="68744-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="68744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68744-102">SYNOPSIS</span></span>
<span data-ttu-id="68744-103">Ändert ein API-Schema</span><span class="sxs-lookup"><span data-stu-id="68744-103">Modifies an API Schema</span></span>

## <span data-ttu-id="68744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68744-104">SYNTAX</span></span>

### <span data-ttu-id="68744-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="68744-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68744-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="68744-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68744-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="68744-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68744-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68744-108">DESCRIPTION</span></span>
<span data-ttu-id="68744-109">Das Cmdlet " **Satz-AzApiManagementApiSchema** " ändert ein Azure API Management-API-Schema.</span><span class="sxs-lookup"><span data-stu-id="68744-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="68744-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68744-110">EXAMPLES</span></span>

### <span data-ttu-id="68744-111">Beispiel 1: ändert ein API-Schema</span><span class="sxs-lookup"><span data-stu-id="68744-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="68744-112">Im Beispiel wird das API-Schema aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="68744-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="68744-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="68744-113">PARAMETERS</span></span>

### <span data-ttu-id="68744-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="68744-114">-ApiId</span></span>
<span data-ttu-id="68744-115">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="68744-115">Identifier of existing API.</span></span>
<span data-ttu-id="68744-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68744-116">This parameter is required.</span></span>

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

### <span data-ttu-id="68744-117">-Context</span><span class="sxs-lookup"><span data-stu-id="68744-117">-Context</span></span>
<span data-ttu-id="68744-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="68744-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="68744-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68744-119">This parameter is required.</span></span>

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

### <span data-ttu-id="68744-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68744-120">-DefaultProfile</span></span>
<span data-ttu-id="68744-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68744-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68744-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68744-122">-InputObject</span></span>
<span data-ttu-id="68744-123">Instanz von PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="68744-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="68744-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68744-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68744-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68744-125">-PassThru</span></span>
<span data-ttu-id="68744-126">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi-Typs, die die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="68744-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="68744-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="68744-127">-ResourceId</span></span>
<span data-ttu-id="68744-128">Arm-Resourcen-Diagnose-oder API-Schema</span><span class="sxs-lookup"><span data-stu-id="68744-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="68744-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68744-129">This parameter is required.</span></span>

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

### <span data-ttu-id="68744-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="68744-130">-SchemaDocument</span></span>
<span data-ttu-id="68744-131">API-Schemadokument als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="68744-131">Api schema document as a string.</span></span> <span data-ttu-id="68744-132">Dieser Parameter ist erforderlich, da-SchemaDocumentFile nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="68744-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68744-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="68744-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="68744-134">ContentType des API-Schemas.</span><span class="sxs-lookup"><span data-stu-id="68744-134">ContentType of the api Schema.</span></span> <span data-ttu-id="68744-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="68744-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68744-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="68744-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="68744-137">API-Schema-Dokument Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="68744-137">Api schema document file path.</span></span> <span data-ttu-id="68744-138">Dieser Parameter ist erforderlich, da-SchemaDocument nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="68744-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68744-139">-Schema-Nr</span><span class="sxs-lookup"><span data-stu-id="68744-139">-SchemaId</span></span>
<span data-ttu-id="68744-140">Bezeichner des vorhandenen Schemas</span><span class="sxs-lookup"><span data-stu-id="68744-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="68744-141">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68744-141">This parameter is required.</span></span>

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

### <span data-ttu-id="68744-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68744-142">-Confirm</span></span>
<span data-ttu-id="68744-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68744-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68744-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68744-144">-WhatIf</span></span>
<span data-ttu-id="68744-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68744-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68744-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68744-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68744-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68744-147">CommonParameters</span></span>
<span data-ttu-id="68744-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68744-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68744-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68744-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68744-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68744-150">INPUTS</span></span>

### <span data-ttu-id="68744-151">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68744-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68744-152">System. String</span><span class="sxs-lookup"><span data-stu-id="68744-152">System.String</span></span>

### <span data-ttu-id="68744-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="68744-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="68744-154">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="68744-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68744-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68744-155">OUTPUTS</span></span>

### <span data-ttu-id="68744-156">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="68744-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="68744-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="68744-157">NOTES</span></span>

## <span data-ttu-id="68744-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68744-158">RELATED LINKS</span></span>

[<span data-ttu-id="68744-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="68744-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="68744-160">Neu – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="68744-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="68744-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="68744-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)


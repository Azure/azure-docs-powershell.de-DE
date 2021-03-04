---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 3af651595ba51f7e5443a9f6447d07848470dc90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923091"
---
# <span data-ttu-id="7f4e0-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7f4e0-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="7f4e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4e0-103">Abrufen der Details des API-Schemas</span><span class="sxs-lookup"><span data-stu-id="7f4e0-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="7f4e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f4e0-104">SYNTAX</span></span>

### <span data-ttu-id="7f4e0-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f4e0-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f4e0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f4e0-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f4e0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f4e0-107">DESCRIPTION</span></span>
<span data-ttu-id="7f4e0-108">Das **Get-AzApiManagementApiSchema-Cmdlet** ruft die Details des API-Schemas ab.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="7f4e0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f4e0-109">EXAMPLES</span></span>

### <span data-ttu-id="7f4e0-110">Beispiel 1: Abrufen der Details aller Apischemas einer Api</span><span class="sxs-lookup"><span data-stu-id="7f4e0-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="7f4e0-111">Dieser Befehl ruft alle API-Schemas ab, die einer Api für einen bestimmten `swagger-petstore-extensive` ApiManagement-Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="7f4e0-112">Beispiel 2: Abrufen des bestimmten Schemas, das einer Api zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="7f4e0-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="7f4e0-113">Dieser Befehl ruft das API-Schema ab, das einer Api für einen bestimmten `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` ApiManagement-Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="7f4e0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7f4e0-114">PARAMETERS</span></span>

### <span data-ttu-id="7f4e0-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7f4e0-115">-ApiId</span></span>
<span data-ttu-id="7f4e0-116">API-Bezeichner, nach dem Sie suchen können.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-116">API identifier to look for.</span></span>
<span data-ttu-id="7f4e0-117">Wenn angegeben, wird versucht, die API über die ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e0-118">-Context</span><span class="sxs-lookup"><span data-stu-id="7f4e0-118">-Context</span></span>
<span data-ttu-id="7f4e0-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7f4e0-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4e0-121">-DefaultProfile</span></span>
<span data-ttu-id="7f4e0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4e0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4e0-123">-ResourceId</span></span>
<span data-ttu-id="7f4e0-124">Arm Resource Identifier eines Api-Schemas.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="7f4e0-125">Wenn angegeben, wird versucht, das Apischema durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="7f4e0-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e0-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="7f4e0-127">-SchemaId</span></span>
<span data-ttu-id="7f4e0-128">Der Bezeichner des Schemas.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4e0-129">CommonParameters</span></span>
<span data-ttu-id="7f4e0-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4e0-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f4e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4e0-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f4e0-132">INPUTS</span></span>

### <span data-ttu-id="7f4e0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7f4e0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7f4e0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7f4e0-134">System.String</span></span>

## <span data-ttu-id="7f4e0-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f4e0-135">OUTPUTS</span></span>

### <span data-ttu-id="7f4e0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7f4e0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="7f4e0-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7f4e0-137">NOTES</span></span>

## <span data-ttu-id="7f4e0-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7f4e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="7f4e0-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7f4e0-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="7f4e0-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7f4e0-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="7f4e0-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7f4e0-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
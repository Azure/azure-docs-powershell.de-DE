---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297149"
---
# <span data-ttu-id="ac232-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ac232-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="ac232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac232-102">SYNOPSIS</span></span>
<span data-ttu-id="ac232-103">Abrufen der Details des API-Schemas</span><span class="sxs-lookup"><span data-stu-id="ac232-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="ac232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac232-104">SYNTAX</span></span>

### <span data-ttu-id="ac232-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac232-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac232-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac232-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac232-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac232-107">DESCRIPTION</span></span>
<span data-ttu-id="ac232-108">Das **Cmdlet "Get-AzApiManagementApiSchema"** ruft die Details des API-Schemas ab.</span><span class="sxs-lookup"><span data-stu-id="ac232-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="ac232-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac232-109">EXAMPLES</span></span>

### <span data-ttu-id="ac232-110">Beispiel 1: Abrufen der Details aller Api-Schemas einer API</span><span class="sxs-lookup"><span data-stu-id="ac232-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="ac232-111">Dieser Befehl ruft alle API-Schemas ab, die einer API für `swagger-petstore-extensive` einen bestimmten ApiManagement-Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ac232-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="ac232-112">Beispiel 2: Abrufen des spezifischen Schemas, das einer API zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="ac232-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="ac232-113">Dieser Befehl ruft das API-Schema ab, `5cc9cf67e6ed3b1154e638bd` das einer API für einen `swagger-petstore-extensive` bestimmten ApiManagement-Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ac232-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="ac232-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac232-114">PARAMETERS</span></span>

### <span data-ttu-id="ac232-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ac232-115">-ApiId</span></span>
<span data-ttu-id="ac232-116">API-ID, nach der sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="ac232-116">API identifier to look for.</span></span>
<span data-ttu-id="ac232-117">Wenn diese Angabe angegeben wird, wird versucht, die API nach der ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac232-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="ac232-118">-Context</span><span class="sxs-lookup"><span data-stu-id="ac232-118">-Context</span></span>
<span data-ttu-id="ac232-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ac232-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ac232-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ac232-120">This parameter is required.</span></span>

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

### <span data-ttu-id="ac232-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac232-121">-DefaultProfile</span></span>
<span data-ttu-id="ac232-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac232-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac232-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac232-123">-ResourceId</span></span>
<span data-ttu-id="ac232-124">Arm Resource Identifier eines API-Schemas.</span><span class="sxs-lookup"><span data-stu-id="ac232-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="ac232-125">Bei Angabe wird versucht, nach dem Bezeichner nach dem API-Schema zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ac232-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="ac232-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ac232-126">This parameter is required.</span></span>

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

### <span data-ttu-id="ac232-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="ac232-127">-SchemaId</span></span>
<span data-ttu-id="ac232-128">Der Bezeichner des Schemas.</span><span class="sxs-lookup"><span data-stu-id="ac232-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="ac232-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac232-129">CommonParameters</span></span>
<span data-ttu-id="ac232-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac232-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac232-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac232-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac232-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac232-132">INPUTS</span></span>

### <span data-ttu-id="ac232-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac232-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac232-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ac232-134">System.String</span></span>

## <span data-ttu-id="ac232-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac232-135">OUTPUTS</span></span>

### <span data-ttu-id="ac232-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ac232-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="ac232-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac232-137">NOTES</span></span>

## <span data-ttu-id="ac232-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac232-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac232-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ac232-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="ac232-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ac232-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="ac232-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ac232-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
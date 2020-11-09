---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302254"
---
# <span data-ttu-id="0c8b3-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="0c8b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8b3-103">Abrufen der Details des API-Schemas</span><span class="sxs-lookup"><span data-stu-id="0c8b3-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="0c8b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c8b3-104">SYNTAX</span></span>

### <span data-ttu-id="0c8b3-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c8b3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c8b3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c8b3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c8b3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c8b3-107">DESCRIPTION</span></span>
<span data-ttu-id="0c8b3-108">Das Cmdlet " **Get-AzApiManagementApiSchema** " Ruft die Details des API-Schemas ab.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="0c8b3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c8b3-109">EXAMPLES</span></span>

### <span data-ttu-id="0c8b3-110">Beispiel 1: Abrufen der Details zum gesamten API-Schema einer API</span><span class="sxs-lookup"><span data-stu-id="0c8b3-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="0c8b3-111">Dieser Befehl ruft alle API-Schemas ab, die einer API `swagger-petstore-extensive` für einen bestimmten ApiManagement-Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="0c8b3-112">Beispiel 2: Abrufen des spezifischen Schemas, das einer API zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="0c8b3-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="0c8b3-113">Dieser Befehl ruft das API-Schema ab `5cc9cf67e6ed3b1154e638bd` , das einer API `swagger-petstore-extensive` für einen bestimmten ApiManagement-Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="0c8b3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c8b3-114">PARAMETERS</span></span>

### <span data-ttu-id="0c8b3-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0c8b3-115">-ApiId</span></span>
<span data-ttu-id="0c8b3-116">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-116">API identifier to look for.</span></span>
<span data-ttu-id="0c8b3-117">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="0c8b3-118">-Context</span><span class="sxs-lookup"><span data-stu-id="0c8b3-118">-Context</span></span>
<span data-ttu-id="0c8b3-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c8b3-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-120">This parameter is required.</span></span>

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

### <span data-ttu-id="0c8b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8b3-121">-DefaultProfile</span></span>
<span data-ttu-id="0c8b3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8b3-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0c8b3-123">-ResourceId</span></span>
<span data-ttu-id="0c8b3-124">Arm-Ressourcenbezeichner für ein API-Schema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="0c8b3-125">Wenn angegeben, wird versucht, das API-Schema nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="0c8b3-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-126">This parameter is required.</span></span>

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

### <span data-ttu-id="0c8b3-127">-Schema-Nr</span><span class="sxs-lookup"><span data-stu-id="0c8b3-127">-SchemaId</span></span>
<span data-ttu-id="0c8b3-128">Der Bezeichner des Schemas.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="0c8b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8b3-129">CommonParameters</span></span>
<span data-ttu-id="0c8b3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c8b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8b3-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c8b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8b3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c8b3-132">INPUTS</span></span>

### <span data-ttu-id="0c8b3-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c8b3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c8b3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0c8b3-134">System.String</span></span>

## <span data-ttu-id="0c8b3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c8b3-135">OUTPUTS</span></span>

### <span data-ttu-id="0c8b3-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="0c8b3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c8b3-137">NOTES</span></span>

## <span data-ttu-id="0c8b3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c8b3-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c8b3-139">Neu – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="0c8b3-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="0c8b3-141">Satz-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0c8b3-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
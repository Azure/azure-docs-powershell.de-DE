---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 6d9c099457c25831d0ce97786b8d710cf4c0dc98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167380"
---
# <span data-ttu-id="9ce36-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="9ce36-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="9ce36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ce36-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce36-103">Sie erhalten die Metadaten einer Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="9ce36-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="9ce36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ce36-104">SYNTAX</span></span>

### <span data-ttu-id="9ce36-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ce36-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ce36-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ce36-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ce36-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ce36-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ce36-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ce36-108">DESCRIPTION</span></span>
<span data-ttu-id="9ce36-109">Ruft vorhandene Dienstkonten im Gesundheitswesen ab, die im angegebenen Abonnement oder in einer Ressourcengruppe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9ce36-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="9ce36-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ce36-110">EXAMPLES</span></span>

### <span data-ttu-id="9ce36-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ce36-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="9ce36-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9ce36-112">Example 2</span></span>

<span data-ttu-id="9ce36-113">Ruft die Metadaten für alle Dienste im Gesundheitswesen in der bereitgestellten Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="9ce36-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="9ce36-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9ce36-114">Example 3</span></span>

<span data-ttu-id="9ce36-115">Ruft die Metadaten für alle Dienste im Gesundheitswesen im angegebenen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9ce36-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="9ce36-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ce36-116">PARAMETERS</span></span>

### <span data-ttu-id="9ce36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce36-117">-DefaultProfile</span></span>
<span data-ttu-id="9ce36-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ce36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ce36-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9ce36-119">-Name</span></span>
<span data-ttu-id="9ce36-120">Dienstname von HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="9ce36-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce36-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce36-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ce36-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9ce36-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce36-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ce36-123">-ResourceId</span></span>
<span data-ttu-id="9ce36-124">Ressourcen-ID-Name.</span><span class="sxs-lookup"><span data-stu-id="9ce36-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="9ce36-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce36-125">CommonParameters</span></span>
<span data-ttu-id="9ce36-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce36-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce36-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ce36-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce36-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ce36-128">INPUTS</span></span>

### <span data-ttu-id="9ce36-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9ce36-129">System.String</span></span>

## <span data-ttu-id="9ce36-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ce36-130">OUTPUTS</span></span>

### <span data-ttu-id="9ce36-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="9ce36-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="9ce36-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ce36-132">NOTES</span></span>

## <span data-ttu-id="9ce36-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ce36-133">RELATED LINKS</span></span>

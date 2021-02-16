---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148633"
---
# <span data-ttu-id="0ad98-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0ad98-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0ad98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad98-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad98-103">Holen Sie sich Das Kundenkonto.</span><span class="sxs-lookup"><span data-stu-id="0ad98-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="0ad98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ad98-104">SYNTAX</span></span>

### <span data-ttu-id="0ad98-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ad98-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ad98-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad98-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad98-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ad98-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad98-108">Das **Cmdlet "Get-AzCosmosDBAccount"** ruft die Liste aller vorhandenen "Vorname"-Konten für einen bestimmten ResourceGroupName ab und ruft ein einzelnes "Durchlaufsdb"-Konto für einen bestimmten ResourceGroupName und AccountName ab.</span><span class="sxs-lookup"><span data-stu-id="0ad98-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="0ad98-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ad98-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad98-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ad98-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="0ad98-111">Holen Sie sich das Dbdb-Datenbankkonto mit name databaseAccountName in ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0ad98-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="0ad98-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ad98-112">PARAMETERS</span></span>

### <span data-ttu-id="0ad98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad98-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad98-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ad98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad98-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad98-115">-Name</span></span>
<span data-ttu-id="0ad98-116">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="0ad98-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad98-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad98-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ad98-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ad98-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad98-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ad98-119">-ResourceId</span></span>
<span data-ttu-id="0ad98-120">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0ad98-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad98-121">CommonParameters</span></span>
<span data-ttu-id="0ad98-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad98-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ad98-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad98-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ad98-124">INPUTS</span></span>

### <span data-ttu-id="0ad98-125">Keine</span><span class="sxs-lookup"><span data-stu-id="0ad98-125">None</span></span>

## <span data-ttu-id="0ad98-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ad98-126">OUTPUTS</span></span>

### <span data-ttu-id="0ad98-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0ad98-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0ad98-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ad98-128">NOTES</span></span>

## <span data-ttu-id="0ad98-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ad98-129">RELATED LINKS</span></span>

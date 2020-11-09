---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299595"
---
# <span data-ttu-id="4ead9-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="4ead9-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="4ead9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ead9-102">SYNOPSIS</span></span>
<span data-ttu-id="4ead9-103">Rufen Sie CosmosDB-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="4ead9-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="4ead9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ead9-104">SYNTAX</span></span>

### <span data-ttu-id="4ead9-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ead9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ead9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ead9-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ead9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ead9-107">DESCRIPTION</span></span>
<span data-ttu-id="4ead9-108">Das Cmdlet " **Get-AzCosmosDBAccount** " Ruft die Liste aller vorhandenen CosmosDB-Konten für eine bestimmte ResourceGroupName ab und ruft ein einzelnes CosmosDB-Konto für eine bestimmte ResourceGroupName und einen angegebenen Kontonamen ab.</span><span class="sxs-lookup"><span data-stu-id="4ead9-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="4ead9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ead9-109">EXAMPLES</span></span>

### <span data-ttu-id="4ead9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ead9-110">Example 1</span></span>
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

<span data-ttu-id="4ead9-111">Abrufen des CosmosDB-Daten Bankkontos mit dem Namen databaseAccountName in der ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="4ead9-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="4ead9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ead9-112">PARAMETERS</span></span>

### <span data-ttu-id="4ead9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ead9-113">-DefaultProfile</span></span>
<span data-ttu-id="4ead9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ead9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ead9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4ead9-115">-Name</span></span>
<span data-ttu-id="4ead9-116">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="4ead9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4ead9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ead9-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ead9-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ead9-118">Name of resource group.</span></span>

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

### <span data-ttu-id="4ead9-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4ead9-119">-ResourceId</span></span>
<span data-ttu-id="4ead9-120">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="4ead9-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="4ead9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ead9-121">CommonParameters</span></span>
<span data-ttu-id="4ead9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ead9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ead9-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ead9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ead9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ead9-124">INPUTS</span></span>

### <span data-ttu-id="4ead9-125">Keine</span><span class="sxs-lookup"><span data-stu-id="4ead9-125">None</span></span>

## <span data-ttu-id="4ead9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ead9-126">OUTPUTS</span></span>

### <span data-ttu-id="4ead9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4ead9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4ead9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ead9-128">NOTES</span></span>

## <span data-ttu-id="4ead9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ead9-129">RELATED LINKS</span></span>

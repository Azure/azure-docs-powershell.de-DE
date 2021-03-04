---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: c143fed64e99dd9f564b4375c4ef20e5b5ad4354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934480"
---
# <span data-ttu-id="30707-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="30707-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="30707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30707-102">SYNOPSIS</span></span>
<span data-ttu-id="30707-103">Holen Sie sich Schlüssel{"ConnectionKeys", "PrimaryReadOnly" oder "Keys"} für das angegebene CosmosDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="30707-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="30707-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30707-104">SYNTAX</span></span>

### <span data-ttu-id="30707-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="30707-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30707-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30707-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30707-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30707-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30707-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30707-108">DESCRIPTION</span></span>
<span data-ttu-id="30707-109">Hier erhalten Sie die Liste der Verbindungstasten.</span><span class="sxs-lookup"><span data-stu-id="30707-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="30707-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30707-110">EXAMPLES</span></span>

### <span data-ttu-id="30707-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30707-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="30707-112">Listet die Schlüssel für das CosmosDB-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="30707-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="30707-113">Der Schlüsseltyp kann der Wert aus sein: ConnectionStrings, Keys und ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="30707-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="30707-114">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="30707-114">Default is Keys.</span></span>

## <span data-ttu-id="30707-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30707-115">PARAMETERS</span></span>

### <span data-ttu-id="30707-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30707-116">-DefaultProfile</span></span>
<span data-ttu-id="30707-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30707-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30707-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30707-118">-InputObject</span></span>
<span data-ttu-id="30707-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="30707-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30707-120">-Name</span><span class="sxs-lookup"><span data-stu-id="30707-120">-Name</span></span>
<span data-ttu-id="30707-121">Name des Datenbankkontos "Cosmos DB".</span><span class="sxs-lookup"><span data-stu-id="30707-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="30707-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30707-122">-ResourceGroupName</span></span>
<span data-ttu-id="30707-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30707-123">Name of resource group.</span></span>

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

### <span data-ttu-id="30707-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30707-124">-ResourceId</span></span>
<span data-ttu-id="30707-125">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="30707-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="30707-126">-Type</span><span class="sxs-lookup"><span data-stu-id="30707-126">-Type</span></span>
<span data-ttu-id="30707-127">Wert aus: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="30707-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="30707-128">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="30707-128">Default is Keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30707-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30707-129">CommonParameters</span></span>
<span data-ttu-id="30707-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30707-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30707-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30707-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30707-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30707-132">INPUTS</span></span>

### <span data-ttu-id="30707-133">Keine</span><span class="sxs-lookup"><span data-stu-id="30707-133">None</span></span>

## <span data-ttu-id="30707-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30707-134">OUTPUTS</span></span>

### <span data-ttu-id="30707-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="30707-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="30707-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="30707-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="30707-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="30707-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="30707-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30707-138">NOTES</span></span>

## <span data-ttu-id="30707-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30707-139">RELATED LINKS</span></span>

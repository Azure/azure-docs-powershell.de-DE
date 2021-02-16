---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166313"
---
# <span data-ttu-id="ba730-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba730-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="ba730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba730-102">SYNOPSIS</span></span>
<span data-ttu-id="ba730-103">Holen Sie sich Schlüssel{"ConnectionKeys", "PrimaryReadOnly" oder "Keys"} für das angegebene ThreadsDB-Konto.</span><span class="sxs-lookup"><span data-stu-id="ba730-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="ba730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba730-104">SYNTAX</span></span>

### <span data-ttu-id="ba730-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba730-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba730-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba730-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba730-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba730-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba730-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba730-108">DESCRIPTION</span></span>
<span data-ttu-id="ba730-109">Hier finden Sie die Liste der Verbindungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="ba730-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="ba730-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba730-110">EXAMPLES</span></span>

### <span data-ttu-id="ba730-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba730-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="ba730-112">Listet die Schlüssel für Das Konto von Unterndb auf.</span><span class="sxs-lookup"><span data-stu-id="ba730-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="ba730-113">Der Schlüsseltyp kann den Wert "from: ConnectionStrings", "Keys" und "ReadOnlyKeys" haben.</span><span class="sxs-lookup"><span data-stu-id="ba730-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="ba730-114">Der Standardwert ist "Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="ba730-114">Default is Keys.</span></span>

## <span data-ttu-id="ba730-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba730-115">PARAMETERS</span></span>

### <span data-ttu-id="ba730-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba730-116">-DefaultProfile</span></span>
<span data-ttu-id="ba730-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba730-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba730-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba730-118">-InputObject</span></span>
<span data-ttu-id="ba730-119">Objekt "Abt.-Konto"</span><span class="sxs-lookup"><span data-stu-id="ba730-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ba730-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ba730-120">-Name</span></span>
<span data-ttu-id="ba730-121">Der Name des Dbdatenbankkontos von Db.</span><span class="sxs-lookup"><span data-stu-id="ba730-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba730-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba730-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba730-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba730-123">Name of resource group.</span></span>

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

### <span data-ttu-id="ba730-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba730-124">-ResourceId</span></span>
<span data-ttu-id="ba730-125">ResourceId der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ba730-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="ba730-126">-Type</span><span class="sxs-lookup"><span data-stu-id="ba730-126">-Type</span></span>
<span data-ttu-id="ba730-127">Wert von: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="ba730-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="ba730-128">Der Standardwert ist "Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="ba730-128">Default is Keys.</span></span>

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

### <span data-ttu-id="ba730-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba730-129">CommonParameters</span></span>
<span data-ttu-id="ba730-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba730-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba730-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba730-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba730-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba730-132">INPUTS</span></span>

### <span data-ttu-id="ba730-133">Keine</span><span class="sxs-lookup"><span data-stu-id="ba730-133">None</span></span>

## <span data-ttu-id="ba730-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba730-134">OUTPUTS</span></span>

### <span data-ttu-id="ba730-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ba730-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="ba730-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="ba730-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="ba730-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="ba730-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="ba730-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ba730-138">NOTES</span></span>

## <span data-ttu-id="ba730-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ba730-139">RELATED LINKS</span></span>

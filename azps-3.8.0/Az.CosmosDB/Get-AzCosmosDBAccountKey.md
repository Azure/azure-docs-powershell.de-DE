---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: 6c0fb28010aff759c406ddd04db281dc05ce1f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845644"
---
# <span data-ttu-id="b69f8-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="b69f8-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="b69f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b69f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b69f8-103">Rufen Sie die Schlüssel {"ConnectionKeys", "PrimaryReadOnly" oder "Keys"} für das angegebene CosmosDB-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b69f8-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="b69f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b69f8-104">SYNTAX</span></span>

### <span data-ttu-id="b69f8-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b69f8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b69f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b69f8-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b69f8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b69f8-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b69f8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b69f8-108">DESCRIPTION</span></span>
<span data-ttu-id="b69f8-109">Rufen Sie die Liste der Verbindungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="b69f8-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="b69f8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b69f8-110">EXAMPLES</span></span>

### <span data-ttu-id="b69f8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b69f8-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="b69f8-112">Listet die Schlüssel für das CosmosDB-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="b69f8-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="b69f8-113">Der Schlüsseltyp kann Wert von sein: connectionStrings, Keys und ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="b69f8-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="b69f8-114">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b69f8-114">Default is Keys.</span></span>

## <span data-ttu-id="b69f8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b69f8-115">PARAMETERS</span></span>

### <span data-ttu-id="b69f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69f8-116">-DefaultProfile</span></span>
<span data-ttu-id="b69f8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b69f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69f8-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b69f8-118">-InputObject</span></span>
<span data-ttu-id="b69f8-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b69f8-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b69f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b69f8-120">-Name</span></span>
<span data-ttu-id="b69f8-121">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="b69f8-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b69f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b69f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="b69f8-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b69f8-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b69f8-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b69f8-124">-ResourceId</span></span>
<span data-ttu-id="b69f8-125">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="b69f8-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b69f8-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="b69f8-126">-Type</span></span>
<span data-ttu-id="b69f8-127">Wert von: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="b69f8-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="b69f8-128">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b69f8-128">Default is Keys.</span></span>

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

### <span data-ttu-id="b69f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69f8-129">CommonParameters</span></span>
<span data-ttu-id="b69f8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b69f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69f8-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b69f8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69f8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b69f8-132">INPUTS</span></span>

### <span data-ttu-id="b69f8-133">Keine</span><span class="sxs-lookup"><span data-stu-id="b69f8-133">None</span></span>

## <span data-ttu-id="b69f8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b69f8-134">OUTPUTS</span></span>

### <span data-ttu-id="b69f8-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b69f8-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="b69f8-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="b69f8-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="b69f8-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="b69f8-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="b69f8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b69f8-138">NOTES</span></span>

## <span data-ttu-id="b69f8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b69f8-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299589"
---
# <span data-ttu-id="f9243-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9243-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="f9243-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9243-102">SYNOPSIS</span></span>
<span data-ttu-id="f9243-103">Rufen Sie die Schlüssel {"ConnectionKeys", "PrimaryReadOnly" oder "Keys"} für das angegebene CosmosDB-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="f9243-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="f9243-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9243-104">SYNTAX</span></span>

### <span data-ttu-id="f9243-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9243-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9243-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9243-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9243-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9243-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9243-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9243-108">DESCRIPTION</span></span>
<span data-ttu-id="f9243-109">Rufen Sie die Liste der Verbindungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="f9243-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="f9243-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9243-110">EXAMPLES</span></span>

### <span data-ttu-id="f9243-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9243-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="f9243-112">Listet die Schlüssel für das CosmosDB-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="f9243-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="f9243-113">Der Schlüsseltyp kann Wert von sein: connectionStrings, Keys und ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="f9243-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="f9243-114">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f9243-114">Default is Keys.</span></span>

## <span data-ttu-id="f9243-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9243-115">PARAMETERS</span></span>

### <span data-ttu-id="f9243-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9243-116">-DefaultProfile</span></span>
<span data-ttu-id="f9243-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9243-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9243-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9243-118">-InputObject</span></span>
<span data-ttu-id="f9243-119">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="f9243-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f9243-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9243-120">-Name</span></span>
<span data-ttu-id="f9243-121">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="f9243-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f9243-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9243-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9243-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9243-123">Name of resource group.</span></span>

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

### <span data-ttu-id="f9243-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f9243-124">-ResourceId</span></span>
<span data-ttu-id="f9243-125">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="f9243-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="f9243-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="f9243-126">-Type</span></span>
<span data-ttu-id="f9243-127">Wert von: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="f9243-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="f9243-128">Standard ist Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f9243-128">Default is Keys.</span></span>

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

### <span data-ttu-id="f9243-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9243-129">CommonParameters</span></span>
<span data-ttu-id="f9243-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9243-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9243-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9243-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9243-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9243-132">INPUTS</span></span>

### <span data-ttu-id="f9243-133">Keine</span><span class="sxs-lookup"><span data-stu-id="f9243-133">None</span></span>

## <span data-ttu-id="f9243-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9243-134">OUTPUTS</span></span>

### <span data-ttu-id="f9243-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="f9243-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="f9243-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="f9243-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="f9243-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="f9243-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="f9243-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9243-138">NOTES</span></span>

## <span data-ttu-id="f9243-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9243-139">RELATED LINKS</span></span>

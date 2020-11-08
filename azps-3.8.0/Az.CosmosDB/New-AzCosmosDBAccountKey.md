---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996619"
---
# <span data-ttu-id="fe8d8-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe8d8-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="fe8d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8d8-103">Regenerieren eines angegebenen CosmosDB-kontoschlüssels</span><span class="sxs-lookup"><span data-stu-id="fe8d8-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="fe8d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe8d8-104">SYNTAX</span></span>

### <span data-ttu-id="fe8d8-105">ByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe8d8-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8d8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8d8-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8d8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8d8-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe8d8-108">DESCRIPTION</span></span>
<span data-ttu-id="fe8d8-109">Erstellen Sie ein neues CosmosDB-Konto in der angegebenen ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="fe8d8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe8d8-110">EXAMPLES</span></span>

### <span data-ttu-id="fe8d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe8d8-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="fe8d8-112">Neue Schlüssel werden für das Konto mit dem Kontonamen dbname in der ResourceGroup RG generiert.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="fe8d8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe8d8-113">PARAMETERS</span></span>

### <span data-ttu-id="fe8d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe8d8-114">-AsJob</span></span>
<span data-ttu-id="fe8d8-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe8d8-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8d8-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe8d8-116">-Confirm</span></span>
<span data-ttu-id="fe8d8-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8d8-118">-DefaultProfile</span></span>
<span data-ttu-id="fe8d8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe8d8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fe8d8-120">-InputObject</span></span>
<span data-ttu-id="fe8d8-121">CosmosDB-Kontoobjekt</span><span class="sxs-lookup"><span data-stu-id="fe8d8-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fe8d8-122">-Keykind</span><span class="sxs-lookup"><span data-stu-id="fe8d8-122">-KeyKind</span></span>
<span data-ttu-id="fe8d8-123">Die Zugriffstaste, die neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-123">The access key to regenerate.</span></span>
<span data-ttu-id="fe8d8-124">Akzeptierte Werte: primär, primaryReadonly, sekundär, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="fe8d8-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

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

### <span data-ttu-id="fe8d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fe8d8-125">-Name</span></span>
<span data-ttu-id="fe8d8-126">Name des Cosmos DB-Daten Bankkontos.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fe8d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe8d8-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="fe8d8-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fe8d8-129">-ResourceId</span></span>
<span data-ttu-id="fe8d8-130">Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="fe8d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8d8-131">-WhatIf</span></span>
<span data-ttu-id="fe8d8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8d8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8d8-134">CommonParameters</span></span>
<span data-ttu-id="fe8d8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe8d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8d8-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe8d8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8d8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe8d8-137">INPUTS</span></span>

### <span data-ttu-id="fe8d8-138">Keine</span><span class="sxs-lookup"><span data-stu-id="fe8d8-138">None</span></span>

## <span data-ttu-id="fe8d8-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe8d8-139">OUTPUTS</span></span>

### <span data-ttu-id="fe8d8-140">System. void</span><span class="sxs-lookup"><span data-stu-id="fe8d8-140">System.Void</span></span>

## <span data-ttu-id="fe8d8-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe8d8-141">NOTES</span></span>

## <span data-ttu-id="fe8d8-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe8d8-142">RELATED LINKS</span></span>

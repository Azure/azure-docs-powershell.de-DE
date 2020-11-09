---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299211"
---
# <span data-ttu-id="97a63-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="97a63-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="97a63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97a63-102">SYNOPSIS</span></span>
<span data-ttu-id="97a63-103">Erstellt ein neues CosmosDB-SqlUniqueKeyPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97a63-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="97a63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97a63-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97a63-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97a63-105">DESCRIPTION</span></span>
<span data-ttu-id="97a63-106">Das Cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** erstellt ein neues Objekt vom Typ PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="97a63-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="97a63-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97a63-107">EXAMPLES</span></span>

### <span data-ttu-id="97a63-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97a63-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="97a63-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a63-109">PARAMETERS</span></span>

### <span data-ttu-id="97a63-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a63-110">-DefaultProfile</span></span>
<span data-ttu-id="97a63-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97a63-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a63-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="97a63-112">-UniqueKey</span></span>
<span data-ttu-id="97a63-113">Datenbankname</span><span class="sxs-lookup"><span data-stu-id="97a63-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a63-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a63-114">CommonParameters</span></span>
<span data-ttu-id="97a63-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a63-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a63-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97a63-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a63-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97a63-117">INPUTS</span></span>

### <span data-ttu-id="97a63-118">Keine</span><span class="sxs-lookup"><span data-stu-id="97a63-118">None</span></span>

## <span data-ttu-id="97a63-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97a63-119">OUTPUTS</span></span>

### <span data-ttu-id="97a63-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="97a63-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="97a63-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="97a63-121">NOTES</span></span>

## <span data-ttu-id="97a63-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97a63-122">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167841"
---
# <span data-ttu-id="4178e-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="4178e-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="4178e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4178e-102">SYNOPSIS</span></span>
<span data-ttu-id="4178e-103">Erstellt ein neues Sql UniqueKey-Objekt aus".</span><span class="sxs-lookup"><span data-stu-id="4178e-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="4178e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4178e-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4178e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4178e-105">DESCRIPTION</span></span>
<span data-ttu-id="4178e-106">Das **Cmdlet "New-AzCosmosDBSqlUniqueKey"** erstellt ein neues Objekt vom Typ PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="4178e-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="4178e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4178e-107">EXAMPLES</span></span>

### <span data-ttu-id="4178e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4178e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="4178e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4178e-109">PARAMETERS</span></span>

### <span data-ttu-id="4178e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4178e-110">-DefaultProfile</span></span>
<span data-ttu-id="4178e-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4178e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4178e-112">-Path</span><span class="sxs-lookup"><span data-stu-id="4178e-112">-Path</span></span>
<span data-ttu-id="4178e-113">Array mit Zeichenfolgen von Pfadwerten</span><span class="sxs-lookup"><span data-stu-id="4178e-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4178e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4178e-114">CommonParameters</span></span>
<span data-ttu-id="4178e-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4178e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4178e-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4178e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4178e-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4178e-117">INPUTS</span></span>

### <span data-ttu-id="4178e-118">Keine</span><span class="sxs-lookup"><span data-stu-id="4178e-118">None</span></span>

## <span data-ttu-id="4178e-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4178e-119">OUTPUTS</span></span>

### <span data-ttu-id="4178e-120">Microsoft.Azure.Commands.SkriptsDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="4178e-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="4178e-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4178e-121">NOTES</span></span>

## <span data-ttu-id="4178e-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4178e-122">RELATED LINKS</span></span>

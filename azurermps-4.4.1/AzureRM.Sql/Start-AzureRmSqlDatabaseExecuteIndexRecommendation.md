---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664416"
---
# <span data-ttu-id="eb593-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="eb593-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="eb593-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb593-102">SYNOPSIS</span></span>
<span data-ttu-id="eb593-103">Startet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb593-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb593-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb593-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb593-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb593-105">DESCRIPTION</span></span>
<span data-ttu-id="eb593-106">Das Cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** startet den Workflow, der einen empfohlenen Indexvorgang für eine Azure SQL-Datenbank ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb593-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="eb593-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb593-107">EXAMPLES</span></span>

### <span data-ttu-id="eb593-108">Beispiel 1: Ausführen einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="eb593-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="eb593-109">Dieser Befehl führt eine Indexempfehlung aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="eb593-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb593-110">PARAMETERS</span></span>

### <span data-ttu-id="eb593-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb593-111">-DatabaseName</span></span>
<span data-ttu-id="eb593-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="eb593-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb593-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="eb593-113">-IndexRecommendationName</span></span>
<span data-ttu-id="eb593-114">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb593-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb593-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb593-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb593-116">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="eb593-116">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb593-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="eb593-117">-ServerName</span></span>
<span data-ttu-id="eb593-118">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow startet.</span><span class="sxs-lookup"><span data-stu-id="eb593-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb593-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb593-119">-DefaultProfile</span></span>
<span data-ttu-id="eb593-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb593-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb593-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb593-121">CommonParameters</span></span>
<span data-ttu-id="eb593-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb593-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb593-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb593-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb593-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb593-124">INPUTS</span></span>

## <span data-ttu-id="eb593-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb593-125">OUTPUTS</span></span>

## <span data-ttu-id="eb593-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb593-126">NOTES</span></span>

## <span data-ttu-id="eb593-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb593-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb593-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="eb593-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="eb593-129">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="eb593-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="eb593-130">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="eb593-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



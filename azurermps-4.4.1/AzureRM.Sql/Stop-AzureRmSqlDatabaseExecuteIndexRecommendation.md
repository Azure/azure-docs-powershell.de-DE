---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4fef918efd69d1ef5506efb70f1db94903845a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664414"
---
# <span data-ttu-id="872a4-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="872a4-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="872a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="872a4-102">SYNOPSIS</span></span>
<span data-ttu-id="872a4-103">Beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="872a4-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="872a4-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="872a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="872a4-105">DESCRIPTION</span></span>
<span data-ttu-id="872a4-106">Das Cmdlet **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** beendet den Workflow, der einen empfohlenen Indexvorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="872a4-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="872a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="872a4-107">EXAMPLES</span></span>

### <span data-ttu-id="872a4-108">Beispiel 1: Beenden der Ausführung einer Indexempfehlung</span><span class="sxs-lookup"><span data-stu-id="872a4-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="872a4-109">Dieser Befehl beendet die Ausführung einer Indexempfehlung.</span><span class="sxs-lookup"><span data-stu-id="872a4-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="872a4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="872a4-110">PARAMETERS</span></span>

### <span data-ttu-id="872a4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="872a4-111">-DatabaseName</span></span>
<span data-ttu-id="872a4-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="872a4-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="872a4-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="872a4-113">-IndexRecommendationName</span></span>
<span data-ttu-id="872a4-114">Gibt den Namen der Indexempfehlung an, die mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="872a4-114">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="872a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="872a4-116">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="872a4-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="872a4-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="872a4-117">-ServerName</span></span>
<span data-ttu-id="872a4-118">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow beendet.</span><span class="sxs-lookup"><span data-stu-id="872a4-118">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="872a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872a4-119">-DefaultProfile</span></span>
<span data-ttu-id="872a4-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="872a4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="872a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872a4-121">CommonParameters</span></span>
<span data-ttu-id="872a4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872a4-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872a4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872a4-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="872a4-124">INPUTS</span></span>

## <span data-ttu-id="872a4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="872a4-125">OUTPUTS</span></span>

## <span data-ttu-id="872a4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="872a4-126">NOTES</span></span>

## <span data-ttu-id="872a4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="872a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="872a4-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="872a4-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="872a4-129">Anfang-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="872a4-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="872a4-130">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="872a4-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



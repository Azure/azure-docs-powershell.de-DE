---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663414"
---
# <span data-ttu-id="6046e-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="6046e-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="6046e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6046e-102">SYNOPSIS</span></span>
<span data-ttu-id="6046e-103">Bricht den asynchronen Aktualisierungsvorgang für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="6046e-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6046e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6046e-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6046e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6046e-105">DESCRIPTION</span></span>
<span data-ttu-id="6046e-106">Mit dem Cmdlet " **Stop-AzureRmSqlDatabaseActivity** " wird der asynchrone Aktualisierungsvorgang für die Datenbank abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6046e-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="6046e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6046e-107">EXAMPLES</span></span>

### <span data-ttu-id="6046e-108">Beispiel 1: Abbrechen des asynchronen Updates-Vorgangs in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="6046e-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="6046e-109">Mit diesem Befehl wird der asynchrone Aktualisierungsvorgang für die Datenbank abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6046e-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="6046e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6046e-110">PARAMETERS</span></span>

### <span data-ttu-id="6046e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6046e-111">-DatabaseName</span></span>
<span data-ttu-id="6046e-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="6046e-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6046e-113">-DefaultProfile</span></span>
<span data-ttu-id="6046e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6046e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6046e-115">-ElasticPoolName</span></span>
<span data-ttu-id="6046e-116">Der Name des Azure SQL-elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="6046e-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-117">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="6046e-117">-OperationId</span></span>
<span data-ttu-id="6046e-118">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6046e-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6046e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6046e-120">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6046e-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="6046e-121">-ServerName</span></span>
<span data-ttu-id="6046e-122">Gibt den Namen des Microsoft SQL Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="6046e-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6046e-123">-Confirm</span></span>
<span data-ttu-id="6046e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6046e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6046e-125">-WhatIf</span></span>
<span data-ttu-id="6046e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6046e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6046e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6046e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6046e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6046e-128">CommonParameters</span></span>
<span data-ttu-id="6046e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6046e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6046e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6046e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6046e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6046e-131">INPUTS</span></span>

### <span data-ttu-id="6046e-132">Keine</span><span class="sxs-lookup"><span data-stu-id="6046e-132">None</span></span>
<span data-ttu-id="6046e-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6046e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6046e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6046e-134">OUTPUTS</span></span>

### <span data-ttu-id="6046e-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="6046e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="6046e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6046e-136">NOTES</span></span>

## <span data-ttu-id="6046e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6046e-137">RELATED LINKS</span></span>

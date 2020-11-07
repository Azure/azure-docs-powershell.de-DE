---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5bcd5c6317688cc433d83b002cd3cb81ea790aaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662213"
---
# <span data-ttu-id="6abfb-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="6abfb-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="6abfb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6abfb-102">SYNOPSIS</span></span>
<span data-ttu-id="6abfb-103">Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="6abfb-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6abfb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6abfb-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6abfb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6abfb-105">DESCRIPTION</span></span>
<span data-ttu-id="6abfb-106">Das Cmdlet " **Get-AzureRmSqlServerServiceObjective** " Ruft die verfügbaren Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="6abfb-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="6abfb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6abfb-107">EXAMPLES</span></span>

### <span data-ttu-id="6abfb-108">Beispiel 1: Abrufen von Dienst Zielen</span><span class="sxs-lookup"><span data-stu-id="6abfb-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="6abfb-109">Dieser Befehl ruft die Dienst Ziele für den Server mit dem Namen Server01 und die Datenbank mit dem Namen database01 ab.</span><span class="sxs-lookup"><span data-stu-id="6abfb-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="6abfb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6abfb-110">PARAMETERS</span></span>

### <span data-ttu-id="6abfb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6abfb-111">-DatabaseName</span></span>
<span data-ttu-id="6abfb-112">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="6abfb-112">SQL Database name.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6abfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6abfb-113">-DefaultProfile</span></span>
<span data-ttu-id="6abfb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6abfb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6abfb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6abfb-115">-ResourceGroupName</span></span>
<span data-ttu-id="6abfb-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6abfb-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6abfb-117">Dieses Cmdlet ruft Dienst Ziele für einen SQL-Datenbankserver ab, der dieser Ressource zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6abfb-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="6abfb-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="6abfb-118">-ServerName</span></span>
<span data-ttu-id="6abfb-119">Gibt den Namen eines SQL-Datenbank-SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="6abfb-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="6abfb-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6abfb-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="6abfb-121">Gibt den Namen eines Dienst Ziels für einen Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="6abfb-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="6abfb-122">Die zulässigen Werte für diesen Parameter sind: Basic, S0, S1, S2, P1, P2 und P3.</span><span class="sxs-lookup"><span data-stu-id="6abfb-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6abfb-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6abfb-123">-Confirm</span></span>
<span data-ttu-id="6abfb-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6abfb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6abfb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6abfb-125">-WhatIf</span></span>
<span data-ttu-id="6abfb-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6abfb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6abfb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6abfb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6abfb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6abfb-128">CommonParameters</span></span>
<span data-ttu-id="6abfb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6abfb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6abfb-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6abfb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6abfb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6abfb-131">INPUTS</span></span>

### <span data-ttu-id="6abfb-132">Keine</span><span class="sxs-lookup"><span data-stu-id="6abfb-132">None</span></span>
<span data-ttu-id="6abfb-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6abfb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6abfb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6abfb-134">OUTPUTS</span></span>

### <span data-ttu-id="6abfb-135">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="6abfb-135">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="6abfb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6abfb-136">NOTES</span></span>

## <span data-ttu-id="6abfb-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6abfb-137">RELATED LINKS</span></span>

[<span data-ttu-id="6abfb-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6abfb-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



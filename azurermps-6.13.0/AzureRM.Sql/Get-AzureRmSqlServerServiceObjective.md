---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 13ce7a2410f8231d4c5194fbd57d41074d0ca892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477674"
---
# <span data-ttu-id="d1173-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="d1173-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="d1173-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1173-102">SYNOPSIS</span></span>
<span data-ttu-id="d1173-103">Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="d1173-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1173-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1173-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1173-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1173-105">DESCRIPTION</span></span>
<span data-ttu-id="d1173-106">Das Cmdlet " **Get-AzureRmSqlServerServiceObjective** " Ruft die verfügbaren Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="d1173-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="d1173-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1173-107">EXAMPLES</span></span>

### <span data-ttu-id="d1173-108">Beispiel 1: Abrufen von Dienst Zielen</span><span class="sxs-lookup"><span data-stu-id="d1173-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="d1173-109">Dieser Befehl ruft die Dienst Ziele für den Server mit dem Namen Server01 und die Datenbank mit dem Namen database01 ab.</span><span class="sxs-lookup"><span data-stu-id="d1173-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="d1173-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1173-110">PARAMETERS</span></span>

### <span data-ttu-id="d1173-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1173-111">-DatabaseName</span></span>
<span data-ttu-id="d1173-112">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="d1173-112">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1173-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1173-113">-DefaultProfile</span></span>
<span data-ttu-id="d1173-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d1173-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1173-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1173-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1173-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d1173-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d1173-117">Dieses Cmdlet ruft Dienst Ziele für einen SQL-Datenbankserver ab, der dieser Ressource zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d1173-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="d1173-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="d1173-118">-ServerName</span></span>
<span data-ttu-id="d1173-119">Gibt den Namen eines SQL-Datenbank-SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="d1173-119">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1173-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d1173-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="d1173-121">Gibt den Namen eines Dienst Ziels für einen Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="d1173-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="d1173-122">Die zulässigen Werte für diesen Parameter sind: Basic, S0, S1, S2, P1, P2 und P3.</span><span class="sxs-lookup"><span data-stu-id="d1173-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1173-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1173-123">-Confirm</span></span>
<span data-ttu-id="d1173-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1173-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1173-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1173-125">-WhatIf</span></span>
<span data-ttu-id="d1173-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1173-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1173-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1173-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1173-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1173-128">CommonParameters</span></span>
<span data-ttu-id="d1173-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1173-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1173-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1173-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1173-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1173-131">INPUTS</span></span>

### <span data-ttu-id="d1173-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1173-132">System.String</span></span>

## <span data-ttu-id="d1173-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1173-133">OUTPUTS</span></span>

### <span data-ttu-id="d1173-134">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="d1173-134">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="d1173-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1173-135">NOTES</span></span>

## <span data-ttu-id="d1173-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1173-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1173-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d1173-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



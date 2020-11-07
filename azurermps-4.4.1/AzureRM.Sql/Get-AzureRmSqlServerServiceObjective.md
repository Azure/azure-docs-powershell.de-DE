---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664417"
---
# <span data-ttu-id="70224-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="70224-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="70224-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70224-102">SYNOPSIS</span></span>
<span data-ttu-id="70224-103">Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="70224-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70224-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70224-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70224-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70224-105">DESCRIPTION</span></span>
<span data-ttu-id="70224-106">Das Cmdlet " **Get-AzureRmSqlServerServiceObjective** " Ruft die verfügbaren Dienst Ziele für einen Azure SQL-Datenbankserver ab.</span><span class="sxs-lookup"><span data-stu-id="70224-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="70224-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70224-107">EXAMPLES</span></span>

### <span data-ttu-id="70224-108">Beispiel 1: Abrufen von Dienst Zielen</span><span class="sxs-lookup"><span data-stu-id="70224-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="70224-109">Dieser Befehl ruft die Dienst Ziele für den Server mit dem Namen Server01 und die Datenbank mit dem Namen database01 ab.</span><span class="sxs-lookup"><span data-stu-id="70224-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="70224-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70224-110">PARAMETERS</span></span>

### <span data-ttu-id="70224-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70224-111">-DatabaseName</span></span>
<span data-ttu-id="70224-112">Gibt den Namen einer Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="70224-112">Specifies the name of an Azure SQL Database.</span></span>

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

### <span data-ttu-id="70224-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70224-113">-ResourceGroupName</span></span>
<span data-ttu-id="70224-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="70224-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="70224-115">Dieses Cmdlet ruft Dienst Ziele für einen SQL-Datenbankserver ab, der dieser Ressource zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="70224-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="70224-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="70224-116">-ServerName</span></span>
<span data-ttu-id="70224-117">Gibt den Namen eines SQL-Datenbank-SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="70224-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="70224-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="70224-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="70224-119">Gibt den Namen eines Dienst Ziels für einen Azure SQL-Datenbankserver an.</span><span class="sxs-lookup"><span data-stu-id="70224-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="70224-120">Die zulässigen Werte für diesen Parameter sind: Basic, S0, S1, S2, P1, P2 und P3.</span><span class="sxs-lookup"><span data-stu-id="70224-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="70224-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70224-121">-Confirm</span></span>
<span data-ttu-id="70224-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70224-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70224-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70224-123">-WhatIf</span></span>
<span data-ttu-id="70224-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70224-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70224-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70224-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70224-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70224-126">-DefaultProfile</span></span>
<span data-ttu-id="70224-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70224-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70224-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70224-128">CommonParameters</span></span>
<span data-ttu-id="70224-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70224-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70224-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70224-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70224-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70224-131">INPUTS</span></span>

## <span data-ttu-id="70224-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70224-132">OUTPUTS</span></span>

### <span data-ttu-id="70224-133">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="70224-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="70224-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="70224-134">NOTES</span></span>

## <span data-ttu-id="70224-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70224-135">RELATED LINKS</span></span>

[<span data-ttu-id="70224-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="70224-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



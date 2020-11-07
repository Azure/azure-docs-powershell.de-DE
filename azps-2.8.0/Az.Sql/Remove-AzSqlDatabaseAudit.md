---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825967"
---
# <span data-ttu-id="db47b-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="db47b-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="db47b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db47b-102">SYNOPSIS</span></span>
<span data-ttu-id="db47b-103">Entfernt die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db47b-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="db47b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db47b-104">SYNTAX</span></span>

### <span data-ttu-id="db47b-105">DatabaseParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="db47b-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db47b-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db47b-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db47b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db47b-107">DESCRIPTION</span></span>
<span data-ttu-id="db47b-108">Das Cmdlet **Remove-AzSqlDatabaseAudit** entfernt die Überwachungseinstellungen einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db47b-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="db47b-109">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db47b-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="db47b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db47b-110">EXAMPLES</span></span>

### <span data-ttu-id="db47b-111">Beispiel 1: Entfernen der Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="db47b-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="db47b-112">Beispiel 2: entfernen, durch Pipeline, die Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="db47b-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="db47b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="db47b-113">PARAMETERS</span></span>

### <span data-ttu-id="db47b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db47b-114">-DatabaseName</span></span>
<span data-ttu-id="db47b-115">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="db47b-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="db47b-116">-DatabaseObject</span></span>
<span data-ttu-id="db47b-117">Das Datenbankobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db47b-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db47b-118">-DefaultProfile</span></span>
<span data-ttu-id="db47b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db47b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db47b-120">-ResourceGroupName</span></span>
<span data-ttu-id="db47b-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="db47b-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="db47b-122">-ServerName</span></span>
<span data-ttu-id="db47b-123">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="db47b-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db47b-124">-Confirm</span></span>
<span data-ttu-id="db47b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db47b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db47b-126">-WhatIf</span></span>
<span data-ttu-id="db47b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db47b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db47b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db47b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db47b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db47b-129">CommonParameters</span></span>
<span data-ttu-id="db47b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db47b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db47b-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db47b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db47b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db47b-132">INPUTS</span></span>

### <span data-ttu-id="db47b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="db47b-133">System.String</span></span>

### <span data-ttu-id="db47b-134">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="db47b-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="db47b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db47b-135">OUTPUTS</span></span>

### <span data-ttu-id="db47b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db47b-136">System.Boolean</span></span>

## <span data-ttu-id="db47b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="db47b-137">NOTES</span></span>

## <span data-ttu-id="db47b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db47b-138">RELATED LINKS</span></span>

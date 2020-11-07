---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 91c23a32fd25c184e46249424b439375caed6ac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659257"
---
# <span data-ttu-id="3cc3a-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="3cc3a-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="3cc3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc3a-103">Ruft den Status von Datenbankvorgängen ab.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="3cc3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cc3a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc3a-106">Das Cmdlet " **Get-AzSqlDatabaseActivity** " Ruft den Status von Datenbankvorgängen in Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="3cc3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="3cc3a-108">Beispiel 1: Abrufen des Status für alle SQL-Datenbankinstanzen</span><span class="sxs-lookup"><span data-stu-id="3cc3a-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3cc3a-109">Dieser Befehl gibt den Vorgangsstatus aller SQL-Datenbankinstanzen in einem elastischen Pool mit dem Namen "ElasticPool01" zurück.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="3cc3a-110">Beispiel 2: Abrufen des Status für alle SQL-Datenbankvorgänge</span><span class="sxs-lookup"><span data-stu-id="3cc3a-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3cc3a-111">Dieser Befehl gibt den Status aller SQL-Datenbankvorgänge in einer Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="3cc3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cc3a-112">PARAMETERS</span></span>

### <span data-ttu-id="3cc3a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cc3a-113">-DatabaseName</span></span>
<span data-ttu-id="3cc3a-114">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3cc3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc3a-115">-DefaultProfile</span></span>
<span data-ttu-id="3cc3a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cc3a-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3cc3a-117">-ElasticPoolName</span></span>
<span data-ttu-id="3cc3a-118">Gibt den Namen des elastischen Daten Bank Pools an, für den dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc3a-119">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="3cc3a-119">-OperationId</span></span>
<span data-ttu-id="3cc3a-120">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cc3a-122">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3cc3a-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="3cc3a-123">-ServerName</span></span>
<span data-ttu-id="3cc3a-124">Gibt den Namen des Microsoft SQL Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="3cc3a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cc3a-125">-Confirm</span></span>
<span data-ttu-id="3cc3a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc3a-127">-WhatIf</span></span>
<span data-ttu-id="3cc3a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc3a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc3a-130">CommonParameters</span></span>
<span data-ttu-id="3cc3a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc3a-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cc3a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc3a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cc3a-133">INPUTS</span></span>

### <span data-ttu-id="3cc3a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc3a-134">System.String</span></span>

### <span data-ttu-id="3cc3a-135">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3cc3a-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3cc3a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cc3a-136">OUTPUTS</span></span>

### <span data-ttu-id="3cc3a-137">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="3cc3a-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="3cc3a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cc3a-138">NOTES</span></span>

## <span data-ttu-id="3cc3a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cc3a-139">RELATED LINKS</span></span>

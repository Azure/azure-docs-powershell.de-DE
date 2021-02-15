---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145532"
---
# <span data-ttu-id="ce89c-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="ce89c-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="ce89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce89c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce89c-103">Bricht den Vorgang für asynchrone Updates für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce89c-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="ce89c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce89c-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce89c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce89c-105">DESCRIPTION</span></span>
<span data-ttu-id="ce89c-106">Das **Cmdlet "Stop-AzSqlDatabaseActivity"** bricht den asynchronen Aktualisierungsvorgang für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce89c-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="ce89c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce89c-107">EXAMPLES</span></span>

### <span data-ttu-id="ce89c-108">Beispiel 1: Abbrechen des Vorgangs für asynchrone Updates in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="ce89c-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="ce89c-109">Dieser Befehl bricht den Vorgang für asynchrone Aktualisierungen in der Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce89c-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="ce89c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce89c-110">PARAMETERS</span></span>

### <span data-ttu-id="ce89c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce89c-111">-DatabaseName</span></span>
<span data-ttu-id="ce89c-112">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="ce89c-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="ce89c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce89c-113">-DefaultProfile</span></span>
<span data-ttu-id="ce89c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce89c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce89c-115">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ce89c-115">-ElasticPoolName</span></span>
<span data-ttu-id="ce89c-116">Der Name des Azure SQL Pool pool.</span><span class="sxs-lookup"><span data-stu-id="ce89c-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="ce89c-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ce89c-117">-OperationId</span></span>
<span data-ttu-id="ce89c-118">Gibt die ID des Vorgangs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ce89c-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce89c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce89c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce89c-120">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ce89c-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ce89c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce89c-121">-ServerName</span></span>
<span data-ttu-id="ce89c-122">Gibt den Namen des Microsoft SQL Server an, das die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ce89c-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ce89c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce89c-123">-Confirm</span></span>
<span data-ttu-id="ce89c-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce89c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce89c-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce89c-125">-WhatIf</span></span>
<span data-ttu-id="ce89c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce89c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce89c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce89c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce89c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce89c-128">CommonParameters</span></span>
<span data-ttu-id="ce89c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce89c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce89c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce89c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce89c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce89c-131">INPUTS</span></span>

### <span data-ttu-id="ce89c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ce89c-132">System.String</span></span>

### <span data-ttu-id="ce89c-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce89c-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ce89c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce89c-134">OUTPUTS</span></span>

### <span data-ttu-id="ce89c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="ce89c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="ce89c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce89c-136">NOTES</span></span>

## <span data-ttu-id="ce89c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce89c-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168692"
---
# <span data-ttu-id="5b319-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5b319-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="5b319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b319-102">SYNOPSIS</span></span>
<span data-ttu-id="5b319-103">Erstellt einen neuen Wiederherstellungspunkt, aus dem eine SQL wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b319-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="5b319-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b319-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b319-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b319-105">DESCRIPTION</span></span>
<span data-ttu-id="5b319-106">Das **Cmdlet "New-AzSqlDatabaseRestorePoint"** erstellt einen neuen Wiederherstellungspunkt, aus dem ein Azure SQL Data Warehouse wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b319-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="5b319-107">Dieses Cmdlet wird derzeit für Azure SQL Data Warehouse unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b319-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="5b319-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b319-108">EXAMPLES</span></span>

### <span data-ttu-id="5b319-109">Beispiel 1: Erstellen eines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="5b319-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="5b319-110">Dieser Befehl erstellt einen Wiederherstellungspunkt für Azure SQL Data Warehouse und gibt die Details des Wiederherstellungspunkts zurück.</span><span class="sxs-lookup"><span data-stu-id="5b319-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="5b319-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b319-111">PARAMETERS</span></span>

### <span data-ttu-id="5b319-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b319-112">-DatabaseName</span></span>
<span data-ttu-id="5b319-113">Gibt den Namen der datenbank SQL an.</span><span class="sxs-lookup"><span data-stu-id="5b319-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b319-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b319-114">-DefaultProfile</span></span>
<span data-ttu-id="5b319-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5b319-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b319-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b319-116">-ResourceGroupName</span></span>
<span data-ttu-id="5b319-117">Gibt den Namen der Ressourcengruppe an, der die SQL Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5b319-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="5b319-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="5b319-118">-RestorePointLabel</span></span>
<span data-ttu-id="5b319-119">Gibt die Bezeichnung des Wiederherstellungspunkts zur einfachen Identifikation an.</span><span class="sxs-lookup"><span data-stu-id="5b319-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="5b319-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b319-120">-ServerName</span></span>
<span data-ttu-id="5b319-121">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="5b319-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="5b319-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b319-122">-Confirm</span></span>
<span data-ttu-id="5b319-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b319-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b319-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5b319-124">-WhatIf</span></span>
<span data-ttu-id="5b319-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b319-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b319-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b319-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b319-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b319-127">CommonParameters</span></span>
<span data-ttu-id="5b319-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b319-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b319-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b319-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b319-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b319-130">INPUTS</span></span>

### <span data-ttu-id="5b319-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5b319-131">System.String</span></span>

## <span data-ttu-id="5b319-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b319-132">OUTPUTS</span></span>

### <span data-ttu-id="5b319-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="5b319-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="5b319-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b319-134">NOTES</span></span>

## <span data-ttu-id="5b319-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b319-135">RELATED LINKS</span></span>

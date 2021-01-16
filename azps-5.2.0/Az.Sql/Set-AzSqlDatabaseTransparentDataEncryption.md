---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307595"
---
# <span data-ttu-id="1bc90-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1bc90-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="1bc90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bc90-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc90-103">Ändert die EIGENSCHAFT "TDE" für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1bc90-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="1bc90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bc90-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc90-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bc90-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc90-106">Das **Cmdlet "Set-AzSqlDatabaseTransparentDataEncryption"** ändert die Eigenschaft "Transparent Data Encryption (TDE)" einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1bc90-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="1bc90-107">Weitere Informationen finden Sie unter "Transparente Datenverschlüsselung mit Azure SQL-Datenbank" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="1bc90-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="1bc90-108">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc90-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1bc90-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1bc90-109">EXAMPLES</span></span>

### <span data-ttu-id="1bc90-110">Beispiel 1: Aktivieren von TDE für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="1bc90-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="1bc90-111">Mit diesem Befehl wird TDE für die Datenbank mit dem Namen "Database01" auf dem Server "Server01" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1bc90-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="1bc90-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bc90-112">PARAMETERS</span></span>

### <span data-ttu-id="1bc90-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1bc90-113">-DatabaseName</span></span>
<span data-ttu-id="1bc90-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1bc90-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1bc90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc90-115">-DefaultProfile</span></span>
<span data-ttu-id="1bc90-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1bc90-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bc90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc90-117">-ResourceGroupName</span></span>
<span data-ttu-id="1bc90-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1bc90-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1bc90-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1bc90-119">-ServerName</span></span>
<span data-ttu-id="1bc90-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="1bc90-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1bc90-121">-State</span><span class="sxs-lookup"><span data-stu-id="1bc90-121">-State</span></span>
<span data-ttu-id="1bc90-122">Gibt den Wert der Eigenschaft "TDE" an.</span><span class="sxs-lookup"><span data-stu-id="1bc90-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="1bc90-123">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1bc90-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bc90-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="1bc90-124">Enabled</span></span> 
- <span data-ttu-id="1bc90-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="1bc90-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc90-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bc90-126">-Confirm</span></span>
<span data-ttu-id="1bc90-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bc90-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bc90-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1bc90-128">-WhatIf</span></span>
<span data-ttu-id="1bc90-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bc90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bc90-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bc90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bc90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc90-131">CommonParameters</span></span>
<span data-ttu-id="1bc90-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc90-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bc90-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc90-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1bc90-134">INPUTS</span></span>

### <span data-ttu-id="1bc90-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="1bc90-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="1bc90-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1bc90-136">System.String</span></span>

## <span data-ttu-id="1bc90-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1bc90-137">OUTPUTS</span></span>

### <span data-ttu-id="1bc90-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="1bc90-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="1bc90-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1bc90-139">NOTES</span></span>

## <span data-ttu-id="1bc90-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1bc90-140">RELATED LINKS</span></span>

[<span data-ttu-id="1bc90-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1bc90-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="1bc90-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="1bc90-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="1bc90-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="1bc90-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



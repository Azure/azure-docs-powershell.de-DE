---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8e511fa2e83866ac1a0119c410369f7f13705f14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944705"
---
# <span data-ttu-id="aa203-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="aa203-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="aa203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa203-102">SYNOPSIS</span></span>
<span data-ttu-id="aa203-103">Ändert die TDE-Eigenschaft für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="aa203-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="aa203-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa203-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa203-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa203-105">DESCRIPTION</span></span>
<span data-ttu-id="aa203-106">Das **Cmdlet Set-AzSqlDatabaseTransparentDataEncryption** ändert die Eigenschaft Transparente Datenverschlüsselung (Transparent Data Encryption, TDE) einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="aa203-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="aa203-107">Weitere Informationen finden Sie unter Transparente Datenverschlüsselung mit Azure SQL -Datenbank https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="aa203-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="aa203-108">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa203-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="aa203-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa203-109">EXAMPLES</span></span>

### <span data-ttu-id="aa203-110">Beispiel 1: Aktivieren von TDE für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="aa203-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="aa203-111">Dieser Befehl aktiviert TDE für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="aa203-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="aa203-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa203-112">PARAMETERS</span></span>

### <span data-ttu-id="aa203-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa203-113">-DatabaseName</span></span>
<span data-ttu-id="aa203-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aa203-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aa203-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa203-115">-DefaultProfile</span></span>
<span data-ttu-id="aa203-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aa203-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa203-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa203-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa203-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="aa203-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="aa203-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="aa203-119">-ServerName</span></span>
<span data-ttu-id="aa203-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="aa203-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="aa203-121">-State</span><span class="sxs-lookup"><span data-stu-id="aa203-121">-State</span></span>
<span data-ttu-id="aa203-122">Gibt den Wert der TDE-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="aa203-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="aa203-123">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="aa203-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa203-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="aa203-124">Enabled</span></span> 
- <span data-ttu-id="aa203-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="aa203-125">Disabled</span></span>

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

### <span data-ttu-id="aa203-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa203-126">-Confirm</span></span>
<span data-ttu-id="aa203-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa203-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa203-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa203-128">-WhatIf</span></span>
<span data-ttu-id="aa203-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa203-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa203-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa203-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa203-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa203-131">CommonParameters</span></span>
<span data-ttu-id="aa203-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa203-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa203-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa203-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa203-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa203-134">INPUTS</span></span>

### <span data-ttu-id="aa203-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="aa203-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="aa203-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aa203-136">System.String</span></span>

## <span data-ttu-id="aa203-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa203-137">OUTPUTS</span></span>

### <span data-ttu-id="aa203-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="aa203-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="aa203-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aa203-139">NOTES</span></span>

## <span data-ttu-id="aa203-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aa203-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa203-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="aa203-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="aa203-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="aa203-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="aa203-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="aa203-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003143"
---
# <span data-ttu-id="0cc86-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0cc86-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="0cc86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cc86-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc86-103">Ändert die DSA-Eigenschaft für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0cc86-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="0cc86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc86-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cc86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cc86-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc86-106">Das Cmdlet " **festlegen-AzSqlDatabaseTransparentDataEncryption** " ändert die Eigenschaft "transparente Datenverschlüsselung" (DSA) einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0cc86-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="0cc86-107">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="0cc86-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="0cc86-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0cc86-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0cc86-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cc86-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc86-110">Beispiel 1: Aktivieren von DSA für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0cc86-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="0cc86-111">Mit diesem Befehl wird DSA für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0cc86-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0cc86-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc86-112">PARAMETERS</span></span>

### <span data-ttu-id="0cc86-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0cc86-113">-DatabaseName</span></span>
<span data-ttu-id="0cc86-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0cc86-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0cc86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc86-115">-DefaultProfile</span></span>
<span data-ttu-id="0cc86-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0cc86-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cc86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc86-117">-ResourceGroupName</span></span>
<span data-ttu-id="0cc86-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0cc86-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0cc86-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="0cc86-119">-ServerName</span></span>
<span data-ttu-id="0cc86-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="0cc86-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0cc86-121">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="0cc86-121">-State</span></span>
<span data-ttu-id="0cc86-122">Gibt den Wert der Eigenschaft "DSA" an.</span><span class="sxs-lookup"><span data-stu-id="0cc86-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="0cc86-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0cc86-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0cc86-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0cc86-124">Enabled</span></span> 
- <span data-ttu-id="0cc86-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0cc86-125">Disabled</span></span>

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

### <span data-ttu-id="0cc86-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0cc86-126">-Confirm</span></span>
<span data-ttu-id="0cc86-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cc86-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc86-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc86-128">-WhatIf</span></span>
<span data-ttu-id="0cc86-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cc86-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc86-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cc86-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc86-131">CommonParameters</span></span>
<span data-ttu-id="0cc86-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc86-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cc86-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc86-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cc86-134">INPUTS</span></span>

### <span data-ttu-id="0cc86-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="0cc86-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="0cc86-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0cc86-136">System.String</span></span>

## <span data-ttu-id="0cc86-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cc86-137">OUTPUTS</span></span>

### <span data-ttu-id="0cc86-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="0cc86-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="0cc86-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cc86-139">NOTES</span></span>

## <span data-ttu-id="0cc86-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cc86-140">RELATED LINKS</span></span>

[<span data-ttu-id="0cc86-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0cc86-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="0cc86-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="0cc86-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="0cc86-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="0cc86-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



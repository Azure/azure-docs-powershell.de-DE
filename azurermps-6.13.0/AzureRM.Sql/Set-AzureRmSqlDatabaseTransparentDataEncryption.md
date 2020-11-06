---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502849"
---
# <span data-ttu-id="ba463-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ba463-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="ba463-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba463-102">SYNOPSIS</span></span>
<span data-ttu-id="ba463-103">Ändert die DSA-Eigenschaft für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba463-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba463-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba463-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba463-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba463-105">DESCRIPTION</span></span>
<span data-ttu-id="ba463-106">Das Cmdlet " **festlegen-AzureRmSqlDatabaseTransparentDataEncryption** " ändert die Eigenschaft "transparente Datenverschlüsselung" (DSA) einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ba463-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="ba463-107">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="ba463-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="ba463-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba463-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ba463-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba463-109">EXAMPLES</span></span>

### <span data-ttu-id="ba463-110">Beispiel 1: Aktivieren von DSA für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="ba463-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="ba463-111">Mit diesem Befehl wird DSA für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ba463-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ba463-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba463-112">PARAMETERS</span></span>

### <span data-ttu-id="ba463-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba463-113">-DatabaseName</span></span>
<span data-ttu-id="ba463-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ba463-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba463-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba463-115">-DefaultProfile</span></span>
<span data-ttu-id="ba463-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba463-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba463-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba463-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba463-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ba463-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ba463-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba463-119">-ServerName</span></span>
<span data-ttu-id="ba463-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="ba463-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ba463-121">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="ba463-121">-State</span></span>
<span data-ttu-id="ba463-122">Gibt den Wert der Eigenschaft "DSA" an.</span><span class="sxs-lookup"><span data-stu-id="ba463-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="ba463-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ba463-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba463-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ba463-124">Enabled</span></span> 
- <span data-ttu-id="ba463-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="ba463-125">Disabled</span></span>

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

### <span data-ttu-id="ba463-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba463-126">-Confirm</span></span>
<span data-ttu-id="ba463-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba463-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba463-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba463-128">-WhatIf</span></span>
<span data-ttu-id="ba463-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba463-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba463-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba463-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba463-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba463-131">CommonParameters</span></span>
<span data-ttu-id="ba463-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba463-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba463-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba463-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba463-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba463-134">INPUTS</span></span>

### <span data-ttu-id="ba463-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="ba463-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="ba463-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba463-136">System.String</span></span>

## <span data-ttu-id="ba463-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba463-137">OUTPUTS</span></span>

### <span data-ttu-id="ba463-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="ba463-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="ba463-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba463-139">NOTES</span></span>

## <span data-ttu-id="ba463-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba463-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba463-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="ba463-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="ba463-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="ba463-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="ba463-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ba463-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



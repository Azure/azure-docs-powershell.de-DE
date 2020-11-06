---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0b2a9174f90ece49f417dd413e23da786b983a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478210"
---
# <span data-ttu-id="7fbb2-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7fbb2-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="7fbb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fbb2-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbb2-103">Ändert die DSA-Eigenschaft für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fbb2-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fbb2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fbb2-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbb2-106">Das Cmdlet " **festlegen-AzureRmSqlDatabaseTransparentDataEncryption** " ändert die Eigenschaft "transparente Datenverschlüsselung" (DSA) einer Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="7fbb2-107">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="7fbb2-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7fbb2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fbb2-109">EXAMPLES</span></span>

### <span data-ttu-id="7fbb2-110">Beispiel 1: Aktivieren von DSA für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="7fbb2-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="7fbb2-111">Mit diesem Befehl wird DSA für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="7fbb2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fbb2-112">PARAMETERS</span></span>

### <span data-ttu-id="7fbb2-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fbb2-113">-DatabaseName</span></span>
<span data-ttu-id="7fbb2-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbb2-115">-DefaultProfile</span></span>
<span data-ttu-id="7fbb2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7fbb2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbb2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7fbb2-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-118">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="7fbb2-119">-ServerName</span></span>
<span data-ttu-id="7fbb2-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-120">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-121">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="7fbb2-121">-State</span></span>
<span data-ttu-id="7fbb2-122">Gibt den Wert der Eigenschaft "DSA" an.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="7fbb2-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7fbb2-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7fbb2-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="7fbb2-124">Enabled</span></span> 
- <span data-ttu-id="7fbb2-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="7fbb2-125">Disabled</span></span>

```yaml
Type: TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fbb2-126">-Confirm</span></span>
<span data-ttu-id="7fbb2-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fbb2-128">-WhatIf</span></span>
<span data-ttu-id="7fbb2-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fbb2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbb2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbb2-131">CommonParameters</span></span>
<span data-ttu-id="7fbb2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbb2-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbb2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbb2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fbb2-134">INPUTS</span></span>

### <span data-ttu-id="7fbb2-135">Keine</span><span class="sxs-lookup"><span data-stu-id="7fbb2-135">None</span></span>
<span data-ttu-id="7fbb2-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7fbb2-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7fbb2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fbb2-137">OUTPUTS</span></span>

### <span data-ttu-id="7fbb2-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="7fbb2-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="7fbb2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fbb2-139">NOTES</span></span>

## <span data-ttu-id="7fbb2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fbb2-140">RELATED LINKS</span></span>

[<span data-ttu-id="7fbb2-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7fbb2-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="7fbb2-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="7fbb2-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="7fbb2-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7fbb2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



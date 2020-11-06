---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a6fe2e171338885af2367d6fec1cc3a97002b321
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504706"
---
# <span data-ttu-id="9c3f2-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9c3f2-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="9c3f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3f2-103">Ruft die Überwachungsrichtlinie einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c3f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c3f2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c3f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c3f2-105">DESCRIPTION</span></span>
<span data-ttu-id="9c3f2-106">Das Cmdlet " **Get-AzureRmSqlDatabaseAuditingPolicy** " Ruft die Überwachungsrichtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="9c3f2-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="9c3f2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c3f2-108">EXAMPLES</span></span>

### <span data-ttu-id="9c3f2-109">Beispiel 1: Abrufen der Überwachungsrichtlinie einer Azure SQL-Datenbank mit definierter Tabellen Überwachung</span><span class="sxs-lookup"><span data-stu-id="9c3f2-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="9c3f2-110">Beispiel 2: Abrufen der Überwachungsrichtlinie einer Azure SQL-Datenbank mit definierter BLOB-Überwachung</span><span class="sxs-lookup"><span data-stu-id="9c3f2-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="9c3f2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c3f2-111">PARAMETERS</span></span>

### <span data-ttu-id="9c3f2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c3f2-112">-DatabaseName</span></span>
<span data-ttu-id="9c3f2-113">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-113">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="9c3f2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3f2-114">-ResourceGroupName</span></span>
<span data-ttu-id="9c3f2-115">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-115">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9c3f2-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="9c3f2-116">-ServerName</span></span>
<span data-ttu-id="9c3f2-117">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-117">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="9c3f2-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c3f2-118">-Confirm</span></span>
<span data-ttu-id="9c3f2-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c3f2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c3f2-120">-WhatIf</span></span>
<span data-ttu-id="9c3f2-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c3f2-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c3f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3f2-123">-DefaultProfile</span></span>
<span data-ttu-id="9c3f2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c3f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3f2-125">CommonParameters</span></span>
<span data-ttu-id="9c3f2-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3f2-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3f2-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c3f2-128">INPUTS</span></span>

## <span data-ttu-id="9c3f2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c3f2-129">OUTPUTS</span></span>

### <span data-ttu-id="9c3f2-130">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9c3f2-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="9c3f2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c3f2-131">NOTES</span></span>

## <span data-ttu-id="9c3f2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c3f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="9c3f2-133">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="9c3f2-133">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="9c3f2-134">Satz-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9c3f2-134">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)




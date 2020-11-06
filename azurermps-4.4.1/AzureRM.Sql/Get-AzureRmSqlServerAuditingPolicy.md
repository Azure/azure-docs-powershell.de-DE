---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496814"
---
# <span data-ttu-id="f1cff-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1cff-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="f1cff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1cff-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cff-103">Ruft die Überwachungsrichtlinie eines SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="f1cff-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1cff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1cff-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1cff-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cff-106">Das Cmdlet " **Get-AzureRmSqlServerAuditingPolicy** " Ruft die Überwachungsrichtlinie eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="f1cff-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="f1cff-107">Geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f1cff-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f1cff-108">Dieses Cmdlet gibt eine Richtlinie zurück, die von den Azure SQL-Datenbanken verwendet wird, die beide im angegebenen Azure SQL Server definiert sind, und Ihre Überwachungsrichtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1cff-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="f1cff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1cff-109">EXAMPLES</span></span>

### <span data-ttu-id="f1cff-110">Beispiel 1: Abrufen der Überwachungsrichtlinie eines Azure SQL Server mit definierter Tabellen Überwachung</span><span class="sxs-lookup"><span data-stu-id="f1cff-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="f1cff-111">Beispiel 2: Abrufen der Überwachungsrichtlinie eines Azure SQL Server mit definierter BLOB-Überwachung</span><span class="sxs-lookup"><span data-stu-id="f1cff-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="f1cff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1cff-112">PARAMETERS</span></span>

### <span data-ttu-id="f1cff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1cff-113">-ResourceGroupName</span></span>
<span data-ttu-id="f1cff-114">Gibt den Namen der Ressourcengruppe an, der der Azure SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f1cff-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="f1cff-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="f1cff-115">-ServerName</span></span>
<span data-ttu-id="f1cff-116">Gibt den Namen des Azure SQL Server an, für den dieses Cmdlet die Überwachungsrichtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="f1cff-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="f1cff-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1cff-117">-Confirm</span></span>
<span data-ttu-id="f1cff-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1cff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cff-119">-WhatIf</span></span>
<span data-ttu-id="f1cff-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1cff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1cff-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1cff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cff-122">-DefaultProfile</span></span>
<span data-ttu-id="f1cff-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1cff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cff-124">CommonParameters</span></span>
<span data-ttu-id="f1cff-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cff-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cff-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1cff-127">INPUTS</span></span>

## <span data-ttu-id="f1cff-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1cff-128">OUTPUTS</span></span>

### <span data-ttu-id="f1cff-129">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f1cff-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="f1cff-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1cff-130">NOTES</span></span>

## <span data-ttu-id="f1cff-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1cff-131">RELATED LINKS</span></span>

[<span data-ttu-id="f1cff-132">Satz-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1cff-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f1cff-133">Verwenden von-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1cff-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f1cff-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f1cff-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



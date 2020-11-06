---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 4203609a97a9fc476292fca4020976539eb5d2b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504709"
---
# <span data-ttu-id="ad296-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ad296-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ad296-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad296-102">SYNOPSIS</span></span>
<span data-ttu-id="ad296-103">Ruft die Überwachungseinstellungen einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ad296-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad296-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad296-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad296-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad296-105">DESCRIPTION</span></span>
<span data-ttu-id="ad296-106">Das Cmdlet " **Get-AzureRmSqlDatabaseAuditing** " Ruft die Überwachungseinstellungen einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ad296-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ad296-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ad296-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="ad296-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad296-108">EXAMPLES</span></span>

### <span data-ttu-id="ad296-109">Beispiel 1: Abrufen der Überwachungseinstellungen einer Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ad296-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="ad296-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad296-110">PARAMETERS</span></span>

### <span data-ttu-id="ad296-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad296-111">-DatabaseName</span></span>
<span data-ttu-id="ad296-112">SQL-Datenbankname</span><span class="sxs-lookup"><span data-stu-id="ad296-112">SQL Database name.</span></span>

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

### <span data-ttu-id="ad296-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad296-113">-ResourceGroupName</span></span>
<span data-ttu-id="ad296-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad296-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad296-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="ad296-115">-ServerName</span></span>
<span data-ttu-id="ad296-116">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="ad296-116">SQL Database server name.</span></span>

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

### <span data-ttu-id="ad296-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad296-117">-Confirm</span></span>
<span data-ttu-id="ad296-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad296-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad296-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad296-119">-WhatIf</span></span>
<span data-ttu-id="ad296-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad296-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad296-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad296-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad296-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad296-122">-DefaultProfile</span></span>
<span data-ttu-id="ad296-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad296-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad296-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad296-124">CommonParameters</span></span>
<span data-ttu-id="ad296-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad296-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad296-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad296-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad296-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad296-127">INPUTS</span></span>

## <span data-ttu-id="ad296-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad296-128">OUTPUTS</span></span>

### <span data-ttu-id="ad296-129">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ad296-129">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ad296-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad296-130">NOTES</span></span>

## <span data-ttu-id="ad296-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad296-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483281"
---
# <span data-ttu-id="dfcca-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="dfcca-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="dfcca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfcca-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcca-103">Ruft die Überwachungseinstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="dfcca-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfcca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfcca-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfcca-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcca-106">Das Cmdlet " **Get-AzureRmSqlServerAuditing** " Ruft die BLOB-Überwachungsrichtlinie eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="dfcca-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="dfcca-107">Geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dfcca-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="dfcca-108">Dieses Cmdlet gibt eine Richtlinie zurück, die von den Azure SQL-Datenbanken verwendet wird, die im angegebenen Azure SQL Server definiert sind.</span><span class="sxs-lookup"><span data-stu-id="dfcca-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="dfcca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfcca-109">EXAMPLES</span></span>

### <span data-ttu-id="dfcca-110">Beispiel 1: Abrufen der Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="dfcca-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="dfcca-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfcca-111">PARAMETERS</span></span>

### <span data-ttu-id="dfcca-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcca-112">-ResourceGroupName</span></span>
<span data-ttu-id="dfcca-113">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfcca-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfcca-114">-Servername</span><span class="sxs-lookup"><span data-stu-id="dfcca-114">-ServerName</span></span>
<span data-ttu-id="dfcca-115">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="dfcca-115">SQL server name.</span></span>

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

### <span data-ttu-id="dfcca-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfcca-116">-Confirm</span></span>
<span data-ttu-id="dfcca-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfcca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcca-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcca-118">-WhatIf</span></span>
<span data-ttu-id="dfcca-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfcca-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfcca-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfcca-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcca-121">-DefaultProfile</span></span>
<span data-ttu-id="dfcca-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfcca-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfcca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcca-123">CommonParameters</span></span>
<span data-ttu-id="dfcca-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcca-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcca-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfcca-126">INPUTS</span></span>

## <span data-ttu-id="dfcca-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfcca-127">OUTPUTS</span></span>

### <span data-ttu-id="dfcca-128">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="dfcca-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="dfcca-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfcca-129">NOTES</span></span>

## <span data-ttu-id="dfcca-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfcca-130">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480858"
---
# <span data-ttu-id="2200f-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="2200f-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="2200f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2200f-102">SYNOPSIS</span></span>
<span data-ttu-id="2200f-103">Ruft die Überwachungseinstellungen eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="2200f-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2200f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2200f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2200f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2200f-105">DESCRIPTION</span></span>
<span data-ttu-id="2200f-106">Das Cmdlet " **Get-AzureRmSqlServerAuditing** " Ruft die BLOB-Überwachungsrichtlinie eines Azure SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="2200f-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="2200f-107">Geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2200f-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="2200f-108">Dieses Cmdlet gibt eine Richtlinie zurück, die von den Azure SQL-Datenbanken verwendet wird, die im angegebenen Azure SQL Server definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2200f-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="2200f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2200f-109">EXAMPLES</span></span>

### <span data-ttu-id="2200f-110">Beispiel 1: Abrufen der Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="2200f-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="2200f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2200f-111">PARAMETERS</span></span>

### <span data-ttu-id="2200f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2200f-112">-DefaultProfile</span></span>
<span data-ttu-id="2200f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2200f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2200f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2200f-114">-ResourceGroupName</span></span>
<span data-ttu-id="2200f-115">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2200f-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="2200f-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="2200f-116">-ServerName</span></span>
<span data-ttu-id="2200f-117">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="2200f-117">SQL server name.</span></span>

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

### <span data-ttu-id="2200f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2200f-118">-Confirm</span></span>
<span data-ttu-id="2200f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2200f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2200f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2200f-120">-WhatIf</span></span>
<span data-ttu-id="2200f-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2200f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2200f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2200f-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2200f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2200f-123">CommonParameters</span></span>
<span data-ttu-id="2200f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2200f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2200f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2200f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2200f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2200f-126">INPUTS</span></span>

### <span data-ttu-id="2200f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="2200f-127">None</span></span>
<span data-ttu-id="2200f-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2200f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2200f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2200f-129">OUTPUTS</span></span>

### <span data-ttu-id="2200f-130">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="2200f-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="2200f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2200f-131">NOTES</span></span>

## <span data-ttu-id="2200f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2200f-132">RELATED LINKS</span></span>

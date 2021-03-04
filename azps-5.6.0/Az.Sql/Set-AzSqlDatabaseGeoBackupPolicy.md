---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 18ae68a4ecf0a2511f992e42a202468193022d6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940819"
---
# <span data-ttu-id="fbff5-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fbff5-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="fbff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbff5-102">SYNOPSIS</span></span>
<span data-ttu-id="fbff5-103">Legt eine Datenbank-Geosicherungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="fbff5-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="fbff5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbff5-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbff5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbff5-105">DESCRIPTION</span></span>
<span data-ttu-id="fbff5-106">Das **Cmdlet Set-AzSqlDatabaseGeoBackupPolicy** legt die Geosicherungsrichtlinie fest, die auf eine Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="fbff5-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="fbff5-107">Dies ist eine Azure Backup-Ressource, die zum Definieren der Sicherungsspeicherrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbff5-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="fbff5-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbff5-108">EXAMPLES</span></span>

## <span data-ttu-id="fbff5-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fbff5-109">PARAMETERS</span></span>

### <span data-ttu-id="fbff5-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbff5-110">-DatabaseName</span></span>
<span data-ttu-id="fbff5-111">Gibt den Namen der Datenbank an, für die dieses Cmdlet die Geosicherungsrichtlinie festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="fbff5-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="fbff5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbff5-112">-DefaultProfile</span></span>
<span data-ttu-id="fbff5-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fbff5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbff5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbff5-114">-ResourceGroupName</span></span>
<span data-ttu-id="fbff5-115">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="fbff5-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="fbff5-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="fbff5-116">-ServerName</span></span>
<span data-ttu-id="fbff5-117">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="fbff5-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fbff5-118">-State</span><span class="sxs-lookup"><span data-stu-id="fbff5-118">-State</span></span>
<span data-ttu-id="fbff5-119">Gibt den Status der Geosicherungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="fbff5-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="fbff5-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="fbff5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fbff5-121">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="fbff5-121">Enabled</span></span> 
- <span data-ttu-id="fbff5-122">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="fbff5-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbff5-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbff5-123">-Confirm</span></span>
<span data-ttu-id="fbff5-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbff5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbff5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbff5-125">-WhatIf</span></span>
<span data-ttu-id="fbff5-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbff5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbff5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbff5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbff5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbff5-128">CommonParameters</span></span>
<span data-ttu-id="fbff5-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbff5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbff5-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbff5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbff5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbff5-131">INPUTS</span></span>

### <span data-ttu-id="fbff5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fbff5-132">System.String</span></span>

## <span data-ttu-id="fbff5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbff5-133">OUTPUTS</span></span>

### <span data-ttu-id="fbff5-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fbff5-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="fbff5-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fbff5-135">NOTES</span></span>

## <span data-ttu-id="fbff5-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fbff5-136">RELATED LINKS</span></span>

[<span data-ttu-id="fbff5-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fbff5-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="fbff5-138">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="fbff5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 3b1c2865e6e5084f3108409d9afae0979ae635b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943390"
---
# <span data-ttu-id="30ce6-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30ce6-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="30ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="30ce6-103">Ruft die langfristige Aufbewahrungsrichtlinie einer verwalteten Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="30ce6-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="30ce6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30ce6-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30ce6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="30ce6-106">Das **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy-Cmdlet** ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese verwaltete Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="30ce6-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="30ce6-107">Die Richtlinie ist eine Azure Backup-Ressource, die zum Definieren der Sicherungsspeicherrichtlinie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30ce6-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="30ce6-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30ce6-108">EXAMPLES</span></span>

### <span data-ttu-id="30ce6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30ce6-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="30ce6-110">Ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="30ce6-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="30ce6-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30ce6-111">PARAMETERS</span></span>

### <span data-ttu-id="30ce6-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30ce6-112">-DatabaseName</span></span>
<span data-ttu-id="30ce6-113">Der Name der azure verwalteten Datenbank, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30ce6-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="30ce6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ce6-114">-DefaultProfile</span></span>
<span data-ttu-id="30ce6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30ce6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ce6-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="30ce6-116">-InstanceName</span></span>
<span data-ttu-id="30ce6-117">Der Name der verwalteten Azure-Instanz, zu der die Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="30ce6-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="30ce6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ce6-118">-ResourceGroupName</span></span>
<span data-ttu-id="30ce6-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="30ce6-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="30ce6-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30ce6-120">-Confirm</span></span>
<span data-ttu-id="30ce6-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30ce6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ce6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ce6-122">-WhatIf</span></span>
<span data-ttu-id="30ce6-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30ce6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ce6-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30ce6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ce6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ce6-125">CommonParameters</span></span>
<span data-ttu-id="30ce6-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ce6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ce6-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30ce6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ce6-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30ce6-128">INPUTS</span></span>

### <span data-ttu-id="30ce6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="30ce6-129">System.String</span></span>

## <span data-ttu-id="30ce6-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30ce6-130">OUTPUTS</span></span>

### <span data-ttu-id="30ce6-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="30ce6-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="30ce6-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30ce6-132">NOTES</span></span>

## <span data-ttu-id="30ce6-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30ce6-133">RELATED LINKS</span></span>

[<span data-ttu-id="30ce6-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="30ce6-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="30ce6-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="30ce6-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="30ce6-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30ce6-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="30ce6-137">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="30ce6-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
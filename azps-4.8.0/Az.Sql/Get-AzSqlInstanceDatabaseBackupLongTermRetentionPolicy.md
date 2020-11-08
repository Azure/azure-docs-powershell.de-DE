---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173457"
---
# <span data-ttu-id="fe08a-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe08a-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="fe08a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe08a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe08a-103">Ruft die langfristige Aufbewahrungsrichtlinie einer verwalteten Datenbank ab</span><span class="sxs-lookup"><span data-stu-id="fe08a-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="fe08a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe08a-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe08a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe08a-105">DESCRIPTION</span></span>
<span data-ttu-id="fe08a-106">Das Cmdlet " **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese verwaltete Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="fe08a-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="fe08a-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe08a-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="fe08a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe08a-108">EXAMPLES</span></span>

### <span data-ttu-id="fe08a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe08a-109">Example 1</span></span>
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

<span data-ttu-id="fe08a-110">Ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="fe08a-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="fe08a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe08a-111">PARAMETERS</span></span>

### <span data-ttu-id="fe08a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe08a-112">-DatabaseName</span></span>
<span data-ttu-id="fe08a-113">Der Name der zu verwendenden Azure-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fe08a-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="fe08a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe08a-114">-DefaultProfile</span></span>
<span data-ttu-id="fe08a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe08a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe08a-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fe08a-116">-InstanceName</span></span>
<span data-ttu-id="fe08a-117">Der Name der Azure-verwalteten Instanz, zu der die Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="fe08a-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="fe08a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe08a-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe08a-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe08a-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe08a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe08a-120">-Confirm</span></span>
<span data-ttu-id="fe08a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe08a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe08a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe08a-122">-WhatIf</span></span>
<span data-ttu-id="fe08a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe08a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe08a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe08a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe08a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe08a-125">CommonParameters</span></span>
<span data-ttu-id="fe08a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe08a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe08a-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe08a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe08a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe08a-128">INPUTS</span></span>

### <span data-ttu-id="fe08a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fe08a-129">System.String</span></span>

## <span data-ttu-id="fe08a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe08a-130">OUTPUTS</span></span>

### <span data-ttu-id="fe08a-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fe08a-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="fe08a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe08a-132">NOTES</span></span>

## <span data-ttu-id="fe08a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe08a-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe08a-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe08a-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe08a-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe08a-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe08a-136">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe08a-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe08a-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fe08a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
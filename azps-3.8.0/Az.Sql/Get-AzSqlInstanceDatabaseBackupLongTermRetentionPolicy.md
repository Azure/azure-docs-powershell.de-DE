---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004494"
---
# <span data-ttu-id="d1e13-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1e13-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d1e13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1e13-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e13-103">Ruft die langfristige Aufbewahrungsrichtlinie einer verwalteten Datenbank ab</span><span class="sxs-lookup"><span data-stu-id="d1e13-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="d1e13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1e13-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1e13-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1e13-105">DESCRIPTION</span></span>
<span data-ttu-id="d1e13-106">Das Cmdlet " **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese verwaltete Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d1e13-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="d1e13-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e13-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d1e13-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1e13-108">EXAMPLES</span></span>

### <span data-ttu-id="d1e13-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1e13-109">Example 1</span></span>
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

<span data-ttu-id="d1e13-110">Ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="d1e13-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="d1e13-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1e13-111">PARAMETERS</span></span>

### <span data-ttu-id="d1e13-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1e13-112">-DatabaseName</span></span>
<span data-ttu-id="d1e13-113">Der Name der zu verwendenden Azure-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d1e13-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="d1e13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e13-114">-DefaultProfile</span></span>
<span data-ttu-id="d1e13-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1e13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e13-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1e13-116">-InstanceName</span></span>
<span data-ttu-id="d1e13-117">Der Name der Azure-verwalteten Instanz, zu der die Datenbank gehört.</span><span class="sxs-lookup"><span data-stu-id="d1e13-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="d1e13-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e13-118">-ResourceGroupName</span></span>
<span data-ttu-id="d1e13-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1e13-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1e13-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1e13-120">-Confirm</span></span>
<span data-ttu-id="d1e13-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1e13-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e13-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e13-122">-WhatIf</span></span>
<span data-ttu-id="d1e13-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e13-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e13-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1e13-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e13-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e13-125">CommonParameters</span></span>
<span data-ttu-id="d1e13-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1e13-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e13-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1e13-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e13-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1e13-128">INPUTS</span></span>

### <span data-ttu-id="d1e13-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e13-129">System.String</span></span>

## <span data-ttu-id="d1e13-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1e13-130">OUTPUTS</span></span>

### <span data-ttu-id="d1e13-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d1e13-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d1e13-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1e13-132">NOTES</span></span>

## <span data-ttu-id="d1e13-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1e13-133">RELATED LINKS</span></span>

[<span data-ttu-id="d1e13-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d1e13-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d1e13-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d1e13-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d1e13-136">Satz-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1e13-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d1e13-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d1e13-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163225"
---
# <span data-ttu-id="e8c27-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8c27-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="e8c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8c27-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c27-103">Entfernt ein Azure SQL-Datenbanksynchronisierungsmitglied.</span><span class="sxs-lookup"><span data-stu-id="e8c27-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e8c27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8c27-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8c27-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8c27-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c27-106">Das **Cmdlet "Remove-AzSqlSyncMember"** entfernt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="e8c27-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e8c27-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8c27-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c27-108">Beispiel 1: Entfernen eines Synchronisierungsmitglieds</span><span class="sxs-lookup"><span data-stu-id="e8c27-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="e8c27-109">Mit diesem Befehl wird das Azure SQL-Datenbanksynchronisierungsmember namens "syncMember01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8c27-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="e8c27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8c27-110">PARAMETERS</span></span>

### <span data-ttu-id="e8c27-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8c27-111">-DatabaseName</span></span>
<span data-ttu-id="e8c27-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e8c27-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e8c27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c27-113">-DefaultProfile</span></span>
<span data-ttu-id="e8c27-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e8c27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8c27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8c27-115">-Force</span></span>
<span data-ttu-id="e8c27-116">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="e8c27-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e8c27-117">-Name</span></span>
<span data-ttu-id="e8c27-118">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="e8c27-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c27-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8c27-119">-PassThru</span></span>
<span data-ttu-id="e8c27-120">Definiert, ob das entfernte Synchronisierungsmmitglied zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="e8c27-120">Defines Whether return the removed sync member</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c27-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c27-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8c27-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8c27-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8c27-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8c27-123">-ServerName</span></span>
<span data-ttu-id="e8c27-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e8c27-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e8c27-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c27-125">-SyncGroupName</span></span>
<span data-ttu-id="e8c27-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e8c27-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c27-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8c27-127">-Confirm</span></span>
<span data-ttu-id="e8c27-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8c27-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c27-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e8c27-129">-WhatIf</span></span>
<span data-ttu-id="e8c27-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8c27-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c27-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8c27-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c27-132">CommonParameters</span></span>
<span data-ttu-id="e8c27-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c27-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8c27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c27-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8c27-135">INPUTS</span></span>

### <span data-ttu-id="e8c27-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e8c27-136">System.String</span></span>

## <span data-ttu-id="e8c27-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8c27-137">OUTPUTS</span></span>

### <span data-ttu-id="e8c27-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e8c27-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e8c27-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8c27-139">NOTES</span></span>

## <span data-ttu-id="e8c27-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8c27-140">RELATED LINKS</span></span>

[<span data-ttu-id="e8c27-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8c27-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="e8c27-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8c27-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="e8c27-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8c27-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


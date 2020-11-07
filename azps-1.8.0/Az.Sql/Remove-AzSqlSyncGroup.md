---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 0010dad985755512e97aaccb14540ec16dc47cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659025"
---
# <span data-ttu-id="e3aab-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3aab-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="e3aab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3aab-102">SYNOPSIS</span></span>
<span data-ttu-id="e3aab-103">Entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3aab-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e3aab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3aab-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3aab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3aab-105">DESCRIPTION</span></span>
<span data-ttu-id="e3aab-106">Das Cmdlet **Remove-AzSqlSyncGroup** entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3aab-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e3aab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3aab-107">EXAMPLES</span></span>

### <span data-ttu-id="e3aab-108">Beispiel 1: Entfernen einer Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e3aab-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="e3aab-109">Dieser Befehl entfernt die Azure SQL-Daten Bank Synchronisierungsgruppe mit dem Namen syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="e3aab-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="e3aab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3aab-110">PARAMETERS</span></span>

### <span data-ttu-id="e3aab-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3aab-111">-DatabaseName</span></span>
<span data-ttu-id="e3aab-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e3aab-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e3aab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3aab-113">-DefaultProfile</span></span>
<span data-ttu-id="e3aab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e3aab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3aab-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3aab-115">-Force</span></span>
<span data-ttu-id="e3aab-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="e3aab-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e3aab-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e3aab-117">-Name</span></span>
<span data-ttu-id="e3aab-118">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3aab-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3aab-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3aab-119">-PassThru</span></span>
<span data-ttu-id="e3aab-120">Definiert, ob die entfernte Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="e3aab-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="e3aab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3aab-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3aab-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3aab-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3aab-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="e3aab-123">-ServerName</span></span>
<span data-ttu-id="e3aab-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e3aab-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e3aab-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3aab-125">-Confirm</span></span>
<span data-ttu-id="e3aab-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3aab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3aab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3aab-127">-WhatIf</span></span>
<span data-ttu-id="e3aab-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3aab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3aab-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3aab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3aab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3aab-130">CommonParameters</span></span>
<span data-ttu-id="e3aab-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3aab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3aab-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3aab-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3aab-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3aab-133">INPUTS</span></span>

### <span data-ttu-id="e3aab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e3aab-134">System.String</span></span>

## <span data-ttu-id="e3aab-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3aab-135">OUTPUTS</span></span>

### <span data-ttu-id="e3aab-136">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e3aab-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e3aab-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3aab-137">NOTES</span></span>

## <span data-ttu-id="e3aab-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3aab-138">RELATED LINKS</span></span>

[<span data-ttu-id="e3aab-139">Neu – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3aab-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="e3aab-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3aab-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="e3aab-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3aab-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)


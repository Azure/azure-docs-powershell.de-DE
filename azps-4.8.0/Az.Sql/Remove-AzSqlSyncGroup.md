---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008839"
---
# <span data-ttu-id="3e862-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e862-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="3e862-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e862-102">SYNOPSIS</span></span>
<span data-ttu-id="3e862-103">Entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3e862-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3e862-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e862-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e862-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e862-105">DESCRIPTION</span></span>
<span data-ttu-id="3e862-106">Das Cmdlet **Remove-AzSqlSyncGroup** entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3e862-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="3e862-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e862-107">EXAMPLES</span></span>

### <span data-ttu-id="3e862-108">Beispiel 1: Entfernen einer Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3e862-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="3e862-109">Dieser Befehl entfernt die Azure SQL-Daten Bank Synchronisierungsgruppe mit dem Namen syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="3e862-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="3e862-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e862-110">PARAMETERS</span></span>

### <span data-ttu-id="3e862-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e862-111">-DatabaseName</span></span>
<span data-ttu-id="3e862-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3e862-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3e862-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e862-113">-DefaultProfile</span></span>
<span data-ttu-id="3e862-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3e862-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e862-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3e862-115">-Force</span></span>
<span data-ttu-id="3e862-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="3e862-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3e862-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3e862-117">-Name</span></span>
<span data-ttu-id="3e862-118">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3e862-118">The sync group name.</span></span>

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

### <span data-ttu-id="3e862-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e862-119">-PassThru</span></span>
<span data-ttu-id="3e862-120">Definiert, ob die entfernte Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="3e862-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="3e862-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e862-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e862-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e862-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e862-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="3e862-123">-ServerName</span></span>
<span data-ttu-id="3e862-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e862-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="3e862-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e862-125">-Confirm</span></span>
<span data-ttu-id="3e862-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e862-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e862-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e862-127">-WhatIf</span></span>
<span data-ttu-id="3e862-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e862-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e862-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e862-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e862-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e862-130">CommonParameters</span></span>
<span data-ttu-id="3e862-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e862-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e862-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e862-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e862-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e862-133">INPUTS</span></span>

### <span data-ttu-id="3e862-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e862-134">System.String</span></span>

## <span data-ttu-id="3e862-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e862-135">OUTPUTS</span></span>

### <span data-ttu-id="3e862-136">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="3e862-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="3e862-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e862-137">NOTES</span></span>

## <span data-ttu-id="3e862-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e862-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e862-139">Neu – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e862-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="3e862-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e862-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="3e862-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3e862-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: e7c6dc8adc9aa3e5880b72997389144d0c402d89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826331"
---
# <span data-ttu-id="86c22-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="86c22-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="86c22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86c22-102">SYNOPSIS</span></span>
<span data-ttu-id="86c22-103">Beendet die Synchronisierung einer Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="86c22-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="86c22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86c22-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86c22-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86c22-105">DESCRIPTION</span></span>
<span data-ttu-id="86c22-106">Das Cmdlet " **Stop-AzSqlSyncGroupSync** " beendet die Synchronisierung der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="86c22-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="86c22-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86c22-107">EXAMPLES</span></span>

### <span data-ttu-id="86c22-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86c22-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="86c22-109">Dieser Befehl beendet die Synchronisierung, die für die Synchronisierungsgruppe mysg fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="86c22-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="86c22-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c22-110">PARAMETERS</span></span>

### <span data-ttu-id="86c22-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86c22-111">-DatabaseName</span></span>
<span data-ttu-id="86c22-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="86c22-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="86c22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c22-113">-DefaultProfile</span></span>
<span data-ttu-id="86c22-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="86c22-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c22-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c22-115">-PassThru</span></span>
<span data-ttu-id="86c22-116">Definiert, ob die Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="86c22-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="86c22-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c22-117">-ResourceGroupName</span></span>
<span data-ttu-id="86c22-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86c22-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="86c22-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="86c22-119">-ServerName</span></span>
<span data-ttu-id="86c22-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="86c22-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="86c22-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="86c22-121">-SyncGroupName</span></span>
<span data-ttu-id="86c22-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="86c22-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c22-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86c22-123">-Confirm</span></span>
<span data-ttu-id="86c22-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86c22-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c22-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c22-125">-WhatIf</span></span>
<span data-ttu-id="86c22-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86c22-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c22-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86c22-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c22-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c22-128">CommonParameters</span></span>
<span data-ttu-id="86c22-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c22-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c22-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86c22-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c22-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86c22-131">INPUTS</span></span>

### <span data-ttu-id="86c22-132">System. String</span><span class="sxs-lookup"><span data-stu-id="86c22-132">System.String</span></span>

## <span data-ttu-id="86c22-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86c22-133">OUTPUTS</span></span>

### <span data-ttu-id="86c22-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="86c22-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="86c22-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="86c22-135">NOTES</span></span>

## <span data-ttu-id="86c22-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86c22-136">RELATED LINKS</span></span>

[<span data-ttu-id="86c22-137">Anfang-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="86c22-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)


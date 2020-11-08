---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010433"
---
# <span data-ttu-id="c1afb-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c1afb-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="c1afb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1afb-102">SYNOPSIS</span></span>
<span data-ttu-id="c1afb-103">Startet eine Synchronisierungsgruppen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="c1afb-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="c1afb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1afb-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1afb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1afb-105">DESCRIPTION</span></span>
<span data-ttu-id="c1afb-106">Das Cmdlet **Start-AzSqlSyncGroupSync** startet eine Synchronisierungsgruppen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="c1afb-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="c1afb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1afb-107">EXAMPLES</span></span>

### <span data-ttu-id="c1afb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1afb-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="c1afb-109">Mit diesem Befehl wird eine Synchronisierungs Runde für die Synchronisierungsgruppe mysg.</span><span class="sxs-lookup"><span data-stu-id="c1afb-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="c1afb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1afb-110">PARAMETERS</span></span>

### <span data-ttu-id="c1afb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1afb-111">-DatabaseName</span></span>
<span data-ttu-id="c1afb-112">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c1afb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c1afb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1afb-113">-DefaultProfile</span></span>
<span data-ttu-id="c1afb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c1afb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1afb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1afb-115">-PassThru</span></span>
<span data-ttu-id="c1afb-116">Definiert, ob die Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="c1afb-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="c1afb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1afb-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1afb-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1afb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1afb-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="c1afb-119">-ServerName</span></span>
<span data-ttu-id="c1afb-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c1afb-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c1afb-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c1afb-121">-SyncGroupName</span></span>
<span data-ttu-id="c1afb-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c1afb-122">The sync group name.</span></span>

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

### <span data-ttu-id="c1afb-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1afb-123">-Confirm</span></span>
<span data-ttu-id="c1afb-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1afb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1afb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1afb-125">-WhatIf</span></span>
<span data-ttu-id="c1afb-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1afb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1afb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1afb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1afb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1afb-128">CommonParameters</span></span>
<span data-ttu-id="c1afb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1afb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1afb-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1afb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1afb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1afb-131">INPUTS</span></span>

### <span data-ttu-id="c1afb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c1afb-132">System.String</span></span>

## <span data-ttu-id="c1afb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1afb-133">OUTPUTS</span></span>

### <span data-ttu-id="c1afb-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c1afb-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c1afb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1afb-135">NOTES</span></span>

## <span data-ttu-id="c1afb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1afb-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1afb-137">Stopp-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="c1afb-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846420"
---
# <span data-ttu-id="5899d-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="5899d-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="5899d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5899d-102">SYNOPSIS</span></span>
<span data-ttu-id="5899d-103">Aktualisieren Sie das Synchronisierungs Schema für eine Synchronisierungs Mitglieder-Datenbank oder eine Synchronisierungs-Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5899d-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="5899d-104">Sie erhält das aktuelle Datenbankschema aus der realen Datenbank und verwendet Sie dann, um das von der Synchronisierungs-Metadaten-Datenbank zwischengespeicherte Schema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5899d-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="5899d-105">Wenn "SyncMemberName" angegeben ist, wird das Mitgliedsdaten Bank Schema aktualisiert; Wenn dies nicht der Fall ist, wird das Hub-Datenbankschema aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5899d-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="5899d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5899d-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5899d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5899d-107">DESCRIPTION</span></span>
<span data-ttu-id="5899d-108">Das Cmdlet **Update-AzSqlSyncSchema** aktualisiert das Synchronisierungs Schema für eine Synchronisierungs Mitglieder-Datenbank oder eine Synchronisierungs-Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5899d-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="5899d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5899d-109">EXAMPLES</span></span>

### <span data-ttu-id="5899d-110">Beispiel 1: Aktualisieren des Synchronisierungsschemas für eine Hub-Datenbank</span><span class="sxs-lookup"><span data-stu-id="5899d-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="5899d-111">Dieser Befehl aktualisiert das Synchronisierungs Schema für die Hub-Datenbank in der Synchronisierungsgruppe syncGroup01</span><span class="sxs-lookup"><span data-stu-id="5899d-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="5899d-112">Beispiel 2: Aktualisieren des Synchronisierungsschemas für eine Mitgliedsdatenbank</span><span class="sxs-lookup"><span data-stu-id="5899d-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="5899d-113">Mit diesem Befehl wird das Synchronisierungs Schema für die Mitgliedsdatenbank in der Synchronisierungs Member-syncMember01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5899d-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="5899d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5899d-114">PARAMETERS</span></span>

### <span data-ttu-id="5899d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5899d-115">-DatabaseName</span></span>
<span data-ttu-id="5899d-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5899d-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5899d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5899d-117">-DefaultProfile</span></span>
<span data-ttu-id="5899d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5899d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5899d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5899d-119">-PassThru</span></span>
<span data-ttu-id="5899d-120">Definiert, ob die Synchronisierungsgruppe, für die dieses Cmdlet verwendet wird, zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="5899d-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="5899d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5899d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5899d-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5899d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5899d-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="5899d-123">-ServerName</span></span>
<span data-ttu-id="5899d-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5899d-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5899d-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5899d-125">-SyncGroupName</span></span>
<span data-ttu-id="5899d-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5899d-126">The sync group name.</span></span>

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

### <span data-ttu-id="5899d-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="5899d-127">-SyncMemberName</span></span>
<span data-ttu-id="5899d-128">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="5899d-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5899d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5899d-129">-Confirm</span></span>
<span data-ttu-id="5899d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5899d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5899d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5899d-131">-WhatIf</span></span>
<span data-ttu-id="5899d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5899d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5899d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5899d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5899d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5899d-134">CommonParameters</span></span>
<span data-ttu-id="5899d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5899d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5899d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5899d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5899d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5899d-137">INPUTS</span></span>

### <span data-ttu-id="5899d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5899d-138">System.String</span></span>

## <span data-ttu-id="5899d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5899d-139">OUTPUTS</span></span>

### <span data-ttu-id="5899d-140">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5899d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5899d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5899d-141">NOTES</span></span>

## <span data-ttu-id="5899d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5899d-142">RELATED LINKS</span></span>

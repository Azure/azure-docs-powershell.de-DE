---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467984"
---
# <span data-ttu-id="f72ef-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="f72ef-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="f72ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f72ef-103">Aktualisieren Sie das Synchronisierungsschema für eine Synchronisierungsmitgliedsdatenbank oder eine Synchronisierungshubdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f72ef-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="f72ef-104">Es wird das neueste Datenbankschema aus der echten Datenbank erhalten und dann verwendet, um das von der Synchronisierungsmetadatendatenbank zwischengespeicherte Schema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f72ef-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="f72ef-105">Wenn "SyncMemberName" angegeben ist, wird das Memberdatenbankschema aktualisiert. andern falls nicht, wird das Hubdatenbankschema aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f72ef-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="f72ef-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f72ef-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f72ef-107">DESCRIPTION</span></span>
<span data-ttu-id="f72ef-108">Das **Cmdlet "Update-AzSqlSyncSchema"** aktualisiert das Synchronisierungsschema für eine Synchronisierungsmitgliedsdatenbank oder eine Synchronisierungshubdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f72ef-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="f72ef-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f72ef-109">EXAMPLES</span></span>

### <span data-ttu-id="f72ef-110">Beispiel 1: Aktualisieren des Synchronisierungsschemas für eine Hubdatenbank</span><span class="sxs-lookup"><span data-stu-id="f72ef-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="f72ef-111">Mit diesem Befehl wird das Synchronisierungsschema für die Hubdatenbank in der Synchronisierungsgruppe syncGroup01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f72ef-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="f72ef-112">Beispiel 2: Aktualisieren des Synchronisierungsschemas für eine Memberdatenbank</span><span class="sxs-lookup"><span data-stu-id="f72ef-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="f72ef-113">Mit diesem Befehl wird das Synchronisierungsschema für die Memberdatenbank im Synchronisierungsmember01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f72ef-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="f72ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f72ef-114">PARAMETERS</span></span>

### <span data-ttu-id="f72ef-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f72ef-115">-DatabaseName</span></span>
<span data-ttu-id="f72ef-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f72ef-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f72ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72ef-117">-DefaultProfile</span></span>
<span data-ttu-id="f72ef-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f72ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f72ef-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f72ef-119">-PassThru</span></span>
<span data-ttu-id="f72ef-120">Definiert, ob die Synchronisierungsgruppe, an der dieses Cmdlet arbeitet, zurücksentrat</span><span class="sxs-lookup"><span data-stu-id="f72ef-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="f72ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="f72ef-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f72ef-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f72ef-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f72ef-123">-ServerName</span></span>
<span data-ttu-id="f72ef-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f72ef-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f72ef-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f72ef-125">-SyncGroupName</span></span>
<span data-ttu-id="f72ef-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f72ef-126">The sync group name.</span></span>

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

### <span data-ttu-id="f72ef-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="f72ef-127">-SyncMemberName</span></span>
<span data-ttu-id="f72ef-128">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="f72ef-128">The sync member name.</span></span>

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

### <span data-ttu-id="f72ef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f72ef-129">-Confirm</span></span>
<span data-ttu-id="f72ef-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f72ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72ef-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f72ef-131">-WhatIf</span></span>
<span data-ttu-id="f72ef-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f72ef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f72ef-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72ef-134">CommonParameters</span></span>
<span data-ttu-id="f72ef-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72ef-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f72ef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72ef-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f72ef-137">INPUTS</span></span>

### <span data-ttu-id="f72ef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f72ef-138">System.String</span></span>

## <span data-ttu-id="f72ef-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f72ef-139">OUTPUTS</span></span>

### <span data-ttu-id="f72ef-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="f72ef-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f72ef-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f72ef-141">NOTES</span></span>

## <span data-ttu-id="f72ef-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f72ef-142">RELATED LINKS</span></span>

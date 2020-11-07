---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: a78e22c66e5099ec3987fb98d1b354906c11a8d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664146"
---
# <span data-ttu-id="75b64-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="75b64-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="75b64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75b64-102">SYNOPSIS</span></span>
<span data-ttu-id="75b64-103">Aktualisieren Sie das Synchronisierungs Schema für eine Synchronisierungs Mitglieder-Datenbank oder eine Synchronisierungs-Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75b64-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="75b64-104">Sie erhält das aktuelle Datenbankschema aus der realen Datenbank und verwendet Sie dann, um das von der Synchronisierungs-Metadaten-Datenbank zwischengespeicherte Schema zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="75b64-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="75b64-105">Wenn "SyncMemberName" angegeben ist, wird das Mitgliedsdaten Bank Schema aktualisiert; Wenn dies nicht der Fall ist, wird das Hub-Datenbankschema aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75b64-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b64-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b64-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b64-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75b64-107">DESCRIPTION</span></span>
<span data-ttu-id="75b64-108">Das Cmdlet **Update-AzureRmSqlSyncSchema** aktualisiert das Synchronisierungs Schema für eine Synchronisierungs Mitglieder-Datenbank oder eine Synchronisierungs-Hub-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75b64-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="75b64-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75b64-109">EXAMPLES</span></span>

### <span data-ttu-id="75b64-110">Beispiel 1: Aktualisieren des Synchronisierungsschemas für eine Hub-Datenbank</span><span class="sxs-lookup"><span data-stu-id="75b64-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="75b64-111">Dieser Befehl aktualisiert das Synchronisierungs Schema für die Hub-Datenbank in der Synchronisierungsgruppe syncGroup01</span><span class="sxs-lookup"><span data-stu-id="75b64-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="75b64-112">Beispiel 2: Aktualisieren des Synchronisierungsschemas für eine Mitgliedsdatenbank</span><span class="sxs-lookup"><span data-stu-id="75b64-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="75b64-113">Mit diesem Befehl wird das Synchronisierungs Schema für die Mitgliedsdatenbank in der Synchronisierungs Member-syncMember01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75b64-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="75b64-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b64-114">PARAMETERS</span></span>

### <span data-ttu-id="75b64-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75b64-115">-DatabaseName</span></span>
<span data-ttu-id="75b64-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75b64-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="75b64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b64-117">-DefaultProfile</span></span>
<span data-ttu-id="75b64-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75b64-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b64-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75b64-119">-PassThru</span></span>
<span data-ttu-id="75b64-120">Definiert, ob die Synchronisierungsgruppe, für die dieses Cmdlet verwendet wird, zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="75b64-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b64-121">-ResourceGroupName</span></span>
<span data-ttu-id="75b64-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75b64-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="75b64-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="75b64-123">-ServerName</span></span>
<span data-ttu-id="75b64-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75b64-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="75b64-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="75b64-125">-SyncGroupName</span></span>
<span data-ttu-id="75b64-126">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="75b64-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b64-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="75b64-127">-SyncMemberName</span></span>
<span data-ttu-id="75b64-128">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="75b64-128">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b64-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75b64-129">-Confirm</span></span>
<span data-ttu-id="75b64-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75b64-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b64-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b64-131">-WhatIf</span></span>
<span data-ttu-id="75b64-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75b64-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b64-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75b64-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b64-134">CommonParameters</span></span>
<span data-ttu-id="75b64-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b64-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b64-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b64-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75b64-137">INPUTS</span></span>

### <span data-ttu-id="75b64-138">Keine</span><span class="sxs-lookup"><span data-stu-id="75b64-138">None</span></span>
<span data-ttu-id="75b64-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="75b64-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75b64-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75b64-140">OUTPUTS</span></span>

### <span data-ttu-id="75b64-141">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="75b64-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="75b64-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="75b64-142">NOTES</span></span>

## <span data-ttu-id="75b64-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75b64-143">RELATED LINKS</span></span>

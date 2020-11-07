---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665247"
---
# <span data-ttu-id="e7d1f-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7d1f-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e7d1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d1f-103">Entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7d1f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d1f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d1f-106">Das Cmdlet **Remove-AzureRmSqlSyncGroup** entfernt eine Azure SQL-Daten Bank Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e7d1f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7d1f-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d1f-108">Beispiel 1: Entfernen einer Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e7d1f-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="e7d1f-109">Dieser Befehl entfernt die Azure SQL-Daten Bank Synchronisierungsgruppe mit dem Namen syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="e7d1f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7d1f-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d1f-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7d1f-111">-Confirm</span></span>
<span data-ttu-id="e7d1f-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d1f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7d1f-113">-DatabaseName</span></span>
<span data-ttu-id="e7d1f-114">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e7d1f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d1f-115">-Force</span></span>
<span data-ttu-id="e7d1f-116">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="e7d1f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e7d1f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d1f-117">-Name</span></span>
<span data-ttu-id="e7d1f-118">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-118">The sync group name.</span></span>

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

### <span data-ttu-id="e7d1f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7d1f-119">-PassThru</span></span>
<span data-ttu-id="e7d1f-120">Definiert, ob die entfernte Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="e7d1f-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="e7d1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7d1f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7d1f-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="e7d1f-123">-ServerName</span></span>
<span data-ttu-id="e7d1f-124">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e7d1f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d1f-125">-WhatIf</span></span>
<span data-ttu-id="e7d1f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d1f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d1f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d1f-128">-DefaultProfile</span></span>
<span data-ttu-id="e7d1f-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d1f-130">CommonParameters</span></span>
<span data-ttu-id="e7d1f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d1f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d1f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7d1f-133">INPUTS</span></span>

## <span data-ttu-id="e7d1f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7d1f-134">OUTPUTS</span></span>

### <span data-ttu-id="e7d1f-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e7d1f-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e7d1f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7d1f-136">NOTES</span></span>

## <span data-ttu-id="e7d1f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7d1f-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7d1f-138">Neu – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7d1f-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e7d1f-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7d1f-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e7d1f-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e7d1f-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)


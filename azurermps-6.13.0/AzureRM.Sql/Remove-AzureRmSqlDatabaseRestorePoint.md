---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: be4a4f418268d1e2523e13d5a779f911381c7309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499330"
---
# <span data-ttu-id="bd461-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="bd461-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="bd461-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd461-102">SYNOPSIS</span></span>
<span data-ttu-id="bd461-103">Entfernt den angegebenen Wiederherstellungspunkt aus einer SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bd461-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd461-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd461-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd461-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd461-105">DESCRIPTION</span></span>
<span data-ttu-id="bd461-106">Das Cmdlet **Remove-AzureRmSqlDatabaseRestorePoint** entfernt den angegebenen Wiederherstellungspunkt aus der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bd461-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="bd461-107">Dieses Cmdlet wird derzeit vom SQL Server Datawarehouse-Dienst in Azure SQL-Datenbank unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd461-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="bd461-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd461-108">EXAMPLES</span></span>

### <span data-ttu-id="bd461-109">Beispiel 1: entfernt einen Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="bd461-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="bd461-110">Dieser Befehl entfernt einen Wiederherstellungspunkt für die Azure SQL-Datenbank, wobei das Erstellungsdatum angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bd461-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="bd461-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd461-111">PARAMETERS</span></span>

### <span data-ttu-id="bd461-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd461-112">-DatabaseName</span></span>
<span data-ttu-id="bd461-113">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="bd461-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="bd461-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd461-114">-DefaultProfile</span></span>
<span data-ttu-id="bd461-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bd461-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd461-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd461-116">-PassThru</span></span>
<span data-ttu-id="bd461-117">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bd461-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bd461-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd461-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd461-119">Gibt den Namen der Ressourcengruppe an, der die SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bd461-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="bd461-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="bd461-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="bd461-121">Gibt das Erstellungsdatum des Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="bd461-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd461-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="bd461-122">-ServerName</span></span>
<span data-ttu-id="bd461-123">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="bd461-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="bd461-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd461-124">-Confirm</span></span>
<span data-ttu-id="bd461-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd461-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd461-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd461-126">-WhatIf</span></span>
<span data-ttu-id="bd461-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd461-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd461-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd461-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd461-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd461-129">CommonParameters</span></span>
<span data-ttu-id="bd461-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd461-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd461-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd461-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd461-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd461-132">INPUTS</span></span>

### <span data-ttu-id="bd461-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bd461-133">System.DateTime</span></span>

### <span data-ttu-id="bd461-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd461-134">System.String</span></span>

## <span data-ttu-id="bd461-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd461-135">OUTPUTS</span></span>

### <span data-ttu-id="bd461-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="bd461-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="bd461-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd461-137">NOTES</span></span>

## <span data-ttu-id="bd461-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd461-138">RELATED LINKS</span></span>

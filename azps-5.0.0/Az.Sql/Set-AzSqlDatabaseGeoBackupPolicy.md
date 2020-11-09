---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301774"
---
# <span data-ttu-id="d7f1c-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d7f1c-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d7f1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f1c-103">Legt eine Daten Bank Geo-Sicherungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="d7f1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f1c-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7f1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f1c-106">Das Cmdlet " **Set-AzSqlDatabaseGeoBackupPolicy** " legt die für eine Datenbank registrierte Geo-Sicherungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="d7f1c-107">Hierbei handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d7f1c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7f1c-108">EXAMPLES</span></span>

## <span data-ttu-id="d7f1c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f1c-109">PARAMETERS</span></span>

### <span data-ttu-id="d7f1c-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7f1c-110">-DatabaseName</span></span>
<span data-ttu-id="d7f1c-111">Gibt den Namen der Datenbank an, für die dieses Cmdlet die Geo-Sicherungsrichtlinie festlegt.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="d7f1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f1c-112">-DefaultProfile</span></span>
<span data-ttu-id="d7f1c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7f1c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7f1c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f1c-114">-ResourceGroupName</span></span>
<span data-ttu-id="d7f1c-115">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d7f1c-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="d7f1c-116">-ServerName</span></span>
<span data-ttu-id="d7f1c-117">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d7f1c-118">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="d7f1c-118">-State</span></span>
<span data-ttu-id="d7f1c-119">Gibt den Zustand der Geo-Backup-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="d7f1c-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7f1c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7f1c-121">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d7f1c-121">Enabled</span></span> 
- <span data-ttu-id="d7f1c-122">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="d7f1c-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f1c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7f1c-123">-Confirm</span></span>
<span data-ttu-id="d7f1c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7f1c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f1c-125">-WhatIf</span></span>
<span data-ttu-id="d7f1c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f1c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7f1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f1c-128">CommonParameters</span></span>
<span data-ttu-id="d7f1c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f1c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7f1c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f1c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7f1c-131">INPUTS</span></span>

### <span data-ttu-id="d7f1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d7f1c-132">System.String</span></span>

## <span data-ttu-id="d7f1c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7f1c-133">OUTPUTS</span></span>

### <span data-ttu-id="d7f1c-134">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d7f1c-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d7f1c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7f1c-135">NOTES</span></span>

## <span data-ttu-id="d7f1c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7f1c-136">RELATED LINKS</span></span>

[<span data-ttu-id="d7f1c-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d7f1c-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d7f1c-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d7f1c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


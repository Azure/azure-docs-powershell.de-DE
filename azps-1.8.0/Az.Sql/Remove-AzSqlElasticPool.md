---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: b58ec1f76737f34664bdecef38f2b596be3702d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659051"
---
# <span data-ttu-id="6d941-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d941-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="6d941-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d941-102">SYNOPSIS</span></span>
<span data-ttu-id="6d941-103">Löscht einen elastischen datenbankpool.</span><span class="sxs-lookup"><span data-stu-id="6d941-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="6d941-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d941-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d941-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d941-105">DESCRIPTION</span></span>
<span data-ttu-id="6d941-106">Das Cmdlet **Remove-AzSqlElasticPool** löscht einen Azure SQL-Datenbank-Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="6d941-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="6d941-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d941-107">EXAMPLES</span></span>

### <span data-ttu-id="6d941-108">Beispiel 1: Löschen eines elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="6d941-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6d941-109">Dieser Befehl löscht einen elastischen Pool mit dem Namen ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="6d941-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6d941-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d941-110">PARAMETERS</span></span>

### <span data-ttu-id="6d941-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d941-111">-DefaultProfile</span></span>
<span data-ttu-id="6d941-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6d941-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d941-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6d941-113">-ElasticPoolName</span></span>
<span data-ttu-id="6d941-114">Gibt den Namen des elastischen Pools an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="6d941-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d941-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6d941-115">-Force</span></span>
<span data-ttu-id="6d941-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6d941-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d941-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d941-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d941-118">Gibt den Namen der Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6d941-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6d941-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="6d941-119">-ServerName</span></span>
<span data-ttu-id="6d941-120">Gibt den Namen des Servers an, der den elastischen Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="6d941-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6d941-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d941-121">-Confirm</span></span>
<span data-ttu-id="6d941-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d941-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d941-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d941-123">-WhatIf</span></span>
<span data-ttu-id="6d941-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d941-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d941-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d941-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d941-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d941-126">CommonParameters</span></span>
<span data-ttu-id="6d941-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d941-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d941-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d941-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d941-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d941-129">INPUTS</span></span>

### <span data-ttu-id="6d941-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d941-130">System.String</span></span>

## <span data-ttu-id="6d941-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d941-131">OUTPUTS</span></span>

### <span data-ttu-id="6d941-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6d941-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6d941-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d941-133">NOTES</span></span>

## <span data-ttu-id="6d941-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d941-134">RELATED LINKS</span></span>

[<span data-ttu-id="6d941-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d941-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6d941-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6d941-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6d941-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6d941-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6d941-138">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d941-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="6d941-139">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d941-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="6d941-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6d941-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



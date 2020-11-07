---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 61a72691aaaaf9cbdfd4e0706f6ace17d7291851
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659197"
---
# <span data-ttu-id="ddac5-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ddac5-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="ddac5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddac5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddac5-103">Ruft den Status von Vorgängen in einem elastischen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="ddac5-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="ddac5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddac5-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddac5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddac5-105">DESCRIPTION</span></span>
<span data-ttu-id="ddac5-106">Das Cmdlet " **Get-AzSqlElasticPoolActivity** " Ruft den Status von Vorgängen in einem elastischen Pool für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ddac5-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="ddac5-107">Sie können den Status beider Pool Erstellungs-und Konfigurationsupdates sehen.</span><span class="sxs-lookup"><span data-stu-id="ddac5-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="ddac5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddac5-108">EXAMPLES</span></span>

### <span data-ttu-id="ddac5-109">Beispiel 1: Abrufen des Status von Vorgängen für einen elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="ddac5-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ddac5-110">Dieser Befehl ruft den Status der Vorgänge für den elastischen Pool mit dem Namen ElasticPool01 ab.</span><span class="sxs-lookup"><span data-stu-id="ddac5-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="ddac5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddac5-111">PARAMETERS</span></span>

### <span data-ttu-id="ddac5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddac5-112">-DefaultProfile</span></span>
<span data-ttu-id="ddac5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ddac5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddac5-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ddac5-114">-ElasticPoolName</span></span>
<span data-ttu-id="ddac5-115">Gibt den Namen eines elastischen Pools an.</span><span class="sxs-lookup"><span data-stu-id="ddac5-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="ddac5-116">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="ddac5-116">-OperationId</span></span>
<span data-ttu-id="ddac5-117">Die ID des abzurufenden Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ddac5-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddac5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddac5-118">-ResourceGroupName</span></span>
<span data-ttu-id="ddac5-119">Gibt den Namen einer Ressourcengruppe an, der der elastische Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ddac5-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ddac5-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="ddac5-120">-ServerName</span></span>
<span data-ttu-id="ddac5-121">Gibt den Namen eines Servers an, der einen elastischen Pool enthält.</span><span class="sxs-lookup"><span data-stu-id="ddac5-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="ddac5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddac5-122">-Confirm</span></span>
<span data-ttu-id="ddac5-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddac5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddac5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddac5-124">-WhatIf</span></span>
<span data-ttu-id="ddac5-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddac5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddac5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddac5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddac5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddac5-127">CommonParameters</span></span>
<span data-ttu-id="ddac5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddac5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddac5-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddac5-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddac5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddac5-130">INPUTS</span></span>

### <span data-ttu-id="ddac5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ddac5-131">System.String</span></span>

### <span data-ttu-id="ddac5-132">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ddac5-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ddac5-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddac5-133">OUTPUTS</span></span>

### <span data-ttu-id="ddac5-134">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="ddac5-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="ddac5-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddac5-135">NOTES</span></span>

## <span data-ttu-id="ddac5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddac5-136">RELATED LINKS</span></span>

[<span data-ttu-id="ddac5-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddac5-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="ddac5-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ddac5-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="ddac5-139">Neu – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddac5-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ddac5-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddac5-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ddac5-141">Satz-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ddac5-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)



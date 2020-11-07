---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b3a84fc37e747cb54571bc26563789599fac3a7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658962"
---
# <span data-ttu-id="400be-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="400be-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="400be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="400be-102">SYNOPSIS</span></span>
<span data-ttu-id="400be-103">Ändert eine Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="400be-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="400be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="400be-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="400be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="400be-105">DESCRIPTION</span></span>
<span data-ttu-id="400be-106">Das Cmdlet " **Satz-AzSqlServerDisasterRecoveryConfiguration** " ändert eine SQL-Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="400be-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="400be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="400be-107">EXAMPLES</span></span>

## <span data-ttu-id="400be-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="400be-108">PARAMETERS</span></span>

### <span data-ttu-id="400be-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="400be-109">-AllowDataLoss</span></span>
<span data-ttu-id="400be-110">Gibt an, dass der Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="400be-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="400be-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="400be-111">-AsJob</span></span>
<span data-ttu-id="400be-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="400be-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400be-113">-DefaultProfile</span></span>
<span data-ttu-id="400be-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="400be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="400be-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="400be-115">-Failover</span></span>
<span data-ttu-id="400be-116">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="400be-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400be-117">-ResourceGroupName</span></span>
<span data-ttu-id="400be-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="400be-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="400be-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="400be-119">-ServerName</span></span>
<span data-ttu-id="400be-120">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="400be-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="400be-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="400be-121">-VirtualEndpointName</span></span>
<span data-ttu-id="400be-122">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="400be-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400be-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="400be-123">-Confirm</span></span>
<span data-ttu-id="400be-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="400be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="400be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="400be-125">-WhatIf</span></span>
<span data-ttu-id="400be-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="400be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="400be-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="400be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="400be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400be-128">CommonParameters</span></span>
<span data-ttu-id="400be-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="400be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400be-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="400be-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400be-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="400be-131">INPUTS</span></span>

### <span data-ttu-id="400be-132">System. String</span><span class="sxs-lookup"><span data-stu-id="400be-132">System.String</span></span>

## <span data-ttu-id="400be-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="400be-133">OUTPUTS</span></span>

### <span data-ttu-id="400be-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="400be-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="400be-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="400be-135">NOTES</span></span>

## <span data-ttu-id="400be-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="400be-136">RELATED LINKS</span></span>

[<span data-ttu-id="400be-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="400be-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="400be-138">Neu – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="400be-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="400be-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="400be-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="400be-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="400be-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

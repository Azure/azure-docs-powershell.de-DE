---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155201"
---
# <span data-ttu-id="36e96-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e96-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="36e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e96-102">SYNOPSIS</span></span>
<span data-ttu-id="36e96-103">Ändert eine Datenbankserverwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="36e96-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="36e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36e96-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e96-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36e96-105">DESCRIPTION</span></span>
<span data-ttu-id="36e96-106">Das **Cmdlet "Set-AzSqlServerDisasterRecoveryConfiguration"** ändert SQL Datenbankserverwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="36e96-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="36e96-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36e96-107">EXAMPLES</span></span>

## <span data-ttu-id="36e96-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e96-108">PARAMETERS</span></span>

### <span data-ttu-id="36e96-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="36e96-109">-AllowDataLoss</span></span>
<span data-ttu-id="36e96-110">Gibt an, dass der Failovervorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="36e96-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="36e96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36e96-111">-AsJob</span></span>
<span data-ttu-id="36e96-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="36e96-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36e96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e96-113">-DefaultProfile</span></span>
<span data-ttu-id="36e96-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="36e96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e96-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="36e96-115">-Failover</span></span>
<span data-ttu-id="36e96-116">Gibt an, dass es sich bei diesem Vorgang um einen Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="36e96-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="36e96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e96-117">-ResourceGroupName</span></span>
<span data-ttu-id="36e96-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="36e96-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="36e96-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36e96-119">-ServerName</span></span>
<span data-ttu-id="36e96-120">Gibt den Namen eines SQL Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="36e96-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="36e96-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="36e96-121">-VirtualEndpointName</span></span>
<span data-ttu-id="36e96-122">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="36e96-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="36e96-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36e96-123">-Confirm</span></span>
<span data-ttu-id="36e96-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36e96-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e96-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36e96-125">-WhatIf</span></span>
<span data-ttu-id="36e96-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36e96-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e96-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36e96-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e96-128">CommonParameters</span></span>
<span data-ttu-id="36e96-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e96-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e96-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e96-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36e96-131">INPUTS</span></span>

### <span data-ttu-id="36e96-132">System.String</span><span class="sxs-lookup"><span data-stu-id="36e96-132">System.String</span></span>

## <span data-ttu-id="36e96-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36e96-133">OUTPUTS</span></span>

### <span data-ttu-id="36e96-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="36e96-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="36e96-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36e96-135">NOTES</span></span>

## <span data-ttu-id="36e96-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36e96-136">RELATED LINKS</span></span>

[<span data-ttu-id="36e96-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e96-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="36e96-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e96-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="36e96-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="36e96-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="36e96-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="36e96-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

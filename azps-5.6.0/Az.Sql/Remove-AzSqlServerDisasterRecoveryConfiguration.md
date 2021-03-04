---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940971"
---
# <span data-ttu-id="a92eb-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a92eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a92eb-103">Entfernt eine SQL Datenbankserversystemwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a92eb-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a92eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a92eb-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a92eb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a92eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a92eb-106">Das **Cmdlet Remove-AzSqlServerDisasterRecoveryConfiguration** entfernt eine SQL Datenbankserversystemwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a92eb-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a92eb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a92eb-107">EXAMPLES</span></span>

## <span data-ttu-id="a92eb-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a92eb-108">PARAMETERS</span></span>

### <span data-ttu-id="a92eb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92eb-109">-DefaultProfile</span></span>
<span data-ttu-id="a92eb-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a92eb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92eb-111">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a92eb-111">-Force</span></span>
<span data-ttu-id="a92eb-112">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="a92eb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a92eb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92eb-113">-ResourceGroupName</span></span>
<span data-ttu-id="a92eb-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a92eb-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a92eb-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="a92eb-115">-ServerName</span></span>
<span data-ttu-id="a92eb-116">Gibt den Namen eines SQL an.</span><span class="sxs-lookup"><span data-stu-id="a92eb-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="a92eb-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a92eb-117">-VirtualEndpointName</span></span>
<span data-ttu-id="a92eb-118">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="a92eb-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="a92eb-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a92eb-119">-Confirm</span></span>
<span data-ttu-id="a92eb-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a92eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92eb-121">-WhatIf</span></span>
<span data-ttu-id="a92eb-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a92eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92eb-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a92eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92eb-124">CommonParameters</span></span>
<span data-ttu-id="a92eb-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92eb-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a92eb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92eb-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a92eb-127">INPUTS</span></span>

### <span data-ttu-id="a92eb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a92eb-128">System.String</span></span>

## <span data-ttu-id="a92eb-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a92eb-129">OUTPUTS</span></span>

### <span data-ttu-id="a92eb-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="a92eb-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="a92eb-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a92eb-131">NOTES</span></span>

## <span data-ttu-id="a92eb-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a92eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="a92eb-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a92eb-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a92eb-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a92eb-136">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="a92eb-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

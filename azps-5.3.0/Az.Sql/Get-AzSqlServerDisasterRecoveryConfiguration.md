---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470334"
---
# <span data-ttu-id="09956-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="09956-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="09956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09956-102">SYNOPSIS</span></span>
<span data-ttu-id="09956-103">Ruft eine Datenbankserversystemwiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="09956-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="09956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09956-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09956-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09956-105">DESCRIPTION</span></span>
<span data-ttu-id="09956-106">Das **Cmdlet "Get-AzSqlServerDisasterRecoveryConfiguration"** ruft SQL Wiederherstellungskonfiguration des Datenbankserversystems ab.</span><span class="sxs-lookup"><span data-stu-id="09956-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="09956-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09956-107">EXAMPLES</span></span>

## <span data-ttu-id="09956-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09956-108">PARAMETERS</span></span>

### <span data-ttu-id="09956-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09956-109">-DefaultProfile</span></span>
<span data-ttu-id="09956-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="09956-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09956-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09956-111">-ResourceGroupName</span></span>
<span data-ttu-id="09956-112">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="09956-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="09956-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09956-113">-ServerName</span></span>
<span data-ttu-id="09956-114">Gibt den Namen SQL Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="09956-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="09956-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="09956-115">-VirtualEndpointName</span></span>
<span data-ttu-id="09956-116">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="09956-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09956-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09956-117">-Confirm</span></span>
<span data-ttu-id="09956-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09956-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09956-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09956-119">-WhatIf</span></span>
<span data-ttu-id="09956-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09956-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09956-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09956-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09956-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09956-122">CommonParameters</span></span>
<span data-ttu-id="09956-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09956-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09956-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09956-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09956-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09956-125">INPUTS</span></span>

### <span data-ttu-id="09956-126">System.String</span><span class="sxs-lookup"><span data-stu-id="09956-126">System.String</span></span>

## <span data-ttu-id="09956-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09956-127">OUTPUTS</span></span>

### <span data-ttu-id="09956-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="09956-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="09956-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09956-129">NOTES</span></span>

## <span data-ttu-id="09956-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09956-130">RELATED LINKS</span></span>

[<span data-ttu-id="09956-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="09956-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09956-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="09956-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09956-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="09956-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="09956-134">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="09956-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


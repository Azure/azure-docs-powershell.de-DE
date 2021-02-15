---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145612"
---
# <span data-ttu-id="c9946-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9946-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="c9946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9946-102">SYNOPSIS</span></span>
<span data-ttu-id="c9946-103">Erstellt eine Datenbankserversystemwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c9946-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="c9946-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9946-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9946-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9946-105">DESCRIPTION</span></span>
<span data-ttu-id="c9946-106">Das **Cmdlet "New-AzSqlServerDisasterRecoveryConfiguration"** erstellt SQL Wiederherstellungskonfiguration des Datenbankserversystems.</span><span class="sxs-lookup"><span data-stu-id="c9946-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c9946-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9946-107">EXAMPLES</span></span>

## <span data-ttu-id="c9946-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9946-108">PARAMETERS</span></span>

### <span data-ttu-id="c9946-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9946-109">-AsJob</span></span>
<span data-ttu-id="c9946-110">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c9946-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9946-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9946-111">-DefaultProfile</span></span>
<span data-ttu-id="c9946-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c9946-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9946-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c9946-113">-FailoverPolicy</span></span>
<span data-ttu-id="c9946-114">Gibt die Failoverrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="c9946-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="c9946-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9946-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c9946-116">Gibt den Namen der Partnerressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9946-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="c9946-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c9946-117">-PartnerServerName</span></span>
<span data-ttu-id="c9946-118">Gibt den Namen des Partnerservers an.</span><span class="sxs-lookup"><span data-stu-id="c9946-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="c9946-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9946-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9946-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c9946-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c9946-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9946-121">-ServerName</span></span>
<span data-ttu-id="c9946-122">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="c9946-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c9946-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="c9946-123">-VirtualEndpointName</span></span>
<span data-ttu-id="c9946-124">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="c9946-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="c9946-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9946-125">-Confirm</span></span>
<span data-ttu-id="c9946-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9946-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9946-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c9946-127">-WhatIf</span></span>
<span data-ttu-id="c9946-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9946-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9946-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9946-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9946-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9946-130">CommonParameters</span></span>
<span data-ttu-id="c9946-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9946-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9946-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9946-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9946-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9946-133">INPUTS</span></span>

### <span data-ttu-id="c9946-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c9946-134">System.String</span></span>

## <span data-ttu-id="c9946-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9946-135">OUTPUTS</span></span>

### <span data-ttu-id="c9946-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="c9946-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="c9946-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c9946-137">NOTES</span></span>

## <span data-ttu-id="c9946-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c9946-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9946-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9946-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c9946-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9946-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c9946-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9946-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c9946-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c9946-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

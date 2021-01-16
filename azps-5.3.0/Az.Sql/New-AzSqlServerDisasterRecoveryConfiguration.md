---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460683"
---
# <span data-ttu-id="7805a-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7805a-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="7805a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7805a-102">SYNOPSIS</span></span>
<span data-ttu-id="7805a-103">Erstellt eine Datenbankserversystemwiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7805a-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="7805a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7805a-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7805a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7805a-105">DESCRIPTION</span></span>
<span data-ttu-id="7805a-106">Das **Cmdlet "New-AzSqlServerDisasterRecoveryConfiguration"** erstellt SQL Wiederherstellungskonfiguration des Datenbankserversystems.</span><span class="sxs-lookup"><span data-stu-id="7805a-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="7805a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7805a-107">EXAMPLES</span></span>

## <span data-ttu-id="7805a-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7805a-108">PARAMETERS</span></span>

### <span data-ttu-id="7805a-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7805a-109">-AsJob</span></span>
<span data-ttu-id="7805a-110">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7805a-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7805a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7805a-111">-DefaultProfile</span></span>
<span data-ttu-id="7805a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7805a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7805a-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7805a-113">-FailoverPolicy</span></span>
<span data-ttu-id="7805a-114">Gibt die Failoverrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7805a-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="7805a-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7805a-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7805a-116">Gibt den Namen der Partnerressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7805a-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="7805a-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="7805a-117">-PartnerServerName</span></span>
<span data-ttu-id="7805a-118">Gibt den Namen des Partnerservers an.</span><span class="sxs-lookup"><span data-stu-id="7805a-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="7805a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7805a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7805a-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7805a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7805a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7805a-121">-ServerName</span></span>
<span data-ttu-id="7805a-122">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="7805a-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7805a-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="7805a-123">-VirtualEndpointName</span></span>
<span data-ttu-id="7805a-124">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="7805a-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="7805a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7805a-125">-Confirm</span></span>
<span data-ttu-id="7805a-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7805a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7805a-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7805a-127">-WhatIf</span></span>
<span data-ttu-id="7805a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7805a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7805a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7805a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7805a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7805a-130">CommonParameters</span></span>
<span data-ttu-id="7805a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7805a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7805a-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7805a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7805a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7805a-133">INPUTS</span></span>

### <span data-ttu-id="7805a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7805a-134">System.String</span></span>

## <span data-ttu-id="7805a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7805a-135">OUTPUTS</span></span>

### <span data-ttu-id="7805a-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="7805a-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="7805a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7805a-137">NOTES</span></span>

## <span data-ttu-id="7805a-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7805a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7805a-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7805a-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7805a-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7805a-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7805a-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7805a-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7805a-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="7805a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

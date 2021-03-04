---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 07065c18b9e06f75863ddd41f8a6f0155a3699f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926307"
---
# <span data-ttu-id="00e94-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="00e94-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="00e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e94-102">SYNOPSIS</span></span>
<span data-ttu-id="00e94-103">Entfernt Azure SQL Server DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="00e94-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="00e94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00e94-104">SYNTAX</span></span>

### <span data-ttu-id="00e94-105">Entfernen eines Server-Dns-Alias aus cmdlet-Eingabeparametern</span><span class="sxs-lookup"><span data-stu-id="00e94-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e94-106">Entfernen eines Server-Dns-Alias aus der AzureSqlServerDnsAliasModel-Instanzdefinition</span><span class="sxs-lookup"><span data-stu-id="00e94-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e94-107">Entfernen eines Server-Dns-Alias aus einer Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="00e94-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e94-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00e94-108">DESCRIPTION</span></span>
<span data-ttu-id="00e94-109">Mit diesen Befehlen wird azure SQL Server DNS-Alias vom Server entfernt, und der Server bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="00e94-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="00e94-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00e94-110">EXAMPLES</span></span>

### <span data-ttu-id="00e94-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00e94-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="00e94-112">Entfernt Azure SQL Server-DNS-Alias mit dem NamenaliasName vom Server mit dem Namenservername</span><span class="sxs-lookup"><span data-stu-id="00e94-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="00e94-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="00e94-113">PARAMETERS</span></span>

### <span data-ttu-id="00e94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00e94-114">-AsJob</span></span>
<span data-ttu-id="00e94-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="00e94-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00e94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e94-116">-DefaultProfile</span></span>
<span data-ttu-id="00e94-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00e94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00e94-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="00e94-118">-Force</span></span>
<span data-ttu-id="00e94-119">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="00e94-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="00e94-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00e94-120">-InputObject</span></span>
<span data-ttu-id="00e94-121">Das zu entfernende Server-Dns-Alias-Objekt</span><span class="sxs-lookup"><span data-stu-id="00e94-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-122">-Name</span><span class="sxs-lookup"><span data-stu-id="00e94-122">-Name</span></span>
<span data-ttu-id="00e94-123">Azure Sql Server Dns Aliasname</span><span class="sxs-lookup"><span data-stu-id="00e94-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e94-124">-ResourceGroupName</span></span>
<span data-ttu-id="00e94-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="00e94-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00e94-126">-ResourceId</span></span>
<span data-ttu-id="00e94-127">Die Ressourcen-ID des zu entfernende Server Dns Alias-Objekts</span><span class="sxs-lookup"><span data-stu-id="00e94-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="00e94-128">-ServerName</span></span>
<span data-ttu-id="00e94-129">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="00e94-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00e94-130">-Confirm</span></span>
<span data-ttu-id="00e94-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00e94-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e94-132">-WhatIf</span></span>
<span data-ttu-id="00e94-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00e94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00e94-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00e94-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e94-135">CommonParameters</span></span>
<span data-ttu-id="00e94-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e94-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00e94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e94-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00e94-138">INPUTS</span></span>

### <span data-ttu-id="00e94-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="00e94-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="00e94-140">System.String</span><span class="sxs-lookup"><span data-stu-id="00e94-140">System.String</span></span>

## <span data-ttu-id="00e94-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00e94-141">OUTPUTS</span></span>

### <span data-ttu-id="00e94-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="00e94-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="00e94-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="00e94-143">NOTES</span></span>

## <span data-ttu-id="00e94-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="00e94-144">RELATED LINKS</span></span>

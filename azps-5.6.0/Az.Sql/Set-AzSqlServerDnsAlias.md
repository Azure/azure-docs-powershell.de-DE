---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: bbc941c260579fb7fdb437f0b30002999635b8eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927704"
---
# <span data-ttu-id="51cc8-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="51cc8-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="51cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="51cc8-103">Ändert den Server, auf den Azure SQL Server -DNS-Alias verweisen</span><span class="sxs-lookup"><span data-stu-id="51cc8-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="51cc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51cc8-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51cc8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="51cc8-106">Mit diesem Befehl wird der Server aktualisiert, auf den der Alias verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="51cc8-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="51cc8-107">Dieser Befehl muss ausgegeben werden, während er beim Abonnement angemeldet ist, auf dem sich der neue Server befindet, auf den der Alias verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="51cc8-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="51cc8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51cc8-108">EXAMPLES</span></span>

### <span data-ttu-id="51cc8-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51cc8-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="51cc8-110">Dieser Befehl aktualisiert den Alias, der zuvor auf "oldServer" zeigte, um auf "server newServer" zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="51cc8-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="51cc8-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="51cc8-111">PARAMETERS</span></span>

### <span data-ttu-id="51cc8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51cc8-112">-AsJob</span></span>
<span data-ttu-id="51cc8-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="51cc8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51cc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cc8-114">-DefaultProfile</span></span>
<span data-ttu-id="51cc8-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cc8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51cc8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="51cc8-116">-Name</span></span>
<span data-ttu-id="51cc8-117">Der Azure Sql Server-Dns-Aliasname.</span><span class="sxs-lookup"><span data-stu-id="51cc8-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51cc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="51cc8-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51cc8-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cc8-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="51cc8-120">-SourceServerName</span></span>
<span data-ttu-id="51cc8-121">Der Name von Azure Sql Server, auf den der Alias derzeit verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="51cc8-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="51cc8-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51cc8-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="51cc8-123">Der Name der Ressourcengruppe des Quellservers.</span><span class="sxs-lookup"><span data-stu-id="51cc8-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="51cc8-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51cc8-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="51cc8-125">Die Abonnement-ID des Quellservers</span><span class="sxs-lookup"><span data-stu-id="51cc8-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cc8-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="51cc8-126">-TargetServerName</span></span>
<span data-ttu-id="51cc8-127">Der Name von Azure Sql Server, auf den der Alias verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="51cc8-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="51cc8-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51cc8-128">-Confirm</span></span>
<span data-ttu-id="51cc8-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51cc8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51cc8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cc8-130">-WhatIf</span></span>
<span data-ttu-id="51cc8-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51cc8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51cc8-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51cc8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51cc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cc8-133">CommonParameters</span></span>
<span data-ttu-id="51cc8-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cc8-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51cc8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cc8-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51cc8-136">INPUTS</span></span>

### <span data-ttu-id="51cc8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="51cc8-137">System.String</span></span>

## <span data-ttu-id="51cc8-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51cc8-138">OUTPUTS</span></span>

### <span data-ttu-id="51cc8-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="51cc8-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="51cc8-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="51cc8-140">NOTES</span></span>

## <span data-ttu-id="51cc8-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="51cc8-141">RELATED LINKS</span></span>

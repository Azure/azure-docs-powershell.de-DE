---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300453"
---
# <span data-ttu-id="3a4cc-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="3a4cc-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="3a4cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4cc-103">Ändert den Server, auf den der Azure SQL Server-DNS-Alias zeigt</span><span class="sxs-lookup"><span data-stu-id="3a4cc-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="3a4cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a4cc-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4cc-106">Mit diesem Befehl wird der Server aktualisiert, auf den Alias verweist.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="3a4cc-107">Dieser Befehl muss während des Anmelde Abonnements ausgestellt werden, wenn sich der neue Server, auf den der Alias verweist, befindet.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="3a4cc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a4cc-108">EXAMPLES</span></span>

### <span data-ttu-id="3a4cc-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a4cc-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="3a4cc-110">Dieser Befehl aktualisiert Alias, der zuvor auf oldServer verweist, um auf Server-Server-Server zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="3a4cc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a4cc-111">PARAMETERS</span></span>

### <span data-ttu-id="3a4cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a4cc-112">-AsJob</span></span>
<span data-ttu-id="3a4cc-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3a4cc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a4cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4cc-114">-DefaultProfile</span></span>
<span data-ttu-id="3a4cc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a4cc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3a4cc-116">-Name</span></span>
<span data-ttu-id="3a4cc-117">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="3a4cc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4cc-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a4cc-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a4cc-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="3a4cc-120">-SourceServerName</span></span>
<span data-ttu-id="3a4cc-121">Der Name des Azure SQL-Servers, auf den Alias aktuell zeigt.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="3a4cc-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4cc-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="3a4cc-123">Der Name der Ressourcengruppe des Quellservers.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="3a4cc-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a4cc-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="3a4cc-125">Die Abonnement-ID des Quellservers</span><span class="sxs-lookup"><span data-stu-id="3a4cc-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="3a4cc-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="3a4cc-126">-TargetServerName</span></span>
<span data-ttu-id="3a4cc-127">Der Name des Azure SQL Server, auf den der Alias verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="3a4cc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a4cc-128">-Confirm</span></span>
<span data-ttu-id="3a4cc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4cc-130">-WhatIf</span></span>
<span data-ttu-id="3a4cc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4cc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4cc-133">CommonParameters</span></span>
<span data-ttu-id="3a4cc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4cc-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a4cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4cc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a4cc-136">INPUTS</span></span>

### <span data-ttu-id="3a4cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3a4cc-137">System.String</span></span>

## <span data-ttu-id="3a4cc-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a4cc-138">OUTPUTS</span></span>

### <span data-ttu-id="3a4cc-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="3a4cc-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="3a4cc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a4cc-140">NOTES</span></span>

## <span data-ttu-id="3a4cc-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a4cc-141">RELATED LINKS</span></span>

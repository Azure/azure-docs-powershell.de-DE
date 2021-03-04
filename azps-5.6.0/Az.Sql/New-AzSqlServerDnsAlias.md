---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920219"
---
# <span data-ttu-id="8bf62-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="8bf62-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="8bf62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bf62-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf62-103">Mit diesem Befehl wird ein neuer Azure SQL Server-DNS-Alias erstellt.</span><span class="sxs-lookup"><span data-stu-id="8bf62-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="8bf62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bf62-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bf62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bf62-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf62-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="8bf62-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="8bf62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bf62-107">EXAMPLES</span></span>

### <span data-ttu-id="8bf62-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8bf62-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="8bf62-109">Mit diesem Befehl wird Azure SQL Server-DNS-Alias mit dem NamenaliasName erstellt, der auf Serverservername verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="8bf62-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="8bf62-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8bf62-110">PARAMETERS</span></span>

### <span data-ttu-id="8bf62-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bf62-111">-AsJob</span></span>
<span data-ttu-id="8bf62-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8bf62-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bf62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf62-113">-DefaultProfile</span></span>
<span data-ttu-id="8bf62-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bf62-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf62-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8bf62-115">-Name</span></span>
<span data-ttu-id="8bf62-116">Der Azure Sql Server-Dns-Aliasname.</span><span class="sxs-lookup"><span data-stu-id="8bf62-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bf62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf62-117">-ResourceGroupName</span></span>
<span data-ttu-id="8bf62-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8bf62-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8bf62-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="8bf62-119">-ServerName</span></span>
<span data-ttu-id="8bf62-120">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="8bf62-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8bf62-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bf62-121">-Confirm</span></span>
<span data-ttu-id="8bf62-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bf62-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf62-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf62-123">-WhatIf</span></span>
<span data-ttu-id="8bf62-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bf62-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf62-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bf62-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf62-126">CommonParameters</span></span>
<span data-ttu-id="8bf62-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf62-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bf62-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf62-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bf62-129">INPUTS</span></span>

### <span data-ttu-id="8bf62-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8bf62-130">System.String</span></span>

## <span data-ttu-id="8bf62-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bf62-131">OUTPUTS</span></span>

### <span data-ttu-id="8bf62-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="8bf62-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="8bf62-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8bf62-133">NOTES</span></span>

## <span data-ttu-id="8bf62-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8bf62-134">RELATED LINKS</span></span>

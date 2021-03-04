---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931656"
---
# <span data-ttu-id="b61f7-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b61f7-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="b61f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b61f7-103">Ruft Azure SQL Server-DNS-Alias ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="b61f7-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="b61f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b61f7-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b61f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b61f7-105">DESCRIPTION</span></span>
<span data-ttu-id="b61f7-106">Holen Sie sich den spezifischen Azure SQL Server-DNS-Alias oder listet alle Server-DNS-Aliase für den Server auf.</span><span class="sxs-lookup"><span data-stu-id="b61f7-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="b61f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b61f7-107">EXAMPLES</span></span>

### <span data-ttu-id="b61f7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b61f7-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="b61f7-109">Listet alle Server-DNS-Aliase für den jeweiligen Server auf.</span><span class="sxs-lookup"><span data-stu-id="b61f7-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="b61f7-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b61f7-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="b61f7-111">Ruft server-DNS-Alias ab, der durch den Server- und Aliasnamen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b61f7-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="b61f7-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b61f7-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="b61f7-113">Listet alle Server-DNS-Aliase für den bestimmten Server auf, die mit "dnsaliasname" beginnen.</span><span class="sxs-lookup"><span data-stu-id="b61f7-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="b61f7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b61f7-114">PARAMETERS</span></span>

### <span data-ttu-id="b61f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61f7-115">-DefaultProfile</span></span>
<span data-ttu-id="b61f7-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b61f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b61f7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b61f7-117">-Name</span></span>
<span data-ttu-id="b61f7-118">Der Azure Sql Server-DNS-Aliasname.</span><span class="sxs-lookup"><span data-stu-id="b61f7-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="b61f7-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b61f7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b61f7-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="b61f7-121">-ServerName</span></span>
<span data-ttu-id="b61f7-122">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="b61f7-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b61f7-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b61f7-123">-Confirm</span></span>
<span data-ttu-id="b61f7-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b61f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61f7-125">-WhatIf</span></span>
<span data-ttu-id="b61f7-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b61f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61f7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b61f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61f7-128">CommonParameters</span></span>
<span data-ttu-id="b61f7-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61f7-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b61f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61f7-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b61f7-131">INPUTS</span></span>

### <span data-ttu-id="b61f7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b61f7-132">System.String</span></span>

## <span data-ttu-id="b61f7-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b61f7-133">OUTPUTS</span></span>

### <span data-ttu-id="b61f7-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b61f7-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b61f7-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b61f7-135">NOTES</span></span>

## <span data-ttu-id="b61f7-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b61f7-136">RELATED LINKS</span></span>

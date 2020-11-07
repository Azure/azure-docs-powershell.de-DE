---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 516fd126b1015bca23c34a4eb295a03752e836f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826068"
---
# <span data-ttu-id="c5d2a-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c5d2a-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="c5d2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d2a-103">Ruft den Azure SQL Server-DNS-Alias ab oder listet ihn auf.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="c5d2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d2a-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5d2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d2a-106">Abrufen des bestimmten Azure SQL Server-DNS-Alias oder Auflisten aller Server-DNS-Aliase für den Server</span><span class="sxs-lookup"><span data-stu-id="c5d2a-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="c5d2a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5d2a-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d2a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5d2a-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c5d2a-109">Listet alle Server-DNS-Aliase für den jeweiligen Server auf</span><span class="sxs-lookup"><span data-stu-id="c5d2a-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="c5d2a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5d2a-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c5d2a-111">Ruft den Server-DNS-Alias ab, der vom Server und Aliasnamen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="c5d2a-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c5d2a-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c5d2a-113">Listet alle Server-DNS-Aliase für den jeweiligen Server auf, die mit "dnsaliasname" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="c5d2a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5d2a-114">PARAMETERS</span></span>

### <span data-ttu-id="c5d2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d2a-115">-DefaultProfile</span></span>
<span data-ttu-id="c5d2a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5d2a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c5d2a-117">-Name</span></span>
<span data-ttu-id="c5d2a-118">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c5d2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5d2a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5d2a-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="c5d2a-121">-ServerName</span></span>
<span data-ttu-id="c5d2a-122">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c5d2a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5d2a-123">-Confirm</span></span>
<span data-ttu-id="c5d2a-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d2a-125">-WhatIf</span></span>
<span data-ttu-id="c5d2a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d2a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d2a-128">CommonParameters</span></span>
<span data-ttu-id="c5d2a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d2a-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5d2a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d2a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5d2a-131">INPUTS</span></span>

### <span data-ttu-id="c5d2a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d2a-132">System.String</span></span>

## <span data-ttu-id="c5d2a-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5d2a-133">OUTPUTS</span></span>

### <span data-ttu-id="c5d2a-134">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="c5d2a-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c5d2a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5d2a-135">NOTES</span></span>

## <span data-ttu-id="c5d2a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5d2a-136">RELATED LINKS</span></span>

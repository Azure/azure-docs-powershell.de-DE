---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659085"
---
# <span data-ttu-id="2a53d-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="2a53d-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="2a53d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a53d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a53d-103">Dieser Befehl erstellt einen neuen Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="2a53d-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="2a53d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a53d-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a53d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a53d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a53d-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweist.</span><span class="sxs-lookup"><span data-stu-id="2a53d-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="2a53d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a53d-107">EXAMPLES</span></span>

### <span data-ttu-id="2a53d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a53d-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="2a53d-109">Dieser Befehl erstellt einen Azure SQL Server-DNS-Alias mit dem Namen Aliasname, der auf Server Name verweist.</span><span class="sxs-lookup"><span data-stu-id="2a53d-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="2a53d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a53d-110">PARAMETERS</span></span>

### <span data-ttu-id="2a53d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a53d-111">-AsJob</span></span>
<span data-ttu-id="2a53d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2a53d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a53d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a53d-113">-DefaultProfile</span></span>
<span data-ttu-id="2a53d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a53d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a53d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2a53d-115">-Name</span></span>
<span data-ttu-id="2a53d-116">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="2a53d-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="2a53d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a53d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a53d-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a53d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a53d-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="2a53d-119">-ServerName</span></span>
<span data-ttu-id="2a53d-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="2a53d-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2a53d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a53d-121">-Confirm</span></span>
<span data-ttu-id="2a53d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a53d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a53d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a53d-123">-WhatIf</span></span>
<span data-ttu-id="2a53d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a53d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a53d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a53d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a53d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a53d-126">CommonParameters</span></span>
<span data-ttu-id="2a53d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a53d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a53d-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a53d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a53d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a53d-129">INPUTS</span></span>

### <span data-ttu-id="2a53d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2a53d-130">System.String</span></span>

## <span data-ttu-id="2a53d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a53d-131">OUTPUTS</span></span>

### <span data-ttu-id="2a53d-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="2a53d-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="2a53d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a53d-133">NOTES</span></span>

## <span data-ttu-id="2a53d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a53d-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498725"
---
# <span data-ttu-id="0352c-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0352c-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="0352c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0352c-102">SYNOPSIS</span></span>
<span data-ttu-id="0352c-103">Dieser Befehl erstellt einen neuen Azure SQL Server-DNS-Alias.</span><span class="sxs-lookup"><span data-stu-id="0352c-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0352c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0352c-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0352c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0352c-105">DESCRIPTION</span></span>
<span data-ttu-id="0352c-106">Erstellt einen neuen Azure SQL Server-DNS-Alias, der auf den angegebenen Server verweist.</span><span class="sxs-lookup"><span data-stu-id="0352c-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="0352c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0352c-107">EXAMPLES</span></span>

### <span data-ttu-id="0352c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0352c-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="0352c-109">Dieser Befehl erstellt einen Azure SQL Server-DNS-Alias mit dem Namen Aliasname, der auf Server Name verweist.</span><span class="sxs-lookup"><span data-stu-id="0352c-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="0352c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0352c-110">PARAMETERS</span></span>

### <span data-ttu-id="0352c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0352c-111">-AsJob</span></span>
<span data-ttu-id="0352c-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0352c-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0352c-113">-DefaultProfile</span></span>
<span data-ttu-id="0352c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0352c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0352c-115">-Name</span></span>
<span data-ttu-id="0352c-116">Der Azure SQL Server-DNS-Alias Name.</span><span class="sxs-lookup"><span data-stu-id="0352c-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0352c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0352c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0352c-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="0352c-119">-ServerName</span></span>
<span data-ttu-id="0352c-120">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="0352c-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0352c-121">-Confirm</span></span>
<span data-ttu-id="0352c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0352c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0352c-123">-WhatIf</span></span>
<span data-ttu-id="0352c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0352c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0352c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0352c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0352c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0352c-126">CommonParameters</span></span>
<span data-ttu-id="0352c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0352c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0352c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0352c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0352c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0352c-129">INPUTS</span></span>

### <span data-ttu-id="0352c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0352c-130">System.String</span></span>

## <span data-ttu-id="0352c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0352c-131">OUTPUTS</span></span>

### <span data-ttu-id="0352c-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="0352c-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0352c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0352c-133">NOTES</span></span>

## <span data-ttu-id="0352c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0352c-134">RELATED LINKS</span></span>

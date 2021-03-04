---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 79d920f866991cae15e2da08d03e2eecd4d2e91e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927499"
---
# <span data-ttu-id="dd609-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dd609-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="dd609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd609-102">SYNOPSIS</span></span>
<span data-ttu-id="dd609-103">Erstellt eine Kommunikationsverbindung für flexible Datenbanktransaktionen zwischen zwei SQL Datenbankservern.</span><span class="sxs-lookup"><span data-stu-id="dd609-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="dd609-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd609-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd609-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd609-105">DESCRIPTION</span></span>
<span data-ttu-id="dd609-106">Das **Cmdlet New-AzSqlServerCommunicationLink** erstellt eine Kommunikationsverbindung für flexible Datenbanktransaktionen zwischen zwei logischen Servern in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dd609-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="dd609-107">Flexible Datenbanktransaktionen können Datenbanken auf einem der gekoppelten Server umfassen.</span><span class="sxs-lookup"><span data-stu-id="dd609-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="dd609-108">Sie können mehrere Links auf einem Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd609-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="dd609-109">Daher können sich transaktionen mit flexiblen Datenbanken über eine größere Anzahl von Servern erstreckt haben.</span><span class="sxs-lookup"><span data-stu-id="dd609-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="dd609-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd609-110">EXAMPLES</span></span>

### <span data-ttu-id="dd609-111">Beispiel 1: Erstellen eines Kommunikationslinks</span><span class="sxs-lookup"><span data-stu-id="dd609-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="dd609-112">Mit diesem Befehl wird ein Link mit dem Namen Link01 zwischen ContosoServer17 und ContosoServer02 erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd609-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="dd609-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd609-113">PARAMETERS</span></span>

### <span data-ttu-id="dd609-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd609-114">-AsJob</span></span>
<span data-ttu-id="dd609-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dd609-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd609-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd609-116">-DefaultProfile</span></span>
<span data-ttu-id="dd609-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dd609-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd609-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="dd609-118">-LinkName</span></span>
<span data-ttu-id="dd609-119">Gibt den Namen des Serverkommunikationslinks an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd609-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dd609-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="dd609-120">-PartnerServer</span></span>
<span data-ttu-id="dd609-121">Gibt den Namen des anderen Servers an, der an diesem Kommunikationslink teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="dd609-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="dd609-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd609-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd609-123">Gibt den Namen der Ressourcengruppe an, zu der der vom *Parameter ServerName angegebene Server* gehört.</span><span class="sxs-lookup"><span data-stu-id="dd609-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="dd609-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="dd609-124">-ServerName</span></span>
<span data-ttu-id="dd609-125">Gibt den Namen des Servers an, auf dem dieses Cmdlet den Kommunikationslink eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="dd609-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="dd609-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd609-126">-Confirm</span></span>
<span data-ttu-id="dd609-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd609-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd609-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd609-128">-WhatIf</span></span>
<span data-ttu-id="dd609-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd609-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd609-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd609-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd609-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd609-131">CommonParameters</span></span>
<span data-ttu-id="dd609-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd609-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd609-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd609-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd609-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd609-134">INPUTS</span></span>

### <span data-ttu-id="dd609-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dd609-135">System.String</span></span>

## <span data-ttu-id="dd609-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd609-136">OUTPUTS</span></span>

### <span data-ttu-id="dd609-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="dd609-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="dd609-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd609-138">NOTES</span></span>
* <span data-ttu-id="dd609-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="dd609-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dd609-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd609-140">RELATED LINKS</span></span>

[<span data-ttu-id="dd609-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dd609-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dd609-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dd609-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dd609-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="dd609-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

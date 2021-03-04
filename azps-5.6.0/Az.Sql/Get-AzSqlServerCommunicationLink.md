---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 20f0fe00486b6b81ec1600e518c42121f5369095
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933651"
---
# <span data-ttu-id="13a5e-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a5e-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="13a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="13a5e-103">Ruft Kommunikationslinks für flexible Datenbanktransaktionen zwischen Datenbankservern ab.</span><span class="sxs-lookup"><span data-stu-id="13a5e-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="13a5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13a5e-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="13a5e-106">Das **Get-AzSqlServerCommunicationLink-Cmdlet** ruft Server-zu-Server-Kommunikationslinks für flexible Datenbanktransaktionen in Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="13a5e-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="13a5e-107">Geben Sie den Namen eines Serverkommunikationslinks an, um die Eigenschaften für diesen Link zu sehen.</span><span class="sxs-lookup"><span data-stu-id="13a5e-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="13a5e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13a5e-108">EXAMPLES</span></span>

### <span data-ttu-id="13a5e-109">Beispiel 1: Alle Kommunikationslinks für einen Server erhalten</span><span class="sxs-lookup"><span data-stu-id="13a5e-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="13a5e-110">Dieser Befehl ruft alle Server-zu-Server-Kommunikationslinks für flexible Datenbanktransaktionen für den Server namens ContosoServer17 ab.</span><span class="sxs-lookup"><span data-stu-id="13a5e-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="13a5e-111">Beispiel 2: Erhalten eines bestimmten Kommunikationslinks für einen Server</span><span class="sxs-lookup"><span data-stu-id="13a5e-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="13a5e-112">Dieser Befehl ruft den Server-zu-Server-Kommunikationslink mit dem Namen Link01 ab.</span><span class="sxs-lookup"><span data-stu-id="13a5e-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="13a5e-113">Beispiel 3: Erhalten aller Kommunikationslinks für einen Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="13a5e-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="13a5e-114">Dieser Befehl ruft alle Server-zu-Server-Kommunikationslinks für transaktionen mit flexiblen Datenbanken für den Server namens ContosoServer17 ab, der mit "Link" beginnt.</span><span class="sxs-lookup"><span data-stu-id="13a5e-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="13a5e-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13a5e-115">PARAMETERS</span></span>

### <span data-ttu-id="13a5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a5e-116">-DefaultProfile</span></span>
<span data-ttu-id="13a5e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="13a5e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13a5e-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="13a5e-118">-LinkName</span></span>
<span data-ttu-id="13a5e-119">Gibt den Namen des Serverkommunikationslinks an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="13a5e-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="13a5e-121">Gibt den Namen der Ressourcengruppe an, zu der der vom *Parameter ServerName angegebene Server* gehört.</span><span class="sxs-lookup"><span data-stu-id="13a5e-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="13a5e-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="13a5e-122">-ServerName</span></span>
<span data-ttu-id="13a5e-123">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="13a5e-123">Specifies the name of a server.</span></span>
<span data-ttu-id="13a5e-124">Dieser Server enthält einen Kommunikationslink, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="13a5e-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13a5e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13a5e-125">-Confirm</span></span>
<span data-ttu-id="13a5e-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13a5e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a5e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a5e-127">-WhatIf</span></span>
<span data-ttu-id="13a5e-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13a5e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a5e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13a5e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a5e-130">CommonParameters</span></span>
<span data-ttu-id="13a5e-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a5e-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13a5e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a5e-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13a5e-133">INPUTS</span></span>

### <span data-ttu-id="13a5e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="13a5e-134">System.String</span></span>

## <span data-ttu-id="13a5e-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13a5e-135">OUTPUTS</span></span>

### <span data-ttu-id="13a5e-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="13a5e-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="13a5e-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="13a5e-137">NOTES</span></span>
* <span data-ttu-id="13a5e-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="13a5e-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="13a5e-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="13a5e-139">RELATED LINKS</span></span>

[<span data-ttu-id="13a5e-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a5e-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="13a5e-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a5e-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="13a5e-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="13a5e-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

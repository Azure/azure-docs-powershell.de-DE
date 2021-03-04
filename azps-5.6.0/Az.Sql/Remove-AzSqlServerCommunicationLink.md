---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: ed6f1c2a689ed122ac16004b80f2ab0f0ea2ea3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940976"
---
# <span data-ttu-id="b2bd4-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b2bd4-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="b2bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bd4-103">Löscht eine Kommunikationsverbindung für flexible Datenbanktransaktionen zwischen zwei Servern.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="b2bd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2bd4-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2bd4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="b2bd4-106">Das **Cmdlet Remove-AzSqlServerCommunicationLink** löscht einen Server-zu-Server-Kommunikationslink für flexible Datenbanktransaktionen in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="b2bd4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="b2bd4-108">Beispiel 1: Löschen eines Kommunikationslinks</span><span class="sxs-lookup"><span data-stu-id="b2bd4-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="b2bd4-109">Mit diesem Befehl wird ein Server-zu-Server-Kommunikationslink namens Link01 auf ContosoServer17 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="b2bd4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2bd4-110">PARAMETERS</span></span>

### <span data-ttu-id="b2bd4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bd4-111">-DefaultProfile</span></span>
<span data-ttu-id="b2bd4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b2bd4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2bd4-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b2bd4-113">-Force</span></span>
<span data-ttu-id="b2bd4-114">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2bd4-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="b2bd4-115">-LinkName</span></span>
<span data-ttu-id="b2bd4-116">Gibt den Namen des Serverkommunikationslinks an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2bd4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2bd4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2bd4-118">Gibt den Namen der Ressourcengruppe an, zu der der vom *Parameter ServerName angegebene Server* gehört.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="b2bd4-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="b2bd4-119">-ServerName</span></span>
<span data-ttu-id="b2bd4-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-120">Specifies the name of a server.</span></span>
<span data-ttu-id="b2bd4-121">Dieser Server enthält den Kommunikationslink, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b2bd4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2bd4-122">-Confirm</span></span>
<span data-ttu-id="b2bd4-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2bd4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2bd4-124">-WhatIf</span></span>
<span data-ttu-id="b2bd4-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2bd4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2bd4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bd4-127">CommonParameters</span></span>
<span data-ttu-id="b2bd4-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bd4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bd4-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2bd4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bd4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2bd4-130">INPUTS</span></span>

### <span data-ttu-id="b2bd4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b2bd4-131">System.String</span></span>

## <span data-ttu-id="b2bd4-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2bd4-132">OUTPUTS</span></span>

### <span data-ttu-id="b2bd4-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b2bd4-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="b2bd4-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2bd4-134">NOTES</span></span>
* <span data-ttu-id="b2bd4-135">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="b2bd4-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b2bd4-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2bd4-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2bd4-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b2bd4-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b2bd4-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b2bd4-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b2bd4-139">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="b2bd4-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302994"
---
# <span data-ttu-id="061cf-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="061cf-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="061cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="061cf-102">SYNOPSIS</span></span>
<span data-ttu-id="061cf-103">Löscht eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei Servern.</span><span class="sxs-lookup"><span data-stu-id="061cf-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="061cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="061cf-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="061cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="061cf-105">DESCRIPTION</span></span>
<span data-ttu-id="061cf-106">Das Cmdlet **Remove-AzSqlServerCommunicationLink** löscht eine Server-zu-Server-Kommunikationsverknüpfung für elastische Datenbanktransaktionen in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="061cf-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="061cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="061cf-107">EXAMPLES</span></span>

### <span data-ttu-id="061cf-108">Beispiel 1: Löschen einer Kommunikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="061cf-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="061cf-109">Dieser Befehl löscht einen Server-zu-Server-Kommunikationslink namens Link01 auf ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="061cf-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="061cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="061cf-110">PARAMETERS</span></span>

### <span data-ttu-id="061cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061cf-111">-DefaultProfile</span></span>
<span data-ttu-id="061cf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="061cf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="061cf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="061cf-113">-Force</span></span>
<span data-ttu-id="061cf-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="061cf-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="061cf-115">-Linkname</span><span class="sxs-lookup"><span data-stu-id="061cf-115">-LinkName</span></span>
<span data-ttu-id="061cf-116">Gibt den Namen des Server Kommunikationslinks an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="061cf-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="061cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="061cf-118">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="061cf-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="061cf-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="061cf-119">-ServerName</span></span>
<span data-ttu-id="061cf-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="061cf-120">Specifies the name of a server.</span></span>
<span data-ttu-id="061cf-121">Dieser Server enthält den Kommunikationslink, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="061cf-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="061cf-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="061cf-122">-Confirm</span></span>
<span data-ttu-id="061cf-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="061cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="061cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="061cf-124">-WhatIf</span></span>
<span data-ttu-id="061cf-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="061cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="061cf-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="061cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="061cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061cf-127">CommonParameters</span></span>
<span data-ttu-id="061cf-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061cf-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="061cf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061cf-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="061cf-130">INPUTS</span></span>

### <span data-ttu-id="061cf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="061cf-131">System.String</span></span>

## <span data-ttu-id="061cf-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="061cf-132">OUTPUTS</span></span>

### <span data-ttu-id="061cf-133">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="061cf-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="061cf-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="061cf-134">NOTES</span></span>
* <span data-ttu-id="061cf-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="061cf-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="061cf-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="061cf-136">RELATED LINKS</span></span>

[<span data-ttu-id="061cf-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="061cf-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="061cf-138">Neu – AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="061cf-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="061cf-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="061cf-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

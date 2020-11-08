---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176873"
---
# <span data-ttu-id="37175-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="37175-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="37175-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37175-102">SYNOPSIS</span></span>
<span data-ttu-id="37175-103">Erstellt eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei SQL-Datenbankservern.</span><span class="sxs-lookup"><span data-stu-id="37175-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="37175-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37175-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37175-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37175-105">DESCRIPTION</span></span>
<span data-ttu-id="37175-106">Das Cmdlet **New-AzSqlServerCommunicationLink** erstellt eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei logischen Servern in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="37175-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="37175-107">Elastische Datenbanktransaktionen können Datenbanken auf einem der gepaarten Server überspannen.</span><span class="sxs-lookup"><span data-stu-id="37175-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="37175-108">Sie können mehr als einen Link auf einem Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="37175-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="37175-109">Daher können sich elastische Datenbanktransaktionen über eine größere Anzahl von Servern erstrecken.</span><span class="sxs-lookup"><span data-stu-id="37175-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="37175-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37175-110">EXAMPLES</span></span>

### <span data-ttu-id="37175-111">Beispiel 1: Erstellen einer Kommunikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="37175-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="37175-112">Dieser Befehl erstellt einen Link mit dem Namen Link01 zwischen ContosoServer17 und ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="37175-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="37175-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="37175-113">PARAMETERS</span></span>

### <span data-ttu-id="37175-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37175-114">-AsJob</span></span>
<span data-ttu-id="37175-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="37175-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37175-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37175-116">-DefaultProfile</span></span>
<span data-ttu-id="37175-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="37175-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37175-118">-Linkname</span><span class="sxs-lookup"><span data-stu-id="37175-118">-LinkName</span></span>
<span data-ttu-id="37175-119">Gibt den Namen der Server Kommunikationsverbindung an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="37175-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="37175-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="37175-120">-PartnerServer</span></span>
<span data-ttu-id="37175-121">Gibt den Namen des anderen Servers an, der an dieser Kommunikationsverknüpfung teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="37175-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="37175-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37175-122">-ResourceGroupName</span></span>
<span data-ttu-id="37175-123">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="37175-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="37175-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="37175-124">-ServerName</span></span>
<span data-ttu-id="37175-125">Gibt den Namen des Servers an, auf dem dieses Cmdlet den Kommunikationslink einrichtet.</span><span class="sxs-lookup"><span data-stu-id="37175-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="37175-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37175-126">-Confirm</span></span>
<span data-ttu-id="37175-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37175-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37175-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37175-128">-WhatIf</span></span>
<span data-ttu-id="37175-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37175-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37175-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37175-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37175-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37175-131">CommonParameters</span></span>
<span data-ttu-id="37175-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37175-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37175-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37175-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37175-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37175-134">INPUTS</span></span>

### <span data-ttu-id="37175-135">System. String</span><span class="sxs-lookup"><span data-stu-id="37175-135">System.String</span></span>

## <span data-ttu-id="37175-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37175-136">OUTPUTS</span></span>

### <span data-ttu-id="37175-137">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="37175-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="37175-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="37175-138">NOTES</span></span>
* <span data-ttu-id="37175-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="37175-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="37175-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37175-140">RELATED LINKS</span></span>

[<span data-ttu-id="37175-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="37175-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="37175-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="37175-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="37175-143">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="37175-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

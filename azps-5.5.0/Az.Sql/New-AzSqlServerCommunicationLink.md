---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145644"
---
# <span data-ttu-id="0cff0-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0cff0-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="0cff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cff0-102">SYNOPSIS</span></span>
<span data-ttu-id="0cff0-103">Erstellt eine Kommunikationsverknüpfung für Datenbanktransaktionen zwischen zwei SQL Datenbankservern.</span><span class="sxs-lookup"><span data-stu-id="0cff0-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="0cff0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cff0-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cff0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cff0-105">DESCRIPTION</span></span>
<span data-ttu-id="0cff0-106">Das **Cmdlet "New-AzSqlServerCommunicationLink"** erstellt eine Kommunikationsverknüpfung für Datenbanktransaktionen zwischen zwei logischen Servern in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0cff0-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="0cff0-107">Weite Datenbanktransaktionen können Datenbanken auf einem der gekoppelten Server umfassen.</span><span class="sxs-lookup"><span data-stu-id="0cff0-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="0cff0-108">Sie können auf einem Server mehrere Links erstellen.</span><span class="sxs-lookup"><span data-stu-id="0cff0-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="0cff0-109">Daher können Datenbanktransaktionen über eine größere Anzahl von Servern hinweg ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0cff0-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="0cff0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0cff0-110">EXAMPLES</span></span>

### <span data-ttu-id="0cff0-111">Beispiel 1: Erstellen einer Kommunikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="0cff0-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="0cff0-112">Mit diesem Befehl wird ein Link namens "Link01" zwischen ContosoServer17 und ContosoServer02 erstellt.</span><span class="sxs-lookup"><span data-stu-id="0cff0-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="0cff0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cff0-113">PARAMETERS</span></span>

### <span data-ttu-id="0cff0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cff0-114">-AsJob</span></span>
<span data-ttu-id="0cff0-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0cff0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cff0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cff0-116">-DefaultProfile</span></span>
<span data-ttu-id="0cff0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0cff0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cff0-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="0cff0-118">-LinkName</span></span>
<span data-ttu-id="0cff0-119">Gibt den Namen der Serverkommunikationsverknüpfung an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0cff0-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0cff0-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="0cff0-120">-PartnerServer</span></span>
<span data-ttu-id="0cff0-121">Gibt den Namen des anderen Servers an, der an diesem Kommunikationslink teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="0cff0-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="0cff0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cff0-122">-ResourceGroupName</span></span>
<span data-ttu-id="0cff0-123">Gibt den Namen der Ressourcengruppe an, zu der der vom Parameter *"ServerName"* angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="0cff0-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="0cff0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0cff0-124">-ServerName</span></span>
<span data-ttu-id="0cff0-125">Gibt den Namen des Servers an, auf dem dieses Cmdlet die Kommunikationsverknüpfung ein richtet.</span><span class="sxs-lookup"><span data-stu-id="0cff0-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="0cff0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cff0-126">-Confirm</span></span>
<span data-ttu-id="0cff0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cff0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cff0-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0cff0-128">-WhatIf</span></span>
<span data-ttu-id="0cff0-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cff0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cff0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cff0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cff0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cff0-131">CommonParameters</span></span>
<span data-ttu-id="0cff0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cff0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cff0-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cff0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cff0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0cff0-134">INPUTS</span></span>

### <span data-ttu-id="0cff0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0cff0-135">System.String</span></span>

## <span data-ttu-id="0cff0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0cff0-136">OUTPUTS</span></span>

### <span data-ttu-id="0cff0-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="0cff0-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="0cff0-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0cff0-138">NOTES</span></span>
* <span data-ttu-id="0cff0-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="0cff0-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="0cff0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0cff0-140">RELATED LINKS</span></span>

[<span data-ttu-id="0cff0-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0cff0-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="0cff0-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="0cff0-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="0cff0-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="0cff0-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

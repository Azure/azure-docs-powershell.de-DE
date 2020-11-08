---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173444"
---
# <span data-ttu-id="79168-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79168-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="79168-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79168-102">SYNOPSIS</span></span>
<span data-ttu-id="79168-103">Ruft Kommunikationslinks für elastische Datenbanktransaktionen zwischen Datenbankservern ab.</span><span class="sxs-lookup"><span data-stu-id="79168-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="79168-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79168-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79168-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79168-105">DESCRIPTION</span></span>
<span data-ttu-id="79168-106">Das Cmdlet " **Get-AzSqlServerCommunicationLink** " Ruft Server-zu-Server-Kommunikationslinks für elastische Datenbanktransaktionen in Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="79168-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="79168-107">Geben Sie den Namen eines Server Kommunikationslinks an, um die Eigenschaften für diesen Link anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="79168-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="79168-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79168-108">EXAMPLES</span></span>

### <span data-ttu-id="79168-109">Beispiel 1: Abrufen aller Kommunikationslinks für einen Server</span><span class="sxs-lookup"><span data-stu-id="79168-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="79168-110">Dieser Befehl ruft alle Server-zu-Server-Kommunikationslinks für elastische Datenbanktransaktionen für den Server mit dem Namen ContosoServer17 ab.</span><span class="sxs-lookup"><span data-stu-id="79168-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="79168-111">Beispiel 2: Abrufen eines bestimmten Kommunikationslinks für einen Server</span><span class="sxs-lookup"><span data-stu-id="79168-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="79168-112">Dieser Befehl ruft den Server-zu-Server-Kommunikationslink mit dem Namen Link01 ab.</span><span class="sxs-lookup"><span data-stu-id="79168-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="79168-113">Beispiel 3: Abrufen aller Kommunikationslinks für einen Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="79168-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="79168-114">Dieser Befehl ruft alle Server-zu-Server-Kommunikationslinks für elastische Datenbanktransaktionen für den Server mit dem Namen "ContosoServer17" ab, die mit "Link" beginnen.</span><span class="sxs-lookup"><span data-stu-id="79168-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="79168-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="79168-115">PARAMETERS</span></span>

### <span data-ttu-id="79168-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79168-116">-DefaultProfile</span></span>
<span data-ttu-id="79168-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="79168-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79168-118">-Linkname</span><span class="sxs-lookup"><span data-stu-id="79168-118">-LinkName</span></span>
<span data-ttu-id="79168-119">Gibt den Namen der Server Kommunikationsverbindung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="79168-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79168-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79168-120">-ResourceGroupName</span></span>
<span data-ttu-id="79168-121">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="79168-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="79168-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="79168-122">-ServerName</span></span>
<span data-ttu-id="79168-123">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="79168-123">Specifies the name of a server.</span></span>
<span data-ttu-id="79168-124">Dieser Server enthält einen Kommunikationslink, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="79168-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79168-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79168-125">-Confirm</span></span>
<span data-ttu-id="79168-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79168-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79168-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79168-127">-WhatIf</span></span>
<span data-ttu-id="79168-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79168-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79168-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79168-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79168-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79168-130">CommonParameters</span></span>
<span data-ttu-id="79168-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79168-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79168-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79168-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79168-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79168-133">INPUTS</span></span>

### <span data-ttu-id="79168-134">System. String</span><span class="sxs-lookup"><span data-stu-id="79168-134">System.String</span></span>

## <span data-ttu-id="79168-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79168-135">OUTPUTS</span></span>

### <span data-ttu-id="79168-136">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="79168-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="79168-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="79168-137">NOTES</span></span>
* <span data-ttu-id="79168-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="79168-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="79168-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79168-139">RELATED LINKS</span></span>

[<span data-ttu-id="79168-140">Neu – AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79168-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="79168-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79168-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="79168-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="79168-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

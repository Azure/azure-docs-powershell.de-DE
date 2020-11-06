---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ac2ec676143ef1179adbfeb793bd787d81e8f435
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478866"
---
# <span data-ttu-id="79e0d-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79e0d-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="79e0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="79e0d-103">Erstellt eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei SQL-Datenbankservern.</span><span class="sxs-lookup"><span data-stu-id="79e0d-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79e0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79e0d-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79e0d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="79e0d-106">Das Cmdlet **New-AzureRmSqlServerCommunicationLink** erstellt eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei logischen Servern in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="79e0d-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="79e0d-107">Elastische Datenbanktransaktionen können Datenbanken auf einem der gepaarten Server überspannen.</span><span class="sxs-lookup"><span data-stu-id="79e0d-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="79e0d-108">Sie können mehr als einen Link auf einem Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="79e0d-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="79e0d-109">Daher können sich elastische Datenbanktransaktionen über eine größere Anzahl von Servern erstrecken.</span><span class="sxs-lookup"><span data-stu-id="79e0d-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="79e0d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="79e0d-111">Beispiel 1: Erstellen einer Kommunikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="79e0d-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="79e0d-112">Dieser Befehl erstellt einen Link mit dem Namen Link01 zwischen ContosoServer17 und ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="79e0d-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="79e0d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="79e0d-113">PARAMETERS</span></span>

### <span data-ttu-id="79e0d-114">-Linkname</span><span class="sxs-lookup"><span data-stu-id="79e0d-114">-LinkName</span></span>
<span data-ttu-id="79e0d-115">Gibt den Namen der Server Kommunikationsverbindung an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="79e0d-115">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="79e0d-116">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="79e0d-116">-PartnerServer</span></span>
<span data-ttu-id="79e0d-117">Gibt den Namen des anderen Servers an, der an dieser Kommunikationsverknüpfung teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="79e0d-117">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="79e0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="79e0d-119">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="79e0d-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="79e0d-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="79e0d-120">-ServerName</span></span>
<span data-ttu-id="79e0d-121">Gibt den Namen des Servers an, auf dem dieses Cmdlet den Kommunikationslink einrichtet.</span><span class="sxs-lookup"><span data-stu-id="79e0d-121">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="79e0d-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79e0d-122">-Confirm</span></span>
<span data-ttu-id="79e0d-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79e0d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e0d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e0d-124">-WhatIf</span></span>
<span data-ttu-id="79e0d-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79e0d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e0d-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79e0d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e0d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e0d-127">-DefaultProfile</span></span>
<span data-ttu-id="79e0d-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79e0d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e0d-129">CommonParameters</span></span>
<span data-ttu-id="79e0d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e0d-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e0d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79e0d-132">INPUTS</span></span>

## <span data-ttu-id="79e0d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79e0d-133">OUTPUTS</span></span>

### <span data-ttu-id="79e0d-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="79e0d-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="79e0d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="79e0d-135">NOTES</span></span>
* <span data-ttu-id="79e0d-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="79e0d-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="79e0d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79e0d-137">RELATED LINKS</span></span>

[<span data-ttu-id="79e0d-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79e0d-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="79e0d-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="79e0d-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="79e0d-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="79e0d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

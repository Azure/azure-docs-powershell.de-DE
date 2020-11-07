---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8240712b4ec6ef17dfff597bed4dc62d60be42b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662556"
---
# <span data-ttu-id="5af1c-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="5af1c-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="5af1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5af1c-102">SYNOPSIS</span></span>
<span data-ttu-id="5af1c-103">Ruft Kommunikationslinks für elastische Datenbanktransaktionen zwischen Datenbankservern ab.</span><span class="sxs-lookup"><span data-stu-id="5af1c-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5af1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5af1c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5af1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5af1c-105">DESCRIPTION</span></span>
<span data-ttu-id="5af1c-106">Das Cmdlet " **Get-AzureRmSqlServerCommunicationLink** " Ruft Server-zu-Server-Kommunikationslinks für elastische Datenbanktransaktionen in Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="5af1c-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="5af1c-107">Geben Sie den Namen eines Server Kommunikationslinks an, um die Eigenschaften für diesen Link anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5af1c-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="5af1c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5af1c-108">EXAMPLES</span></span>

### <span data-ttu-id="5af1c-109">Beispiel 1: Abrufen aller Kommunikationslinks für einen Server</span><span class="sxs-lookup"><span data-stu-id="5af1c-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="5af1c-110">Dieser Befehl ruft alle Server-zu-Server-Kommunikationslinks für elastische Datenbanktransaktionen für den Server mit dem Namen ContosoServer17 ab.</span><span class="sxs-lookup"><span data-stu-id="5af1c-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="5af1c-111">Beispiel 2: Abrufen eines bestimmten Kommunikationslinks für einen Server</span><span class="sxs-lookup"><span data-stu-id="5af1c-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="5af1c-112">Dieser Befehl ruft den Server-zu-Server-Kommunikationslink mit dem Namen Link01 ab.</span><span class="sxs-lookup"><span data-stu-id="5af1c-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="5af1c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af1c-113">PARAMETERS</span></span>

### <span data-ttu-id="5af1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af1c-114">-DefaultProfile</span></span>
<span data-ttu-id="5af1c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5af1c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5af1c-116">-Linkname</span><span class="sxs-lookup"><span data-stu-id="5af1c-116">-LinkName</span></span>
<span data-ttu-id="5af1c-117">Gibt den Namen der Server Kommunikationsverbindung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5af1c-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af1c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af1c-118">-ResourceGroupName</span></span>
<span data-ttu-id="5af1c-119">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="5af1c-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="5af1c-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="5af1c-120">-ServerName</span></span>
<span data-ttu-id="5af1c-121">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="5af1c-121">Specifies the name of a server.</span></span>
<span data-ttu-id="5af1c-122">Dieser Server enthält einen Kommunikationslink, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5af1c-122">This server contains a communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af1c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5af1c-123">-Confirm</span></span>
<span data-ttu-id="5af1c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5af1c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af1c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af1c-125">-WhatIf</span></span>
<span data-ttu-id="5af1c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5af1c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af1c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5af1c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af1c-128">CommonParameters</span></span>
<span data-ttu-id="5af1c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af1c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af1c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5af1c-131">INPUTS</span></span>

### <span data-ttu-id="5af1c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="5af1c-132">None</span></span>
<span data-ttu-id="5af1c-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5af1c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5af1c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5af1c-134">OUTPUTS</span></span>

### <span data-ttu-id="5af1c-135">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="5af1c-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="5af1c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5af1c-136">NOTES</span></span>
* <span data-ttu-id="5af1c-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="5af1c-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="5af1c-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5af1c-138">RELATED LINKS</span></span>

[<span data-ttu-id="5af1c-139">Neu – AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="5af1c-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="5af1c-140">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="5af1c-140">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="5af1c-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5af1c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

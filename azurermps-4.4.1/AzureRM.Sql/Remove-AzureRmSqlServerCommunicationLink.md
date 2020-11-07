---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664958"
---
# <span data-ttu-id="08ee9-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08ee9-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="08ee9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="08ee9-103">Löscht eine Kommunikationsverknüpfung für elastische Datenbanktransaktionen zwischen zwei Servern.</span><span class="sxs-lookup"><span data-stu-id="08ee9-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08ee9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ee9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08ee9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08ee9-105">DESCRIPTION</span></span>
<span data-ttu-id="08ee9-106">Das Cmdlet **Remove-AzureRmSqlServerCommunicationLink** löscht eine Server-zu-Server-Kommunikationsverknüpfung für elastische Datenbanktransaktionen in Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="08ee9-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="08ee9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08ee9-107">EXAMPLES</span></span>

### <span data-ttu-id="08ee9-108">Beispiel 1: Löschen einer Kommunikationsverknüpfung</span><span class="sxs-lookup"><span data-stu-id="08ee9-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="08ee9-109">Dieser Befehl löscht einen Server-zu-Server-Kommunikationslink namens Link01 auf ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="08ee9-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="08ee9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ee9-110">PARAMETERS</span></span>

### <span data-ttu-id="08ee9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="08ee9-111">-Force</span></span>
<span data-ttu-id="08ee9-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="08ee9-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08ee9-113">-Linkname</span><span class="sxs-lookup"><span data-stu-id="08ee9-113">-LinkName</span></span>
<span data-ttu-id="08ee9-114">Gibt den Namen des Server Kommunikationslinks an, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="08ee9-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="08ee9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ee9-115">-ResourceGroupName</span></span>
<span data-ttu-id="08ee9-116">Gibt den Namen der Ressourcengruppe an, zu der der vom Server *Name* -Parameter angegebene Server gehört.</span><span class="sxs-lookup"><span data-stu-id="08ee9-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="08ee9-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="08ee9-117">-ServerName</span></span>
<span data-ttu-id="08ee9-118">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="08ee9-118">Specifies the name of a server.</span></span>
<span data-ttu-id="08ee9-119">Dieser Server enthält den Kommunikationslink, den dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="08ee9-119">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="08ee9-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08ee9-120">-Confirm</span></span>
<span data-ttu-id="08ee9-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08ee9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ee9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ee9-122">-WhatIf</span></span>
<span data-ttu-id="08ee9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08ee9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ee9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08ee9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ee9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ee9-125">-DefaultProfile</span></span>
<span data-ttu-id="08ee9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08ee9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08ee9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ee9-127">CommonParameters</span></span>
<span data-ttu-id="08ee9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ee9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ee9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ee9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ee9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08ee9-130">INPUTS</span></span>

## <span data-ttu-id="08ee9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08ee9-131">OUTPUTS</span></span>

### <span data-ttu-id="08ee9-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="08ee9-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="08ee9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="08ee9-133">NOTES</span></span>
* <span data-ttu-id="08ee9-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL</span><span class="sxs-lookup"><span data-stu-id="08ee9-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="08ee9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08ee9-135">RELATED LINKS</span></span>

[<span data-ttu-id="08ee9-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08ee9-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="08ee9-137">Neu – AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08ee9-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="08ee9-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="08ee9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ebd1fa17bfe35a4f0cb73d5ff3c3658e439abf78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496822"
---
# <span data-ttu-id="11a61-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="11a61-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="11a61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11a61-102">SYNOPSIS</span></span>
<span data-ttu-id="11a61-103">Ruft Informationen zu einem Azure AD-Administrator für SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="11a61-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a61-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a61-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11a61-105">DESCRIPTION</span></span>
<span data-ttu-id="11a61-106">Das Cmdlet " **Get-AzureRmSqlServerActiveDirectoryAdministrator** " Ruft Informationen zu einem Azure Active Directory (Azure AD)-Administrator für einen AzureSQL-Server im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="11a61-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="11a61-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11a61-107">EXAMPLES</span></span>

### <span data-ttu-id="11a61-108">Beispiel 1: Abrufen von Informationen zu einem Administrator für einen Server</span><span class="sxs-lookup"><span data-stu-id="11a61-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="11a61-109">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator für einen Server mit dem Namen SERVER01 ab, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11a61-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="11a61-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="11a61-110">PARAMETERS</span></span>

### <span data-ttu-id="11a61-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a61-111">-ResourceGroupName</span></span>
<span data-ttu-id="11a61-112">Gibt den Namen der Ressourcengruppe an, der der SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="11a61-112">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="11a61-113">-Servername</span><span class="sxs-lookup"><span data-stu-id="11a61-113">-ServerName</span></span>
<span data-ttu-id="11a61-114">Gibt den Namen des SQL-Servers an, für den dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="11a61-114">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="11a61-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11a61-115">-Confirm</span></span>
<span data-ttu-id="11a61-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11a61-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a61-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a61-117">-WhatIf</span></span>
<span data-ttu-id="11a61-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11a61-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a61-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11a61-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a61-120">-DefaultProfile</span></span>
<span data-ttu-id="11a61-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11a61-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a61-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a61-122">CommonParameters</span></span>
<span data-ttu-id="11a61-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a61-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a61-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a61-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a61-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11a61-125">INPUTS</span></span>

## <span data-ttu-id="11a61-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11a61-126">OUTPUTS</span></span>

### <span data-ttu-id="11a61-127">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="11a61-127">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="11a61-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="11a61-128">NOTES</span></span>

## <span data-ttu-id="11a61-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11a61-129">RELATED LINKS</span></span>

[<span data-ttu-id="11a61-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="11a61-130">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="11a61-131">Satz-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="11a61-131">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="11a61-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="11a61-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



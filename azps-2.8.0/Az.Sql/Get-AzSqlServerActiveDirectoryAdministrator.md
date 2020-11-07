---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f98e362c10a0773f16ae4b687e5d725fb12f5053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826084"
---
# <span data-ttu-id="b780e-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b780e-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b780e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b780e-102">SYNOPSIS</span></span>
<span data-ttu-id="b780e-103">Ruft Informationen zu einem Azure AD-Administrator für SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="b780e-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="b780e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b780e-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b780e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b780e-105">DESCRIPTION</span></span>
<span data-ttu-id="b780e-106">Das Cmdlet " **Get-AzSqlServerActiveDirectoryAdministrator** " Ruft Informationen zu einem Azure Active Directory (Azure AD)-Administrator für einen AzureSQL-Server im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b780e-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="b780e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b780e-107">EXAMPLES</span></span>

### <span data-ttu-id="b780e-108">Beispiel 1: Abrufen von Informationen zu einem Administrator für einen Server</span><span class="sxs-lookup"><span data-stu-id="b780e-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b780e-109">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator für einen Server mit dem Namen SERVER01 ab, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b780e-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b780e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b780e-110">PARAMETERS</span></span>

### <span data-ttu-id="b780e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b780e-111">-DefaultProfile</span></span>
<span data-ttu-id="b780e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b780e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b780e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b780e-113">-ResourceGroupName</span></span>
<span data-ttu-id="b780e-114">Gibt den Namen der Ressourcengruppe an, der der SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b780e-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="b780e-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="b780e-115">-ServerName</span></span>
<span data-ttu-id="b780e-116">Gibt den Namen des SQL-Servers an, für den dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="b780e-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="b780e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b780e-117">-Confirm</span></span>
<span data-ttu-id="b780e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b780e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b780e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b780e-119">-WhatIf</span></span>
<span data-ttu-id="b780e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b780e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b780e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b780e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b780e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b780e-122">CommonParameters</span></span>
<span data-ttu-id="b780e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b780e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b780e-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b780e-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b780e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b780e-125">INPUTS</span></span>

### <span data-ttu-id="b780e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b780e-126">System.String</span></span>

## <span data-ttu-id="b780e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b780e-127">OUTPUTS</span></span>

### <span data-ttu-id="b780e-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="b780e-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b780e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b780e-129">NOTES</span></span>

## <span data-ttu-id="b780e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b780e-130">RELATED LINKS</span></span>

[<span data-ttu-id="b780e-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b780e-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b780e-132">Satz-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b780e-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b780e-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b780e-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



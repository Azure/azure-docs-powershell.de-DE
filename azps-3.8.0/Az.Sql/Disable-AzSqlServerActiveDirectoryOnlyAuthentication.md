---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996719"
---
# <span data-ttu-id="5c7ec-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="5c7ec-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="5c7ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7ec-103">Deaktiviert die Azure AD only-Authentifizierung für einen bestimmten SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="5c7ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c7ec-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c7ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="5c7ec-106">Das Cmdlet **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für einen AzureSQL-Server im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="5c7ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c7ec-107">EXAMPLES</span></span>

### <span data-ttu-id="5c7ec-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c7ec-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="5c7ec-109">Dieser Befehl deaktiviert die Azure Active Directory (Azure AD) only-Authentifizierungsanforderung für einen AzureSQL-Server mit dem Namen Server01, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5c7ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c7ec-110">PARAMETERS</span></span>

### <span data-ttu-id="5c7ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7ec-111">-DefaultProfile</span></span>
<span data-ttu-id="5c7ec-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7ec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7ec-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c7ec-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c7ec-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="5c7ec-115">-ServerName</span></span>
<span data-ttu-id="5c7ec-116">Der Name des Azure SQL Server, in dem sich der Azure Active Directory-Administrator befindet.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="5c7ec-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c7ec-117">-Confirm</span></span>
<span data-ttu-id="5c7ec-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7ec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c7ec-119">-WhatIf</span></span>
<span data-ttu-id="5c7ec-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c7ec-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7ec-122">CommonParameters</span></span>
<span data-ttu-id="5c7ec-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c7ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7ec-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c7ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7ec-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c7ec-125">INPUTS</span></span>

### <span data-ttu-id="5c7ec-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5c7ec-126">System.String</span></span>

## <span data-ttu-id="5c7ec-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c7ec-127">OUTPUTS</span></span>

### <span data-ttu-id="5c7ec-128">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="5c7ec-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="5c7ec-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c7ec-129">NOTES</span></span>

## <span data-ttu-id="5c7ec-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c7ec-130">RELATED LINKS</span></span>

[<span data-ttu-id="5c7ec-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5c7ec-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5c7ec-132">Satz-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5c7ec-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5c7ec-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5c7ec-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5c7ec-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5c7ec-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

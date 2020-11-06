---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480862"
---
# <span data-ttu-id="246e3-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="246e3-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="246e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="246e3-102">SYNOPSIS</span></span>
<span data-ttu-id="246e3-103">Ruft Informationen zu einem Azure AD-Administrator für SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="246e3-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="246e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="246e3-105">DESCRIPTION</span></span>
<span data-ttu-id="246e3-106">Das Cmdlet " **Get-AzureRmSqlServerActiveDirectoryAdministrator** " Ruft Informationen zu einem Azure Active Directory (Azure AD)-Administrator für einen AzureSQL-Server im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="246e3-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="246e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="246e3-107">EXAMPLES</span></span>

### <span data-ttu-id="246e3-108">Beispiel 1: Abrufen von Informationen zu einem Administrator für einen Server</span><span class="sxs-lookup"><span data-stu-id="246e3-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="246e3-109">Dieser Befehl ruft Informationen zu einem Azure AD-Administrator für einen Server mit dem Namen SERVER01 ab, der einer Ressourcengruppe mit dem Namen ResourceGroup01 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="246e3-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="246e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="246e3-110">PARAMETERS</span></span>

### <span data-ttu-id="246e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246e3-111">-DefaultProfile</span></span>
<span data-ttu-id="246e3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="246e3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="246e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="246e3-114">Gibt den Namen der Ressourcengruppe an, der der SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="246e3-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="246e3-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="246e3-115">-ServerName</span></span>
<span data-ttu-id="246e3-116">Gibt den Namen des SQL-Servers an, für den dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="246e3-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="246e3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="246e3-117">-Confirm</span></span>
<span data-ttu-id="246e3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="246e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246e3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246e3-119">-WhatIf</span></span>
<span data-ttu-id="246e3-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="246e3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246e3-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="246e3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246e3-122">CommonParameters</span></span>
<span data-ttu-id="246e3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246e3-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246e3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="246e3-125">INPUTS</span></span>

### <span data-ttu-id="246e3-126">Keine</span><span class="sxs-lookup"><span data-stu-id="246e3-126">None</span></span>
<span data-ttu-id="246e3-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="246e3-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="246e3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="246e3-128">OUTPUTS</span></span>

### <span data-ttu-id="246e3-129">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="246e3-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="246e3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="246e3-130">NOTES</span></span>

## <span data-ttu-id="246e3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="246e3-131">RELATED LINKS</span></span>

[<span data-ttu-id="246e3-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="246e3-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="246e3-133">Satz-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="246e3-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="246e3-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="246e3-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



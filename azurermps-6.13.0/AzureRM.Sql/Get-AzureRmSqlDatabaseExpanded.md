---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: f2ee19834cdb4144c8f207ae8ff10a90a733bece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495638"
---
# <span data-ttu-id="34539-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="34539-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="34539-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34539-102">SYNOPSIS</span></span>
<span data-ttu-id="34539-103">Ruft eine Datenbank und deren erweiterte Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="34539-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34539-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34539-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34539-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34539-105">DESCRIPTION</span></span>
<span data-ttu-id="34539-106">Das Cmdlet " **Get-AzureRmSqlDatabaseExpanded** " Ruft eine Datenbank und deren erweiterte Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="34539-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="34539-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34539-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="34539-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34539-108">EXAMPLES</span></span>

### <span data-ttu-id="34539-109">Beispiel 1: Abrufen von Datenbankobjekten mit Informationen zum Dienststatus-Ratgeber</span><span class="sxs-lookup"><span data-stu-id="34539-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="34539-110">Dieser Befehl gibt die Datenbank mit erweiterten Eigenschaften zurück, die die Informationen zum Dienststatus-Ratgeber enthalten.</span><span class="sxs-lookup"><span data-stu-id="34539-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="34539-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="34539-111">PARAMETERS</span></span>

### <span data-ttu-id="34539-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34539-112">-DatabaseName</span></span>
<span data-ttu-id="34539-113">Gibt den Namen der Datenbank an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34539-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="34539-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34539-114">-DefaultProfile</span></span>
<span data-ttu-id="34539-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="34539-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34539-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34539-116">-ResourceGroupName</span></span>
<span data-ttu-id="34539-117">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="34539-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="34539-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="34539-118">-ServerName</span></span>
<span data-ttu-id="34539-119">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="34539-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="34539-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34539-120">-Confirm</span></span>
<span data-ttu-id="34539-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34539-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34539-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34539-122">-WhatIf</span></span>
<span data-ttu-id="34539-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34539-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34539-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34539-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34539-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34539-125">CommonParameters</span></span>
<span data-ttu-id="34539-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34539-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34539-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34539-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34539-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34539-128">INPUTS</span></span>

### <span data-ttu-id="34539-129">System. String</span><span class="sxs-lookup"><span data-stu-id="34539-129">System.String</span></span>

## <span data-ttu-id="34539-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34539-130">OUTPUTS</span></span>

### <span data-ttu-id="34539-131">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="34539-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="34539-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="34539-132">NOTES</span></span>

## <span data-ttu-id="34539-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34539-133">RELATED LINKS</span></span>

[<span data-ttu-id="34539-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="34539-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

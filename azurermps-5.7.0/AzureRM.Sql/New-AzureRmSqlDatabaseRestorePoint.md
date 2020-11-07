---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663743"
---
# <span data-ttu-id="1dbb7-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="1dbb7-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="1dbb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbb7-103">Erstellt einen neuen Wiederherstellungspunkt, von dem eine SQL-Datenbank wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dbb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dbb7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbb7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbb7-106">Das Cmdlet **New-AzureRmSqlDatabaseRestorePoint** erstellt einen neuen Wiederherstellungspunkt, aus dem eine Azure SQL-Datenbank wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="1dbb7-107">Dieses Cmdlet wird derzeit vom SQL Server Datawarehouse-Dienst in Azure SQL-Datenbank unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="1dbb7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dbb7-108">EXAMPLES</span></span>

### <span data-ttu-id="1dbb7-109">Beispiel 1: Erstellen eines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="1dbb7-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="1dbb7-110">Dieser Befehl erstellt einen Wiederherstellungspunkt für Azure SQL-Datenbank und gibt die Details des Wiederherstellungspunkts zurück.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="1dbb7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dbb7-111">PARAMETERS</span></span>

### <span data-ttu-id="1dbb7-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dbb7-112">-DatabaseName</span></span>
<span data-ttu-id="1dbb7-113">Gibt den Namen der SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbb7-114">-DefaultProfile</span></span>
<span data-ttu-id="1dbb7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1dbb7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dbb7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbb7-116">-ResourceGroupName</span></span>
<span data-ttu-id="1dbb7-117">Gibt den Namen der Ressourcengruppe an, der die SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="1dbb7-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="1dbb7-118">-RestorePointLabel</span></span>
<span data-ttu-id="1dbb7-119">Gibt die Beschriftung des Wiederherstellungspunkts zur einfachen Identifizierung an.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbb7-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="1dbb7-120">-ServerName</span></span>
<span data-ttu-id="1dbb7-121">Gibt den Namen des AzureSQL-Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="1dbb7-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dbb7-122">-Confirm</span></span>
<span data-ttu-id="1dbb7-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbb7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbb7-124">-WhatIf</span></span>
<span data-ttu-id="1dbb7-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbb7-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbb7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbb7-127">CommonParameters</span></span>
<span data-ttu-id="1dbb7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbb7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbb7-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbb7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbb7-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dbb7-130">INPUTS</span></span>

## <span data-ttu-id="1dbb7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dbb7-131">OUTPUTS</span></span>

## <span data-ttu-id="1dbb7-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dbb7-132">NOTES</span></span>

## <span data-ttu-id="1dbb7-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dbb7-133">RELATED LINKS</span></span>

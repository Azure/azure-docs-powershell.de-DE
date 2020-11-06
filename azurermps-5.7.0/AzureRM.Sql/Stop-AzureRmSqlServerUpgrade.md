---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476453"
---
# <span data-ttu-id="51db7-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="51db7-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="51db7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51db7-102">SYNOPSIS</span></span>
<span data-ttu-id="51db7-103">Beendet das Upgrade eines SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="51db7-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51db7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51db7-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51db7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51db7-105">DESCRIPTION</span></span>
<span data-ttu-id="51db7-106">Das Cmdlet **Stop-AzureRmSqlServerUpgrade** beendet das Upgrade eines Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="51db7-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="51db7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51db7-107">EXAMPLES</span></span>

### <span data-ttu-id="51db7-108">Beispiel 1: Beenden eines Server Upgrades</span><span class="sxs-lookup"><span data-stu-id="51db7-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="51db7-109">Dieser Befehl beendet die Anforderung zum Upgrade des Servers mit dem Namen Server02, der der Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="51db7-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="51db7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51db7-110">PARAMETERS</span></span>

### <span data-ttu-id="51db7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51db7-111">-DefaultProfile</span></span>
<span data-ttu-id="51db7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="51db7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51db7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="51db7-113">-Force</span></span>
<span data-ttu-id="51db7-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="51db7-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51db7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51db7-115">-ResourceGroupName</span></span>
<span data-ttu-id="51db7-116">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="51db7-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="51db7-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="51db7-117">-ServerName</span></span>
<span data-ttu-id="51db7-118">Gibt den Namen des Servers an, für den das Cmdlet ein Upgrade beendet.</span><span class="sxs-lookup"><span data-stu-id="51db7-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="51db7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51db7-119">-Confirm</span></span>
<span data-ttu-id="51db7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51db7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51db7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51db7-121">-WhatIf</span></span>
<span data-ttu-id="51db7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51db7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51db7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51db7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51db7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51db7-124">CommonParameters</span></span>
<span data-ttu-id="51db7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51db7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51db7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51db7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51db7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51db7-127">INPUTS</span></span>

### <span data-ttu-id="51db7-128">Microsoft. Azure. Commands. SQL. Serverupgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="51db7-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="51db7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51db7-129">OUTPUTS</span></span>

## <span data-ttu-id="51db7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="51db7-130">NOTES</span></span>

## <span data-ttu-id="51db7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51db7-131">RELATED LINKS</span></span>

[<span data-ttu-id="51db7-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="51db7-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="51db7-133">Anfang-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="51db7-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="51db7-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="51db7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



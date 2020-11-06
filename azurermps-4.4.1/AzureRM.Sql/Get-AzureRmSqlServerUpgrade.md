---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478901"
---
# <span data-ttu-id="117e9-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="117e9-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="117e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="117e9-102">SYNOPSIS</span></span>
<span data-ttu-id="117e9-103">Ruft den Status eines Azure SQL-Datenbankserver-Upgrades ab.</span><span class="sxs-lookup"><span data-stu-id="117e9-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="117e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="117e9-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="117e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="117e9-105">DESCRIPTION</span></span>
<span data-ttu-id="117e9-106">Das Cmdlet " **Get-AzureRmSqlServerUpgrade** " Ruft den Status eines Azure SQL-Datenbankserver-Upgrades ab.</span><span class="sxs-lookup"><span data-stu-id="117e9-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="117e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="117e9-107">EXAMPLES</span></span>

### <span data-ttu-id="117e9-108">Beispiel 1: Abrufen des Status eines Upgrades</span><span class="sxs-lookup"><span data-stu-id="117e9-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="117e9-109">Dieser Befehl ruft den Status eines Upgrades vom Server mit dem Namen Server01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="117e9-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="117e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="117e9-110">PARAMETERS</span></span>

### <span data-ttu-id="117e9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117e9-111">-ResourceGroupName</span></span>
<span data-ttu-id="117e9-112">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="117e9-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="117e9-113">-Servername</span><span class="sxs-lookup"><span data-stu-id="117e9-113">-ServerName</span></span>
<span data-ttu-id="117e9-114">Gibt den Namen des Servers an, für den das Cmdlet den Aktualisierungsstatus erhält.</span><span class="sxs-lookup"><span data-stu-id="117e9-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117e9-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="117e9-115">-Confirm</span></span>
<span data-ttu-id="117e9-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="117e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117e9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117e9-117">-WhatIf</span></span>
<span data-ttu-id="117e9-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="117e9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="117e9-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="117e9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117e9-120">-DefaultProfile</span></span>
<span data-ttu-id="117e9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="117e9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117e9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117e9-122">CommonParameters</span></span>
<span data-ttu-id="117e9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117e9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117e9-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117e9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117e9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="117e9-125">INPUTS</span></span>

## <span data-ttu-id="117e9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="117e9-126">OUTPUTS</span></span>

### <span data-ttu-id="117e9-127">Microsoft. Azure. Commands. SQL. Serverupgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="117e9-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="117e9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="117e9-128">NOTES</span></span>

## <span data-ttu-id="117e9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="117e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="117e9-130">Anfang-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="117e9-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="117e9-131">Stopp-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="117e9-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="117e9-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="117e9-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



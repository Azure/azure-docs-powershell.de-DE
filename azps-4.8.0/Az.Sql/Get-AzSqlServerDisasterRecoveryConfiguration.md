---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165526"
---
# <span data-ttu-id="4c914-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c914-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="4c914-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c914-102">SYNOPSIS</span></span>
<span data-ttu-id="4c914-103">Ruft eine Datenbankserver-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="4c914-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="4c914-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c914-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c914-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c914-105">DESCRIPTION</span></span>
<span data-ttu-id="4c914-106">Das Cmdlet " **Get-AzSqlServerDisasterRecoveryConfiguration** " Ruft eine SQL Database Server-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="4c914-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="4c914-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c914-107">EXAMPLES</span></span>

## <span data-ttu-id="4c914-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c914-108">PARAMETERS</span></span>

### <span data-ttu-id="4c914-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c914-109">-DefaultProfile</span></span>
<span data-ttu-id="4c914-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4c914-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c914-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c914-111">-ResourceGroupName</span></span>
<span data-ttu-id="4c914-112">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4c914-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4c914-113">-Servername</span><span class="sxs-lookup"><span data-stu-id="4c914-113">-ServerName</span></span>
<span data-ttu-id="4c914-114">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="4c914-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="4c914-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="4c914-115">-VirtualEndpointName</span></span>
<span data-ttu-id="4c914-116">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="4c914-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c914-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c914-117">-Confirm</span></span>
<span data-ttu-id="4c914-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c914-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c914-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c914-119">-WhatIf</span></span>
<span data-ttu-id="4c914-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c914-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c914-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c914-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c914-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c914-122">CommonParameters</span></span>
<span data-ttu-id="4c914-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c914-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c914-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c914-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c914-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c914-125">INPUTS</span></span>

### <span data-ttu-id="4c914-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4c914-126">System.String</span></span>

## <span data-ttu-id="4c914-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c914-127">OUTPUTS</span></span>

### <span data-ttu-id="4c914-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="4c914-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="4c914-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c914-129">NOTES</span></span>

## <span data-ttu-id="4c914-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c914-130">RELATED LINKS</span></span>

[<span data-ttu-id="4c914-131">Neu – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c914-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4c914-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c914-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4c914-133">Satz-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c914-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4c914-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4c914-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


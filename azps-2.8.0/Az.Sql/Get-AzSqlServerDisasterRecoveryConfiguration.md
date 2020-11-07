---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ac62ac0307422f0015fe578937a80a03e2a730d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826079"
---
# <span data-ttu-id="2c01a-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c01a-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2c01a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c01a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c01a-103">Ruft eine Datenbankserver-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="2c01a-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="2c01a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c01a-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c01a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c01a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c01a-106">Das Cmdlet " **Get-AzSqlServerDisasterRecoveryConfiguration** " Ruft eine SQL Database Server-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="2c01a-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2c01a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c01a-107">EXAMPLES</span></span>

## <span data-ttu-id="2c01a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c01a-108">PARAMETERS</span></span>

### <span data-ttu-id="2c01a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c01a-109">-DefaultProfile</span></span>
<span data-ttu-id="2c01a-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2c01a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c01a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c01a-111">-ResourceGroupName</span></span>
<span data-ttu-id="2c01a-112">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2c01a-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c01a-113">-Servername</span><span class="sxs-lookup"><span data-stu-id="2c01a-113">-ServerName</span></span>
<span data-ttu-id="2c01a-114">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="2c01a-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="2c01a-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2c01a-115">-VirtualEndpointName</span></span>
<span data-ttu-id="2c01a-116">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2c01a-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="2c01a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c01a-117">-Confirm</span></span>
<span data-ttu-id="2c01a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c01a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c01a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c01a-119">-WhatIf</span></span>
<span data-ttu-id="2c01a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c01a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c01a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c01a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c01a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c01a-122">CommonParameters</span></span>
<span data-ttu-id="2c01a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c01a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c01a-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c01a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c01a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c01a-125">INPUTS</span></span>

### <span data-ttu-id="2c01a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c01a-126">System.String</span></span>

## <span data-ttu-id="2c01a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c01a-127">OUTPUTS</span></span>

### <span data-ttu-id="2c01a-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="2c01a-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="2c01a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c01a-129">NOTES</span></span>

## <span data-ttu-id="2c01a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c01a-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c01a-131">Neu – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c01a-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c01a-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c01a-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c01a-133">Satz-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c01a-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c01a-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="2c01a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


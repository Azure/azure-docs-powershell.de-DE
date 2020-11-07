---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e70aafbf938fb8e10c36be41e0003f5310d082db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825919"
---
# <span data-ttu-id="9922c-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9922c-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="9922c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9922c-102">SYNOPSIS</span></span>
<span data-ttu-id="9922c-103">Entfernt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9922c-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="9922c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9922c-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9922c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9922c-105">DESCRIPTION</span></span>
<span data-ttu-id="9922c-106">Das Cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** entfernt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9922c-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="9922c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9922c-107">EXAMPLES</span></span>

## <span data-ttu-id="9922c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9922c-108">PARAMETERS</span></span>

### <span data-ttu-id="9922c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9922c-109">-DefaultProfile</span></span>
<span data-ttu-id="9922c-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9922c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9922c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9922c-111">-Force</span></span>
<span data-ttu-id="9922c-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9922c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9922c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9922c-113">-ResourceGroupName</span></span>
<span data-ttu-id="9922c-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9922c-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9922c-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="9922c-115">-ServerName</span></span>
<span data-ttu-id="9922c-116">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="9922c-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="9922c-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="9922c-117">-VirtualEndpointName</span></span>
<span data-ttu-id="9922c-118">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="9922c-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9922c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9922c-119">-Confirm</span></span>
<span data-ttu-id="9922c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9922c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9922c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9922c-121">-WhatIf</span></span>
<span data-ttu-id="9922c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9922c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9922c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9922c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9922c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9922c-124">CommonParameters</span></span>
<span data-ttu-id="9922c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9922c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9922c-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9922c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9922c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9922c-127">INPUTS</span></span>

### <span data-ttu-id="9922c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9922c-128">System.String</span></span>

## <span data-ttu-id="9922c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9922c-129">OUTPUTS</span></span>

### <span data-ttu-id="9922c-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="9922c-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="9922c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9922c-131">NOTES</span></span>

## <span data-ttu-id="9922c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9922c-132">RELATED LINKS</span></span>

[<span data-ttu-id="9922c-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9922c-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9922c-134">Neu – AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9922c-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9922c-135">Satz-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="9922c-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="9922c-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9922c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847391"
---
# <span data-ttu-id="ce37d-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce37d-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ce37d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce37d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce37d-103">Erstellt eine Datenbankserver-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce37d-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="ce37d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce37d-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce37d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce37d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce37d-106">Das Cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** erstellt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce37d-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ce37d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce37d-107">EXAMPLES</span></span>

## <span data-ttu-id="ce37d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce37d-108">PARAMETERS</span></span>

### <span data-ttu-id="ce37d-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce37d-109">-AsJob</span></span>
<span data-ttu-id="ce37d-110">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce37d-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce37d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce37d-111">-DefaultProfile</span></span>
<span data-ttu-id="ce37d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce37d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce37d-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ce37d-113">-FailoverPolicy</span></span>
<span data-ttu-id="ce37d-114">Gibt die Failover-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="ce37d-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce37d-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ce37d-116">Gibt den Namen der Partner Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce37d-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ce37d-117">-PartnerServerName</span></span>
<span data-ttu-id="ce37d-118">Gibt den Namen des Partnerservers an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-118">Specifies the name of the partner server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce37d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce37d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce37d-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ce37d-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="ce37d-121">-ServerName</span></span>
<span data-ttu-id="ce37d-122">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ce37d-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ce37d-123">-VirtualEndpointName</span></span>
<span data-ttu-id="ce37d-124">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ce37d-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce37d-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce37d-125">-Confirm</span></span>
<span data-ttu-id="ce37d-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce37d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce37d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce37d-127">-WhatIf</span></span>
<span data-ttu-id="ce37d-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce37d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce37d-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce37d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce37d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce37d-130">CommonParameters</span></span>
<span data-ttu-id="ce37d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce37d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce37d-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce37d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce37d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce37d-133">INPUTS</span></span>

### <span data-ttu-id="ce37d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce37d-134">System.String</span></span>

## <span data-ttu-id="ce37d-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce37d-135">OUTPUTS</span></span>

### <span data-ttu-id="ce37d-136">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="ce37d-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="ce37d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce37d-137">NOTES</span></span>

## <span data-ttu-id="ce37d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce37d-138">RELATED LINKS</span></span>

[<span data-ttu-id="ce37d-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce37d-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ce37d-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce37d-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ce37d-141">Satz-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce37d-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ce37d-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ce37d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

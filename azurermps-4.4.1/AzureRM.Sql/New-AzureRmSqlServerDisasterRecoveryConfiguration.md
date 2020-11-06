---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478862"
---
# <span data-ttu-id="74115-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="74115-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="74115-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74115-102">SYNOPSIS</span></span>
<span data-ttu-id="74115-103">Erstellt eine Datenbankserver-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="74115-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74115-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74115-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74115-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74115-105">DESCRIPTION</span></span>
<span data-ttu-id="74115-106">Das Cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** erstellt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="74115-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="74115-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74115-107">EXAMPLES</span></span>

## <span data-ttu-id="74115-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74115-108">PARAMETERS</span></span>

### <span data-ttu-id="74115-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="74115-109">-FailoverPolicy</span></span>
<span data-ttu-id="74115-110">Gibt die Failover-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="74115-110">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="74115-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74115-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="74115-112">Gibt den Namen der Partner Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="74115-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="74115-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="74115-113">-PartnerServerName</span></span>
<span data-ttu-id="74115-114">Gibt den Namen des Partnerservers an.</span><span class="sxs-lookup"><span data-stu-id="74115-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="74115-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74115-115">-ResourceGroupName</span></span>
<span data-ttu-id="74115-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="74115-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74115-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="74115-117">-ServerName</span></span>
<span data-ttu-id="74115-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="74115-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="74115-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="74115-119">-VirtualEndpointName</span></span>
<span data-ttu-id="74115-120">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="74115-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="74115-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74115-121">-Confirm</span></span>
<span data-ttu-id="74115-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74115-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74115-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74115-123">-WhatIf</span></span>
<span data-ttu-id="74115-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74115-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74115-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74115-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74115-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74115-126">-DefaultProfile</span></span>
<span data-ttu-id="74115-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74115-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74115-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74115-128">CommonParameters</span></span>
<span data-ttu-id="74115-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74115-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74115-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74115-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74115-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74115-131">INPUTS</span></span>

## <span data-ttu-id="74115-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74115-132">OUTPUTS</span></span>

## <span data-ttu-id="74115-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="74115-133">NOTES</span></span>

## <span data-ttu-id="74115-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74115-134">RELATED LINKS</span></span>

[<span data-ttu-id="74115-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="74115-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="74115-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="74115-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="74115-137">Satz-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="74115-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="74115-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="74115-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

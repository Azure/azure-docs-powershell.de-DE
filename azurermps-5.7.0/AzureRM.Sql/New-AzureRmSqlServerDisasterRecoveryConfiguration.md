---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498733"
---
# <span data-ttu-id="e45cb-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e45cb-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e45cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e45cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e45cb-103">Erstellt eine Datenbankserver-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e45cb-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e45cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e45cb-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e45cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e45cb-106">Das Cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** erstellt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e45cb-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e45cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e45cb-107">EXAMPLES</span></span>

## <span data-ttu-id="e45cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e45cb-108">PARAMETERS</span></span>

### <span data-ttu-id="e45cb-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e45cb-109">-AsJob</span></span>
<span data-ttu-id="e45cb-110">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e45cb-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="e45cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45cb-111">-DefaultProfile</span></span>
<span data-ttu-id="e45cb-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e45cb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e45cb-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e45cb-113">-FailoverPolicy</span></span>
<span data-ttu-id="e45cb-114">Gibt die Failover-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45cb-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45cb-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e45cb-116">Gibt den Namen der Partner Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45cb-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e45cb-117">-PartnerServerName</span></span>
<span data-ttu-id="e45cb-118">Gibt den Namen des Partnerservers an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="e45cb-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e45cb-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="e45cb-121">-ServerName</span></span>
<span data-ttu-id="e45cb-122">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e45cb-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e45cb-123">-VirtualEndpointName</span></span>
<span data-ttu-id="e45cb-124">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="e45cb-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45cb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e45cb-125">-Confirm</span></span>
<span data-ttu-id="e45cb-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e45cb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45cb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45cb-127">-WhatIf</span></span>
<span data-ttu-id="e45cb-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e45cb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45cb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e45cb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45cb-130">CommonParameters</span></span>
<span data-ttu-id="e45cb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e45cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45cb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45cb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45cb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e45cb-133">INPUTS</span></span>

### <span data-ttu-id="e45cb-134">Keine</span><span class="sxs-lookup"><span data-stu-id="e45cb-134">None</span></span>
<span data-ttu-id="e45cb-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e45cb-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e45cb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e45cb-136">OUTPUTS</span></span>

## <span data-ttu-id="e45cb-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e45cb-137">NOTES</span></span>

## <span data-ttu-id="e45cb-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e45cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="e45cb-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e45cb-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e45cb-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e45cb-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e45cb-141">Satz-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e45cb-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e45cb-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e45cb-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

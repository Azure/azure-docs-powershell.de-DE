---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478209"
---
# <span data-ttu-id="2e1e1-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1e1-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2e1e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1e1-103">Ändert eine Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e1e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e1e1-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e1e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e1e1-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1e1-106">Das Cmdlet " **Satz-AzureRmSqlServerDisasterRecoveryConfiguration** " ändert eine SQL-Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="2e1e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e1e1-107">EXAMPLES</span></span>

## <span data-ttu-id="2e1e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e1e1-108">PARAMETERS</span></span>

### <span data-ttu-id="2e1e1-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="2e1e1-109">-AllowDataLoss</span></span>
<span data-ttu-id="2e1e1-110">Gibt an, dass der Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="2e1e1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e1e1-111">-AsJob</span></span>
<span data-ttu-id="2e1e1-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2e1e1-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1e1-113">-DefaultProfile</span></span>
<span data-ttu-id="2e1e1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2e1e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e1e1-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="2e1e1-115">-Failover</span></span>
<span data-ttu-id="2e1e1-116">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e1e1-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2e1e1-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="2e1e1-119">-ServerName</span></span>
<span data-ttu-id="2e1e1-120">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="2e1e1-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2e1e1-121">-VirtualEndpointName</span></span>
<span data-ttu-id="2e1e1-122">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="2e1e1-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e1e1-123">-Confirm</span></span>
<span data-ttu-id="2e1e1-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e1e1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e1e1-125">-WhatIf</span></span>
<span data-ttu-id="2e1e1-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e1e1-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e1e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1e1-128">CommonParameters</span></span>
<span data-ttu-id="2e1e1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1e1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e1e1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1e1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-131">INPUTS</span></span>

### <span data-ttu-id="2e1e1-132">Keine</span><span class="sxs-lookup"><span data-stu-id="2e1e1-132">None</span></span>
<span data-ttu-id="2e1e1-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e1e1-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-134">OUTPUTS</span></span>

## <span data-ttu-id="2e1e1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e1e1-135">NOTES</span></span>

## <span data-ttu-id="2e1e1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e1e1-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e1e1-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1e1-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2e1e1-138">Neu – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1e1-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2e1e1-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1e1-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2e1e1-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="2e1e1-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

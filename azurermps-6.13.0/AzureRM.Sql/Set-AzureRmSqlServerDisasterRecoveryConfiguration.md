---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481982"
---
# <span data-ttu-id="00b08-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b08-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="00b08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00b08-102">SYNOPSIS</span></span>
<span data-ttu-id="00b08-103">Ändert eine Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="00b08-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00b08-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00b08-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00b08-105">DESCRIPTION</span></span>
<span data-ttu-id="00b08-106">Das Cmdlet " **Satz-AzureRmSqlServerDisasterRecoveryConfiguration** " ändert eine SQL-Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="00b08-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="00b08-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00b08-107">EXAMPLES</span></span>

## <span data-ttu-id="00b08-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="00b08-108">PARAMETERS</span></span>

### <span data-ttu-id="00b08-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="00b08-109">-AllowDataLoss</span></span>
<span data-ttu-id="00b08-110">Gibt an, dass der Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="00b08-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="00b08-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00b08-111">-AsJob</span></span>
<span data-ttu-id="00b08-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="00b08-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b08-113">-DefaultProfile</span></span>
<span data-ttu-id="00b08-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="00b08-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00b08-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="00b08-115">-Failover</span></span>
<span data-ttu-id="00b08-116">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="00b08-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b08-117">-ResourceGroupName</span></span>
<span data-ttu-id="00b08-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="00b08-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="00b08-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="00b08-119">-ServerName</span></span>
<span data-ttu-id="00b08-120">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="00b08-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="00b08-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="00b08-121">-VirtualEndpointName</span></span>
<span data-ttu-id="00b08-122">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="00b08-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="00b08-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00b08-123">-Confirm</span></span>
<span data-ttu-id="00b08-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00b08-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b08-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b08-125">-WhatIf</span></span>
<span data-ttu-id="00b08-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00b08-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00b08-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00b08-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b08-128">CommonParameters</span></span>
<span data-ttu-id="00b08-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b08-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b08-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b08-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00b08-131">INPUTS</span></span>

### <span data-ttu-id="00b08-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00b08-132">System.String</span></span>

## <span data-ttu-id="00b08-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00b08-133">OUTPUTS</span></span>

### <span data-ttu-id="00b08-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="00b08-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="00b08-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="00b08-135">NOTES</span></span>

## <span data-ttu-id="00b08-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00b08-136">RELATED LINKS</span></span>

[<span data-ttu-id="00b08-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b08-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="00b08-138">Neu – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b08-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="00b08-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b08-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="00b08-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="00b08-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

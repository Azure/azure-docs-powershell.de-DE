---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481434"
---
# <span data-ttu-id="4736b-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4736b-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4736b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4736b-102">SYNOPSIS</span></span>
<span data-ttu-id="4736b-103">Wechselt eine sekundäre Datenbank als primäre Datenbank, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="4736b-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4736b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4736b-104">SYNTAX</span></span>

### <span data-ttu-id="4736b-105">Nooptions (Standard)</span><span class="sxs-lookup"><span data-stu-id="4736b-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4736b-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="4736b-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4736b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4736b-107">DESCRIPTION</span></span>
<span data-ttu-id="4736b-108">Das Cmdlet " **Satz-AzureRmSqlDatabaseSecondary** " wechselt eine sekundäre Datenbank als primär, um ein Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="4736b-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="4736b-109">Dieses Cmdlet wurde als allgemeiner Konfigurationsbefehl konzipiert, ist aber derzeit auf das Initiieren eines Failovers limitiert.</span><span class="sxs-lookup"><span data-stu-id="4736b-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="4736b-110">Geben Sie den *AllowDataLoss* -Parameter an, um bei einem Ausfall ein erzwungenes Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="4736b-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="4736b-111">Sie müssen diesen Parameter nicht angeben, wenn Sie einen geplanten Vorgang wie beispielsweise die Wiederherstellungs Übung ausführen.</span><span class="sxs-lookup"><span data-stu-id="4736b-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="4736b-112">In diesem Fall wird die sekundäre Datenbank mit der primären Datenbank synchronisiert, bevor Sie gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="4736b-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="4736b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4736b-113">EXAMPLES</span></span>

## <span data-ttu-id="4736b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4736b-114">PARAMETERS</span></span>

### <span data-ttu-id="4736b-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4736b-115">-AllowDataLoss</span></span>
<span data-ttu-id="4736b-116">Gibt an, dass dieser Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="4736b-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4736b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4736b-117">-DatabaseName</span></span>
<span data-ttu-id="4736b-118">Gibt den Namen der Azure SQL-Datenbank Secondary an.</span><span class="sxs-lookup"><span data-stu-id="4736b-118">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4736b-119">-Failover</span><span class="sxs-lookup"><span data-stu-id="4736b-119">-Failover</span></span>
<span data-ttu-id="4736b-120">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="4736b-120">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4736b-121">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4736b-121">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4736b-122">Gibt den Namen der Ressourcengruppe an, der die Partner Azure SQL-Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4736b-122">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="4736b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4736b-123">-ResourceGroupName</span></span>
<span data-ttu-id="4736b-124">Gibt den Namen der Ressourcengruppe an, der die Azure SQL-Datenbank Secondary zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4736b-124">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="4736b-125">-Servername</span><span class="sxs-lookup"><span data-stu-id="4736b-125">-ServerName</span></span>
<span data-ttu-id="4736b-126">Gibt den Namen des SQL-Servers an, der die Azure SQL-Datenbank Secondary hostet.</span><span class="sxs-lookup"><span data-stu-id="4736b-126">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="4736b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4736b-127">-Confirm</span></span>
<span data-ttu-id="4736b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4736b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4736b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4736b-129">-WhatIf</span></span>
<span data-ttu-id="4736b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4736b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4736b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4736b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4736b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4736b-132">-DefaultProfile</span></span>
<span data-ttu-id="4736b-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4736b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4736b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4736b-134">CommonParameters</span></span>
<span data-ttu-id="4736b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4736b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4736b-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4736b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4736b-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4736b-137">INPUTS</span></span>

###  
<span data-ttu-id="4736b-138">Sie können Instanzen des **Daten Bank** Objekts für die sekundäre Datenbank übergeben, um einen Failover durchführen und die primäre Datenbank zu diesem Cmdlet machen.</span><span class="sxs-lookup"><span data-stu-id="4736b-138">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="4736b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4736b-139">OUTPUTS</span></span>

###  
<span data-ttu-id="4736b-140">Dieses Cmdlet gibt einen **ReplicationLink** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4736b-140">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="4736b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4736b-141">NOTES</span></span>

## <span data-ttu-id="4736b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4736b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4736b-143">Neu – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4736b-143">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="4736b-144">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4736b-144">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="4736b-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="4736b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

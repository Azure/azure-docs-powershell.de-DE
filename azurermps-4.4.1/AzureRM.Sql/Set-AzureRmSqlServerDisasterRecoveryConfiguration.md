---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665245"
---
# <span data-ttu-id="a576f-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a576f-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a576f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a576f-102">SYNOPSIS</span></span>
<span data-ttu-id="a576f-103">Ändert eine Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a576f-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a576f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a576f-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a576f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a576f-105">DESCRIPTION</span></span>
<span data-ttu-id="a576f-106">Das Cmdlet " **Satz-AzureRmSqlServerDisasterRecoveryConfiguration** " ändert eine SQL-Datenbankserver-Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a576f-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="a576f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a576f-107">EXAMPLES</span></span>

## <span data-ttu-id="a576f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a576f-108">PARAMETERS</span></span>

### <span data-ttu-id="a576f-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="a576f-109">-AllowDataLoss</span></span>
<span data-ttu-id="a576f-110">Gibt an, dass der Failover-Vorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="a576f-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="a576f-111">-Failover</span><span class="sxs-lookup"><span data-stu-id="a576f-111">-Failover</span></span>
<span data-ttu-id="a576f-112">Gibt an, dass es sich bei diesem Vorgang um ein Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="a576f-112">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="a576f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a576f-113">-ResourceGroupName</span></span>
<span data-ttu-id="a576f-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a576f-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a576f-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="a576f-115">-ServerName</span></span>
<span data-ttu-id="a576f-116">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="a576f-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="a576f-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a576f-117">-VirtualEndpointName</span></span>
<span data-ttu-id="a576f-118">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="a576f-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="a576f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a576f-119">-Confirm</span></span>
<span data-ttu-id="a576f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a576f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a576f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a576f-121">-WhatIf</span></span>
<span data-ttu-id="a576f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a576f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a576f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a576f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a576f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a576f-124">-DefaultProfile</span></span>
<span data-ttu-id="a576f-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a576f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a576f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a576f-126">CommonParameters</span></span>
<span data-ttu-id="a576f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a576f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a576f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a576f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a576f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a576f-129">INPUTS</span></span>

## <span data-ttu-id="a576f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a576f-130">OUTPUTS</span></span>

## <span data-ttu-id="a576f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a576f-131">NOTES</span></span>

## <span data-ttu-id="a576f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a576f-132">RELATED LINKS</span></span>

[<span data-ttu-id="a576f-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a576f-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a576f-134">Neu – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a576f-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a576f-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a576f-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a576f-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a576f-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: bbb6841f615444175de93e59d4536a07461490de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663812"
---
# <span data-ttu-id="b07e3-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b07e3-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b07e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b07e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b07e3-103">Ruft eine Datenbankserver-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b07e3-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b07e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b07e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b07e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b07e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b07e3-106">Das Cmdlet " **Get-AzureRmSqlServerDisasterRecoveryConfiguration** " Ruft eine SQL Database Server-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b07e3-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b07e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b07e3-107">EXAMPLES</span></span>

## <span data-ttu-id="b07e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07e3-108">PARAMETERS</span></span>

### <span data-ttu-id="b07e3-109">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07e3-109">-ResourceGroupName</span></span>
<span data-ttu-id="b07e3-110">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b07e3-110">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b07e3-111">-Servername</span><span class="sxs-lookup"><span data-stu-id="b07e3-111">-ServerName</span></span>
<span data-ttu-id="b07e3-112">Gibt den Namen des SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="b07e3-112">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="b07e3-113">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b07e3-113">-VirtualEndpointName</span></span>
<span data-ttu-id="b07e3-114">Gibt den Namen des virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="b07e3-114">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="b07e3-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b07e3-115">-Confirm</span></span>
<span data-ttu-id="b07e3-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b07e3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07e3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07e3-117">-WhatIf</span></span>
<span data-ttu-id="b07e3-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b07e3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07e3-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b07e3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07e3-120">-DefaultProfile</span></span>
<span data-ttu-id="b07e3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b07e3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07e3-122">CommonParameters</span></span>
<span data-ttu-id="b07e3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07e3-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07e3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b07e3-125">INPUTS</span></span>

## <span data-ttu-id="b07e3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b07e3-126">OUTPUTS</span></span>

## <span data-ttu-id="b07e3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b07e3-127">NOTES</span></span>

## <span data-ttu-id="b07e3-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b07e3-128">RELATED LINKS</span></span>

[<span data-ttu-id="b07e3-129">Neu – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b07e3-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b07e3-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b07e3-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b07e3-131">Satz-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b07e3-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b07e3-132">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b07e3-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


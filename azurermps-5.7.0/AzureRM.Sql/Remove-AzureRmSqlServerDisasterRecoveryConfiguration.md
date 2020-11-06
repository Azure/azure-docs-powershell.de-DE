---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482681"
---
# <span data-ttu-id="8ce5b-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ce5b-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="8ce5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ce5b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce5b-103">Entfernt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ce5b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ce5b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce5b-106">Das Cmdlet **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** entfernt eine SQL Database Server-System Wiederherstellungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8ce5b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ce5b-107">EXAMPLES</span></span>

## <span data-ttu-id="8ce5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ce5b-108">PARAMETERS</span></span>

### <span data-ttu-id="8ce5b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce5b-109">-DefaultProfile</span></span>
<span data-ttu-id="8ce5b-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8ce5b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ce5b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8ce5b-111">-Force</span></span>
<span data-ttu-id="8ce5b-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ce5b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce5b-113">-ResourceGroupName</span></span>
<span data-ttu-id="8ce5b-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8ce5b-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="8ce5b-115">-ServerName</span></span>
<span data-ttu-id="8ce5b-116">Gibt den Namen eines SQL-Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="8ce5b-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="8ce5b-117">-VirtualEndpointName</span></span>
<span data-ttu-id="8ce5b-118">Gibt den Namen eines virtuellen Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ce5b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ce5b-119">-Confirm</span></span>
<span data-ttu-id="8ce5b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce5b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce5b-121">-WhatIf</span></span>
<span data-ttu-id="8ce5b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce5b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce5b-124">CommonParameters</span></span>
<span data-ttu-id="8ce5b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce5b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce5b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce5b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ce5b-127">INPUTS</span></span>

### <span data-ttu-id="8ce5b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="8ce5b-128">None</span></span>
<span data-ttu-id="8ce5b-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ce5b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ce5b-130">OUTPUTS</span></span>

## <span data-ttu-id="8ce5b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ce5b-131">NOTES</span></span>

## <span data-ttu-id="8ce5b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ce5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ce5b-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ce5b-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8ce5b-134">Neu – AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ce5b-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8ce5b-135">Satz-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ce5b-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8ce5b-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8ce5b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

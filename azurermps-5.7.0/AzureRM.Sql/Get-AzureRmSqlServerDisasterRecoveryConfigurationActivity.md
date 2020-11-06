---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502338"
---
# <span data-ttu-id="bb4bd-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="bb4bd-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="bb4bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4bd-103">Ruft die Aktivität für eine Datenbankserver-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb4bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb4bd-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb4bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4bd-106">Das Cmdlet " **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** " Ruft die Aktivität für eine SQL Database Server-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="bb4bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb4bd-107">EXAMPLES</span></span>

## <span data-ttu-id="bb4bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb4bd-108">PARAMETERS</span></span>

### <span data-ttu-id="bb4bd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4bd-109">-DefaultProfile</span></span>
<span data-ttu-id="bb4bd-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb4bd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb4bd-111">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="bb4bd-111">-OperationId</span></span>
<span data-ttu-id="bb4bd-112">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-112">Specifies the operation ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4bd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb4bd-113">-ResourceGroupName</span></span>
<span data-ttu-id="bb4bd-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb4bd-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bb4bd-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="bb4bd-116">Gibt den Namen der Server System-Wiederherstellungskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4bd-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="bb4bd-117">-ServerName</span></span>
<span data-ttu-id="bb4bd-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="bb4bd-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb4bd-119">-Confirm</span></span>
<span data-ttu-id="bb4bd-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb4bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4bd-121">-WhatIf</span></span>
<span data-ttu-id="bb4bd-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4bd-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb4bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4bd-124">CommonParameters</span></span>
<span data-ttu-id="bb4bd-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4bd-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4bd-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb4bd-127">INPUTS</span></span>

### <span data-ttu-id="bb4bd-128">Keine</span><span class="sxs-lookup"><span data-stu-id="bb4bd-128">None</span></span>
<span data-ttu-id="bb4bd-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bb4bd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb4bd-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb4bd-130">OUTPUTS</span></span>

## <span data-ttu-id="bb4bd-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb4bd-131">NOTES</span></span>

## <span data-ttu-id="bb4bd-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb4bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="bb4bd-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="bb4bd-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
